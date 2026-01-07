# Plan: Implement AWS resource support for Developers RAG

## 0) Goals and scope

- Goal: Let developers ask questions about AWS resources (what they are, how to configure/use them, limits, errors, examples) and get accurate, source-cited answers.
- Scope (initial): 3 services for local MVP (S3, IAM, Lambda).
- Out-of-scope (for now): Billing/account governance, niche services, per-account introspection unless a live AWS tool is added.

## 1) Architecture shape

- Data pipeline: Fetch -> clean/normalize -> chunk -> embed -> store (vector + metadata) -> schedule refresh.
- Retrieval: Hybrid (lexical + vector) with metadata filters (service, doc type, version) and reranking.
- Generation: Retrieval-augmented synthesis with source citations and safety guardrails.
- Optional tools: AWS SDK/CLI-backed tool for live descriptions (limits, ARNs, region defaults) gated behind feature flag.

## 2) Data sources (prioritized)

- AWS Developer Guides + API References (docs.aws.amazon.com) for each in-scope service.
- AWS CLI help text (aws <service> help) for flags and examples (convert to markdown once).
- CloudFormation Resource Spec + AWS SAM/Serverless reference for IaC shapes.
- AWS Well-Architected + service best-practice pages for guardrails.
- Changelog/What’s New feeds for freshness deltas.

## 3) Ingestion and normalization

- Fetchers: site map or curated URL lists per service; add last-modified/version metadata.
- Convert HTML/man pages to markdown; strip nav/ads; preserve code blocks, tables, parameter lists.
- Normalize entities: service code (e.g., s3), doc type (dev_guide, api_ref, cfn_spec, cli_help), region (if applicable), version/date, URL.
- Deduplication: canonicalize URLs; hash content to skip unchanged docs; drop near-duplicates (minhash).

## 4) Chunking strategy

- Chunk size: 200–400 tokens for prose; 80–150 lines for CLI/API parameter tables; keep examples/code blocks intact.
- Semantic chunking cues: section headers, list boundaries, table rows grouped by parameter category.
- Metadata per chunk: service, doc_type, title/section, url, version/date, heading path, content hash.

## 5) Embeddings and storage

- Embedding model (local): bge-base or nomic-embed-text; validate with a pilot eval.
- Store (local): pgvector for vectors + local filesystem for raw markdown + manifest of source/version.
- Indexing: Upsert by content hash; maintain service-level collections to speed filters.

## 6) Retrieval pipeline

- Query preprocessing: Detect target service(s) via keywords/entity mapping (e.g., “bucket policy” -> s3, “execution role” -> iam).
- Hybrid search: BM25/keyword over headings + vector kNN; combine via reciprocal rank fusion.
- Rerank: Cross-encoder reranker on top 50 -> top 5–8 contexts.
- Answer assembly: Enforce citations (URL + heading) and include examples when present.
- Guardrails: Refuse speculative config (e.g., IAM policies) without sources; highlight regional differences when metadata says region-specific.

## 7) Optional live AWS tool

- Add a tool that calls AWS SDK/CLI (read-only) to fetch current limits, ARNs, defaults; requires credentials config and explicit opt-in.
- Cache responses per account/region; mark tool outputs as “live data” and do not mix with static docs without labeling.

## 8) Freshness and jobs

- Scheduler: Daily crawl for changed sitemaps; weekly full re-crawl for drift; immediate fetch on “What’s New” deltas.
- Use ETag/Last-Modified to skip unchanged; emit metrics on add/update/delete counts.
- Alerting: On fetch failures per service; retry with backoff; quarantine malformed pages.

## 9) Evaluation

- Build gold set: 150–300 questions across in-scope services (how-to, limits, error resolution, examples).
- Metrics: Retrieval recall@k, MRR, answer correctness, grounding (citation matches), hallucination rate.
- Regression suite: Run after each data refresh and model change; track by service to catch regressions.

## 10) Delivery plan (milestones)

- M1: Local-first CLI skeleton (fetch -> clean -> chunk -> embed -> store) for 1 service (S3) + basic hybrid search + citation-enforced answers.
- M2: Expand to 3 services (S3, IAM, Lambda); add reranker + eval harness; tighten chunking/dedup.
- M3: CLI polish (source-rich answers, examples-first layout), scheduler and metrics, observability and alerts.
- M4: Optional: live AWS tool and/or lightweight UI once CLI is stable.

## 13) CLI UX (local-first)

- Command: `rag ask "question"` with optional flags `--service`, `--sources`, `--debug`.
- Output: Answer first, then citations with URLs + headings; include examples when present.
- Offline mode: No network access after initial ingestion; allow `rag ingest` to refresh.

## 11) Observability and ops

- Metrics: crawl success, doc freshness age, index size per service, query latency, retrieval overlap, grounding rate.
- Logs/traces: per request include detected services, retrieval candidates, rerank scores, tool calls.
- Dashboards + alerts: freshness drift, latency SLO breaches, hallucination spikes in eval/feedback.

## 12) Security and compliance

- No customer data in index; store only public AWS docs unless live tool opt-in is enabled.
- Credentials isolation for live tool; least-privilege IAM policy; no write actions.
- Provenance: store source URL and version; include in every answer.
