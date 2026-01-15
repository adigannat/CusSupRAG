# Amazon S3 Pricing
Service: S3
Doc: Pricing

Object storage built to retrieve any amount of data from anywhere

Pay only for what you use. There is no minimum charge. Amazon S3 cost components are storage pricing, request and data retrieval pricing, data transfer and transfer acceleration pricing, data management and insights feature pricing, replication pricing, and transform and query feature pricing.

## Storage pricing
You pay for storing objects in your S3 buckets. The rate you're charged depends on your objects' size, how long you stored the objects during the month, and the storage class-S3 Standard, S3 Intelligent-Tiering, S3 Standard-Infrequent Access, S3 One Zone-Infrequent Access, S3 Express One Zone, S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval (Formerly S3 Glacier), and S3 Glacier Deep Archive. You pay a monthly monitoring and automation charge per object stored in the S3 Intelligent-Tiering storage class to monitor access patterns and move objects between access tiers. In S3 Intelligent-Tiering there are no retrieval charges, and no additional tiering charges apply when objects are moved between access tiers.

There are per-request ingest charges when using PUT, COPY, or lifecycle rules to move data into any S3 storage class. Consider the ingest or transition cost before moving objects into any storage class. Estimate your costs using the AWS Pricing Calculator. To find the best S3 storage class for your workload, learn more here.

Please note that we list Storage Requests and Data Retrievals Pricing below the Storage Pricing table.

Region:

Middle East (UAE)

## Storage pricing
S3 Standard - General purpose storage for any type of data, typically used for frequently accessed data
First 50 TB / Month $0.025 per GB
Next 450 TB / Month $0.024 per GB
Over 500 TB / Month $0.023 per GB
S3 Intelligent - Tiering _ - Automatic cost savings for data with unknown or changing access patterns
Monitoring and Automation, All Storage / Month (Objects > 128 KB) $0.0025 per 1,000 objects
Frequent Access Tier, First 50 TB / Month $0.025 per GB
Frequent Access Tier, Next 450 TB / Month $0.024 per GB
Frequent Access Tier, Over 500 TB / Month $0.023 per GB
Infrequent Access Tier, All Storage / Month $0.0138 per GB
Archive Instant Access Tier, All Storage / Month $0.005 per GB
S3 Intelligent - Tiering _ - Optional asynchronous Archive Access tiers
Archive Access Tier, All Storage / Month $0.00405 per GB
Deep Archive Access Tier, All Storage / Month $0.0018 per GB
S3 Standard - Infrequent Access ** - For long lived but infrequently accessed data that needs millisecond access
All Storage / Month $0.0138 per GB
S3 Express One Zone - High-performance storage for your most frequently accessed data
All Storage / Month N/A per GB
S3 Glacier Instant Retrieval \*** - For long-lived archive data accessed once a quarter with instant retrieval in milliseconds
All Storage / Month $0.005 per GB
S3 Glacier Flexible Retrieval **_ - For long-term backups and archives with retrieval option from 1 minute to 12 hours
All Storage / Month $0.00405 per GB
S3 Glacier Deep Archive _** - For long-term data archiving that is accessed once or twice in a year and can be restored within 12 hours
All Storage / Month $0.0018 per GB
S3 One Zone - Infrequent Access \*\* - For re-creatable infrequently accessed data that needs millisecond access
All Storage / Month $0.01104 per GB

- S3 Intelligent-Tiering can store objects smaller than 128 KB, but auto-tiering has a minimum eligible object size of 128 KB. These smaller objects will not be monitored and will always be charged at the Frequent Access tier rates, with no monitoring and automation charge. For each object archived to the Archive Access tier or Deep Archive Access tier in S3 Intelligent-Tiering, Amazon S3 uses 8 KB of storage for the name of the object and other metadata (billed at S3 Standard storage rates) and 32 KB of storage for index and related metadata (billed at S3 Glacier Flexible Retrieval and S3 Glacier Deep Archive storage rates).

\*\* S3 Standard-IA and S3 One Zone-IA storage have a minimum billable object size of 128 KB. Smaller objects may be stored but will be charged for 128 KB of storage at the appropriate storage class rate. S3 Standard-IA, and S3 One Zone-IA storage are charged for a minimum storage duration of 30 days, and objects deleted before 30 days incur a pro-rated charge equal to the storage charge for the remaining days. Objects that are deleted, overwritten, or transitioned to a different storage class before 30 days will incur the normal storage usage charge plus a pro-rated charge for the remainder of the 30-day minimum. This includes objects that are deleted as a result of file operations performed by File Gateway. Objects stored for 30 days or longer will not incur a 30-day minimum charge.

\*\*\* For each object that is stored in the S3 Glacier Flexible Retrieval and S3 Glacier Deep Archive storage classes, AWS charges for 40 KB of additional metadata for each archived object, with 8 KB charged at S3 Standard rates and 32 KB charged at S3 Glacier Flexible Retrieval or S3 Deep Archive rates. This allows you to get a real-time list of all of your S3 objects using the S3 LIST API or the S3 Inventory report. S3 Glacier Instant Retrieval has a minimum billable object size of 128 KB. Smaller objects may be stored but will be charged for 128 KB of storage at the appropriate storage class rate. Objects that are archived to S3 Glacier Instant Retrieval and S3 Glacier Flexible Retrieval are charged for a minimum storage duration of 90 days, and S3 Glacier Deep Archive has a minimum storage duration of 180 days. Objects deleted prior to the minimum storage duration incur a pro-rated charge equal to the storage charge for the remaining days. Objects that are deleted, overwritten, or transitioned to a different storage class before the minimum storage duration will incur the normal storage usage charge plus a pro-rated storage charge for the remainder of the minimum storage duration. Objects stored longer than the minimum storage duration will not incur a minimum storage charge. For customers using the S3 Glacier direct API, pricing for API can be found on the S3 Glacier API pricing page.

## Requests & data retrievals
You pay for requests made against your S3 buckets and objects. S3 request costs are based on the request type, and are charged on the quantity of requests as listed in the table below. When you use the Amazon S3 console to browse your storage, you incur charges for GET, LIST, and other requests that are made to facilitate browsing. Charges are accrued at the same rate as requests that are made using the API/SDK. Reference the S3 developer guide for technical details on the following request types: PUT, COPY, POST, LIST, GET, SELECT, Lifecycle Transition, and Data Retrievals. DELETE and CANCEL requests are free. LIST requests for any storage class are charged at the same rate as S3 Standard PUT, COPY, and POST requests. You pay for retrievals when you GET an object stored in the S3 Standard - Infrequent Access, S3 One Zone - Infrequent Access, or S3 Glacier Instant Retrieval storage classes. When you restore an archive from the S3 Glacier Flexible Retrieval or S3 Glacier Deep Archive storage classes, you pay for retrievals as a part of the restore request. When you restore an archive, you are paying for both the archive (charged at the S3 Glacier Flexible Retrieval or S3 Glacier Deep Archive rate) and a copy, accessible with GET using the same object key, that you restored temporarily (charged at the S3 Standard storage rate for a duration of time you choose). Reference the S3 developer guide for technical details on Data Retrievals.

S3 Lifecycle Transition request pricing below represents requests to that storage class. For example, transitioning data from S3 Standard to S3 Standard-Infrequent Access will be charged $0.01 per 1,000 requests.

There are no retrieval charges in S3 Intelligent-Tiering. If an object in the infrequent access tier is accessed later, it is automatically moved back to the frequent access tier. No additional tiering charges apply when objects are moved between access tiers within the S3 Intelligent-Tiering storage class.

Region:

Middle East (UAE)

PUT, COPY, POST, LIST requests (per 1,000 requests) GET, SELECT, and all other requests (per 1,000 requests) Lifecycle transition requests into (per 1,000 requests) Data retrieval requests (per 1,000 requests) Data uploads (per GB) Data retrievals (per GB)
S3 Standard $0.0055 $0.00044 n/a n/a n/a n/a
S3 Intelligent-Tiering \* $0.0055 $0.00044 $0.01 n/a n/a n/a
Frequent Access n/a n/a n/a n/a n/a n/a
Infrequent Access n/a n/a n/a n/a n/a n/a
Archive Instant n/a n/a n/a n/a n/a n/a
Archive Access, Standard n/a n/a n/a n/a n/a n/a
Archive Access, Bulk n/a n/a n/a n/a n/a n/a
Archive Access, Expedited n/a n/a n/a $12.10 n/a $0.033
Deep Archive Access, Standard n/a n/a n/a n/a n/a n/a
Deep Archive Access, Bulk n/a n/a n/a n/a n/a n/a
S3 Standard-Infrequent Access ** $0.01 $0.001 $0.01 n/a n/a $0.01
S3 Glacier Instant Retrieval \*\*** $0.02 $0.01 $0.02 n/a n/a $0.03
S3 Glacier Flexible Retrieval \***\* $0.0363 $0.00044 $0.0363 See below n/a See below
Expedited n/a n/a n/a $12.10 n/a $0.033
Standard n/a n/a n/a $0.0605 n/a $0.011
Bulk \*\*** n/a n/a n/a n/a n/a n/a
S3 Glacier Deep Archive \***\* $0.0605 $0.00044 $0.0605 See below n/a See below
Standard n/a n/a n/a $0.121 n/a $0.022
Bulk n/a n/a n/a $0.0275 n/a $0.0033
S3 One Zone-Infrequent Access ** $0.01 $0.001 $0.01 n/a n/a $0.01
S3 Lifecycle Transition request pricing above represents requests to that storage class.

- S3 Intelligent-Tiering standard and bulk data retrieval and restore requests are free of charge for all five access tiers: Frequent, Infrequent, Archive Instant, Archive, and Deep Archive access tiers. Subsequent restore requests called on objects already being restored will be billed as a GET request. Expedited retrievals are available for the S3 Intelligent-Tiering Archive Access Tier and are charged at the Expedited request and retrieval rate.

\*\* S3 Standard-IA and S3 One Zone-IA storage are charged for a minimum storage duration of 30 days. Objects that are deleted, overwritten, or transitioned to a different storage class before the minimum storage duration will incur the normal storage usage charge plus a pro-rated charge for the remainder of the minimum storage duration. Objects stored longer than the minimum storage duration will not incur aminimum charge.

\*\*\* S3 Express One Zone is the only storage class that supports the RenameObject API, which is priced the same as PUT, COPY, POST, LIST requests (per 1,000 requests) in S3 Express One Zone. There are no data upload or data retrieval changes with the RenameObject API.

\*\*\*\* Objects that are archived to S3 Glacier Instant Retrieval and S3 Glacier Flexible Retrieval are charged for a minimum storage duration of 90 days, and S3 Glacier Deep Archive has a minimum storage duration of 180 days. Objects deleted prior to the minimum storage duration incur a pro-rated charge equal to the storage charge for the remaining days. Objects that are deleted, overwritten, or transitioned to a different storage class before the minimum storage duration will incur the normal storage usage charge plus a pro-rated charge for the remainder of the minimum storage duration. Objects stored longer than the minimum storage duration will not incur a minimum charge. S3Glacier Flexible Retrieval Bulk data retrievals and requests are free of charge.

**\*** Provisioned Capacity Units allow you to provision capacity for expedited retrievals from S3 Glacier for a given month. Each provisioned capacity unit can provide at least three expedited retrievals every five minutes and up to 150 MB/s of retrieval throughput.

S3 Tables pricing
Amazon S3 Tables deliver S3 storage that is specifically optimized for analytics workloads. With S3 Tables, you pay for storage, requests, and an object monitoring fee per object stored in table buckets. Table buckets are designed to perform continual table maintenance to automatically optimize query efficiency and storage cost over time, even as your data lake scales and evolves.

By default, compaction periodically combines smaller objects into fewer, larger objects to improve query performance. When compaction is enabled, you are charged for the number of objects and the bytes processed during compaction.

Region:

Middle East (UAE)
S3 Tables storage pricing
S3 Tables Standard - Storage specifically optimized for analytics workloads with improved query performance
First 50 TB / Month $0.0288 per GB
Next 450 TB / Month $0.0276 per GB
Over 500 TB / Month $0.0265 per GB
S3 Tables Intelligent - Tiering\* - Automatic cost saving for tabular data with unknown or changing access patterns
Frequent Access Tier, First 50 TB / Month $0.0288 per GB
Frequent Access Tier, Next 450 TB / Month $0.0276 per GB
Frequent Access Tier, Over 500 TB / Month $0.0265 per GB
Infrequent Access Tier, All Storage / Month $0.0159 per GB
Archive Instant Access Tier, All Storage / Month $0.0058 per GB

- S3 Tables Intelligent-Tiering can store objects smaller than 128 KB, but auto-tiering has a minimum eligible object size of 128 KB. As part of table maintenance, compaction can combine these smaller objects into fewer, larger objects and commits them back to your table as a new snapshot. The newly compacted files become eligible for auto-tiering if the new file is 128 KB or larger.

S3 Tables requests pricing
PUT, POST, LIST requests (per 1,000 requests) GET, and all other requests (per 1,000 requests)
S3 Tables - Standard $0.0055 $0.00044
S3 Tables - Intelligent-Tiering $0.0055 $0.00044
Frequent Access n/a n/a
Infrequent Access n/a n/a
Archive Instant Access n/a n/a
S3 Tables monitoring pricing
Monitoring, All Storage / Month $0.025 per 1,000 objects
S3 Tables maintenance pricing
Compaction - Objects* $0.0022 per 1,000 objects processed
Compaction - Data Processed with Binpack (Default) $0.005 per GB processed
Compaction - Data Processed with Sort or Z-order $0.01 per GB processed
* Compaction charges are incurred when objects stored in your table buckets are processed for automatic compaction. These charges will not be incurred if you disable automatic compaction in a specified table in your S3 table bucket.

S3 Tables replication pricing
For S3 Tables replication, you pay the S3 Tables charges for storage in the destination table, for replication PUT requests, for table updates (commits), and for object monitoring on the replicated data. For cross-Region table replication, you also pay for inter-Region Data Transfer OUT from S3 to the destination Region based on the Region pair.

Table updates replicated $0.01 per 1,000 table updates replicated
S3 Tables pricing example:
You use a daily ETL job to pre-process data from different structured and unstructured sources and update an Apache Iceberg table stored in the S3 Standard storage class in your table bucket once a day. This update creates 1,000 new data files with an average object size of 5 MB and 3 metadata files with an average object size of 10 KB. Your table's users frequently perform queries on your dataset and generate 500,000 GET requests per month. You do not have a sort order defined for your table. To optimize query performance, you enable automatic compaction on S3 Tables. At the end of the month, your table is 1 TB in size with an average object size of 100 MB. This example uses the US-West (Oregon) AWS Region.

Your charges would be calculated as follows:

Amazon S3 Tables storage charge ($/GB)
S3 Tables - Standard storage price is $0.0265 per GB for the first 50 TB per month
Since you are storing 1 TB of data in your table, your charge would be:
S3 Tables storage charge: 1 TB (1,024 GB) \* $0.0265/GB = $27.14

Amazon S3 Tables PUT request charge ($/1,000 requests)
S3 Tables - Standard PUT request price is $0.005 per 1,000 requests
Since you are adding 1,000 data files and 3 metadata files per day to your table, your charge would be:
S3 Tables PUT request charge: 1,003 PUT requests/day _ 30 days = 30,090 PUT requests/month _
$0.005/1,000 requests = $0.15

Amazon S3 Tables GET request charge ($/1,000 requests)
S3 Tables - Standard GET request price is $0.0004 per 1,000 requests
Since you are performing 500,000 GET requests per month, your charge would be:
S3 Tables GET request charge: 500,000 GET requests/month \* $0.0004/1,000 requests = $0.20

Amazon S3 Tables object monitoring charge ($/1,000 objects)
S3 Tables object monitoring price is $0.025 per 1,000 objects
Since you have a 1 TB table with an average object size of 100 MB, your charge would be:
S3 Tables object monitoring charge: 1 TB (1,048,576 MB)/100 MB = 10,486 objects \* $0.025/1,000 objects = $0.26

Amazon S3 Tables compaction charge ($/1,000 objects and $/GB processed)
S3 Tables compaction price is $0.002 per 1,000 objects processed and $0.005 per GB processed for default binpack compaction
Since S3 Tables will process 30,000 new 5 MB data files added to your table, your charge would be:
S3 Tables compaction charge: 30,000 data files _ $0.002/1,000 objects = $0.06 and 30,000 data files _ 5
MB = 150,000 MB (146.48 GB) \* $0.005 per GB processed = $0.73.

Total charges
S3 Tables storage charge = $27.14
S3 Tables PUT request charge = $0.15
S3 Tables GET request charge = $0.20
S3 Tables object monitoring charge = $0.26
S3 Tables compaction - objects processed charge = $0.06
S3 Tables compaction - data processed charge = $0.73
S3 Tables total = $28.54

S3 Tables replication pricing example:
You have an Apache Iceberg table in US-West (Oregon) that you replicate to US-East (N. Virginia). Your hourly ETL job updates the table 24 times per day, creating an average of 21 new data files per update with an average object size of 10 MB.

Your replication charges would be calculated as follows:

Amazon S3 Tables replication PUT request charge ($/1,000 requests)
S3 Tables PUT request price is $0.005 per 1,000 requests Since you are replicating approximately 500 data files per day to the destination table, your charge would be:
S3 Tables replication PUT request charge: 21 PUT requests/hour _ 24 hours = 504 PUT requests/day _ 30 days = 15,120 PUT requests/month \* $0.005/1,000 requests = $0.08

Amazon S3 Tables replication table update charge ($/1,000 table updates)
S3 Tables table update price is $0.010 per 1,000 table updates
Since you are updating your table 24 times per day, your charge would be:
S3 Tables replication table update charge: 24 table updates/day _ 30 days = 720 table updates/month _ $0.010/1,000 table updates = $0.0072

Amazon S3 inter-Region Data Transfer OUT charge ($/GB)
Inter-region Data Transfer OUT from US-West (Oregon) to US-East (N. Virginia) is $0.02 per GB
Since you are transferring approximately 504 data files _ 10 MB = 5,040 MB (4.92 GB) per day, your charge would be:
Inter-region Data Transfer OUT charge: 4.92 GB/day _ 30 days = 147.66 GB \* $0.02/GB = $2.95

Total S3 Tables replication charges:
S3 Tables replication PUT request charge = $0.08
S3 Tables replication table update charge = $0.0072
Inter-region Data Transfer OUT charge = $2.95
S3 Tables replication total = $3.04

Note: You also pay for storage and object monitoring for the replicated table in the destination region. See the S3 Tables pricing example above for details.

S3 Vectors
Amazon S3 Vectors provides cost-effective, elastic, and durable vector storage at up to 90% lower costs for uploading, storing, and querying vectors. With S3 Vectors, you can power RAG and other semantic search workloads at scale, at a fraction of the cost for storage, requests, data uploaded, and data queried.

PUT cost
PUT pricing is based on logical GB of the vectors you upload, where each vector is the sum of its logical vector data, metadata, and key. You can upload multiple vectors in a single PUT request, maximizing upload throughput and minimizing upload costs.

Storage cost
Total storage is the sum of logical storage across your indexes, where the size of your storage is determined by the number of vectors you store and their size. Vector size is determined by:

1. Vector data: Each vector has a size determined by number of dimensions. Each dimension equals 4 bytes of storage per vector, so for example, a 1024-dimensional vector requires 4 KB of logical vector data.

2. Metadata: You can store both filterable and non-filterable metadata with your vector. Non-filterable metadata is used to return information as a part of query results while filterable metadata can also be used to filter query results.

3. Key: Each vector is associated with a key. Keys require 1 byte of storage per character.

Query cost
Query charges include a per API charge in addition to a $/TB charge based on the average vector size, including vector data, key, and filterable metadata, multiplied by the number of vectors in the index you're querying. As your vector index grows, data processing charges for query increase proportionally; however, at larger scale, you benefit from lower $/TB pricing above 100K in your vector index.

Vector pricing
Region:

Europe (Frankfurt)
S3 Vectors storage pricing
S3 Vector Storage /Month - monthly logical storage of vector data, key, and metadata $0.064 per GB
S3 Vectors request pricing

PUT requests (per GB)1 GET, LIST and all other requests (per 1,000 requests)
S3 Vectors Requests $0.214 per GB $0.059
[1] PUT is subject to a minimum charge of 128KB per PUT. To lower PUT costs, you can batch multiple vectors per PUT request.

S3 Vectors query pricing

S3 Vectors query requests (per 1,000 requests) $0.0027
S3 Vector data2 - sum of vectors per index multiplied by average vector size (vector data, key, and filterable metadata)
First 100 thousand vectors $0.0043 per TB
Over 100 thousand vectors $0.0021 per TB
[2] Note that it can take up to a day for the storage used by overwritten or deleted vectors to be reclaimed. These vectors are removed from query results immediately, but will continue to be included in the index's storage size during this time. As a result, workloads that frequently overwrite or delete the same keys can temporarily see higher query costs.

Pricing example 1:
You are building a RAG workflow to provide accurate and relevant text responses to customers. You have 10 million vectors, each consisting of 4 KB vector data, 1 KB of filterable metadata, 1 KB of non-filterable metadata, and a key (0.17 KB each), totaling 6.17KB per vector. The 10 million vectors are split into 40 indexes for each of your customers, consisting of 250,000 vectors each. You update the vectors in your vector index every six months, removing old vectors and uploading new ones. This results in PUT of ~16.7% of your data per month. This example uses pricing for the US East (N. Virginia) AWS Region.

With the S3 Vectors query API, you can perform similarity search against a vector you send with your API call; you also have the option to filter the results inline using filterable metadata. Queries are charged at $2.5/MM API calls, in addition to a $/TB charge for data processed. Data processed is calculated by multiplying your average vector size by the number of vectors in your index. Average vector size for query includes vector data, key, and filterable metadata per vector. Non-filterable metadata is not included in data processed for query; you can return non-filterable metadata in your query results at no additional cost. In this example, for each query you will be charged $0.004/TB based on the first 100K vectors processed, and then $0.002/TB for the next 150K records, both at an average vector size of 5.17 KB.

S3 Vectors storage charge
((4 bytes _ 1024 dimensions) vector data/vector + 1 KB filterable metadata/vector + 1 KB non-filterable metadata/vector + 0.17 KB key/vector) = 6.17 KB logical storage per average vector
6.17 KB/average vector _ 250,000 vectors _ 40 vector indexes = 59 GB logical storage
Total monthly storage cost = 59 GB _ $0.06/GB per month = $3.54

S3 Vectors PUT charge
Total monthly PUT cost = 1 full upload/6 months _ 59 GB total storage _ $0.20/GB = $1.97

S3 Vectors Query charge

((4 bytes _ 1024 dimensions) vector data/vector + 1 KB filterable metadata/vector + 0.17 KB key/vector) = 5.17 KB/average vector processed
Tier 1 query processing cost = 100 thousand vectors _ 5.17 KB/average vector _ $0.004/TB _ 1 million queries = $1.93
Tier 2 query processing cost = 150 thousand vectors _ 5.17 KB/average vector _ $0.002/TB _ 1 million queries = $1.44
Query API cost = 1 million queries _ $2.5/million queries = $2.50
Total query cost for 1M queries across all vector indexes = $5.87 per month

Total cost = $11.38 per month

Pricing example 2:
Your customers have expanded their underlying indexes supporting their RAG workflow, resulting in larger indexes of 10 million vectors each, with the same 6.17 KB per vector. In total, you have 40 vector indexes and 400 million vectors stored in S3 Vectors. You have the same PUT rate of 16.7% of data per month; however, your query volume has also increased to 10 million queries per month. This example uses pricing for the US East (N. Virginia) AWS Region.

S3 Vectors storage charge
((4 bytes _ 1024 dimensions) vector data/vector + 1 KB filterable metadata/vector + 1 KB non-filterable metadata/vector + 0.17 KB key/vector) = 6.17 KB logical storage per average vector
6.17 KB/average vector _ 10 million vectors* 40 indexes = 2,354 GB logical storage
Total monthly storage cost = 2,354 GB * $0.06/GB per month = $141.22

S3 Vectors PUT charge
Total monthly PUT cost = 1 full upload/6 months _ 2,354 GB total storage _ $0.20/GB = $78.46

S3 Vectors Query charge
((4 bytes _ 1024 dimensions) vector data/vector + 1 KB filterable metadata/vector + 0.17 KB key/vector) = 5.17 KB/average vector processed
Tier 1 query processing cost = 100 thousand vectors _ 5.17 KB/average vector _ $0.004/TB _ 10 million queries = $19.26
Tier 2 query processing cost = 9.9 million vectors _ 5.17 KB/average vector _ $0.002/TB _ 10 million queries = $953.36
Query API cost = 10 million queries _ $2.5/million queries = $25.00
Total query cost = $997.62 per month

Total cost = $1,217.29 per month

Data Transfer
You pay for all bandwidth into and out of Amazon S3, except for the following:

Data transferred out to the internet for the first 100GB per month, aggregated across all AWS Services and Regions (except China and GovCloud)
Data transferred in from the internet.
Data transferred between S3 buckets in the same AWS Region.
Data transferred from an Amazon S3 bucket to any AWS service(s) within the same AWS Region as the S3 bucket (including to a different account in the same AWS Region).
Data transferred out to Amazon CloudFront (CloudFront).
EU customers may request reduced data transfer rates for eligible use cases under the European Data Act. Please contact AWS Customer Support for more information.
The pricing below is based on data transferred "in" and "out" of Amazon S3 (over the public internet)***. Learn more about AWS Direct Connect pricing.

For Data Transfers exceeding 500 TB/Month, please contact us.
Region:

Middle East (UAE)
Price
Data Transfer IN To Amazon S3 From Internet
All data transfer in $0.00 per GB
Data Transfer OUT From Amazon S3 To Internet

AWS customers receive 100GB of data transfer out to the internet free each month, aggregated across all AWS Services and Regions (except China and GovCloud). The 100 GB free tier for data transfer out to the internet is global and does not apply separately or individually to AWS Regions.

First 10 TB / Month $0.11 per GB
Next 40 TB / Month $0.085 per GB
Next 100 TB / Month $0.077 per GB
Greater than 150 TB / Month $0.055 per GB
Data Transfer OUT From Amazon S3 To
Amazon CloudFront $0.00 per GB
AWS GovCloud (US-West) $0.085 per GB
AWS GovCloud (US-East) $0.085 per GB
Africa (Cape Town) $0.085 per GB
Asia Pacific (Hong Kong) $0.085 per GB
Asia Pacific (Hyderabad) $0.085 per GB
Asia Pacific (Jakarta) $0.085 per GB
Asia Pacific (Malaysia) $0.085 per GB
Asia Pacific (Melbourne) $0.085 per GB
Asia Pacific (Mumbai) $0.085 per GB
Asia Pacific (New Zealand) $0.085 per GB
Asia Pacific (Osaka) $0.085 per GB
Asia Pacific (Seoul) $0.085 per GB
Asia Pacific (Singapore) $0.085 per GB
Asia Pacific (Sydney) $0.085 per GB
Asia Pacific (Taipei) $0.085 per GB
Asia Pacific (Thailand) $0.1105 per GB
Asia Pacific (Tokyo) $0.085 per GB
Canada (Central) $0.085 per GB
Canada West (Calgary) $0.085 per GB
Europe (Frankfurt) $0.085 per GB
Europe (Ireland) $0.085 per GB
Europe (London) $0.085 per GB
Europe (Milan) $0.085 per GB
Europe (Paris) $0.085 per GB
Europe (Spain) $0.085 per GB
Europe (Stockholm) $0.085 per GB
Europe (Zurich) $0.085 per GB
Israel (Tel Aviv) $0.085 per GB
Mexico (Central) $0.085 per GB
Middle East (Bahrain) $0.085 per GB
South America (Sao Paulo) $0.085 per GB
US East (N. Virginia) $0.085 per GB
US East (Ohio) $0.085 per GB
US West (Los Angeles) $0.085 per GB
US West (N. California) $0.085 per GB
US West (Oregon) $0.085 per GB
S3 Multi-Region Access Points pricing
Amazon S3 Multi-Region Access Points accelerate performance by up to 60% when accessing data sets that are replicated across multiple AWS Regions. Based on AWS Global Accelerator, S3 Multi-Region Access Points consider factors like network congestion and the location of the requesting application to dynamically route your requests over the AWS network to the lowest latency copy of your data. This automatic routing allows you to take advantage of the global infrastructure of AWS while maintaining a simple application architecture.
S3 Multi-Region Access Points data routing pricing
When you use an S3 Multi-Region Access Point to route requests within AWS, you pay a data routing cost for each gigabyte (GB) processed, as well as standard charges for S3 requests, storage, data transfer, and replication.

S3 Multi-Region Access Points data routing Pricing
Data routing cost $0.0033 per GB
S3 Multi-Region Access Points internet acceleration pricing
If your application runs outside of AWS and accesses S3 over the internet, S3 Multi-Region Access Points increase performance by automatically routing your requests through an AWS edge location, over the global private AWS network, to the closest copy of your data based on access latency. When you accelerate requests made over the internet, you pay the data routing cost outlined above and an internet acceleration cost.

S3 Multi-Region Access Points internet acceleration pricing varies based on whether the source client is in the same or in a different location as the destination AWS Region, and is in addition to standard S3 data transfer pricing.

For S3 Multi-Region Access Points availability in AWS Regions, please visit the user guide.

Internet acceleration pricing between locations
Internet acceleration WITHIN North America
Pricing
Data transfer IN to Amazon S3 from the internet $0.0025 per GB
Data transfer OUT from Amazon S3 to the internet $0.0050 per GB
Internet acceleration BETWEEN North America AND any other location
Data transfer IN to Amazon S3 from the internet $0.0500 per GB
Data transfer OUT from Amazon S3 to the internet $0.0500 per GB
Internet acceleration WITHIN Europe
Pricing
Data transfer IN to Amazon S3 from the internet $0.0025 per GB
Data transfer OUT from Amazon S3 to the internet $0.0050 per GB
Internet acceleration BETWEEN Europe AND any other location
Data transfer IN to Amazon S3 from the internet $0.0500 per GB
Data transfer OUT from Amazon S3 to the internet $0.0500 per GB
Internet acceleration WITHIN Asia Pacific
Pricing
Data transfer IN to Amazon S3 from the internet $0.0100 per GB
Data transfer OUT from Amazon S3 to the internet $0.0150 per GB
Internet acceleration BETWEEN Asia Pacific AND any other location
Data transfer IN to Amazon S3 from the internet $0.0600 per GB
Data transfer OUT from Amazon S3 to the internet $0.0600 per GB
Internet acceleration WITHIN South America
Pricing
Data transfer IN to Amazon S3 from the internet $0.0250 per GB
Data transfer OUT from Amazon S3 to the internet $0.0400 per GB
Internet acceleration BETWEEN South America AND any other location
Data transfer IN to Amazon S3 from the internet $0.0600 per GB
Data transfer OUT from Amazon S3 to the internet $0.0600 per GB
S3 Multi-Region Access Points failover controls pricing
S3 Multi-Region Access Points failover controls let you shift S3 data access request traffic routed through an Amazon S3 Multi-Region Access Point within minutes to an alternate AWS Region to build highly available applications for business continuity. To use failover controls, you are charged for S3 API costs to view the current routing control status of each Region and submit any routing control changes for initiating a failover.
S3 Multi-Region Access Points pricing examples
Example 1: Using S3 Multi-Region Access Points within an AWS Region
You have an application in US East (N. Virginia), and an S3 Multi-Region Access Point that is configured to dynamically route requests to an S3 bucket in either US East (N. Virginia) or US West (Oregon). Your application sends a 10 GB of data through an S3 Multi-Region Access Point. In this case, the lowest latency bucket to your application will be the bucket in US East (N. Virginia), so your requests will remain within that region. We calculate your cost as follows.

S3 Multi-Region Access Point data routing cost: The S3 Multi-Region Access Point data routing cost is $0.0033 per GB. In this example, 10 GB of data was routed by your S3 Multi-Region Access Point.

Total S3 Multi-Region Access Point data routing cost = $0.0033 \* 10 GB = $0.033

Total charges:

S3 Multi-Region Access Point data routing = $0.033

Total = $0.033

Example 2: Using S3 Multi-Region Access Points across AWS Regions
You have an application in US East (N. Virginia) and a S3 Multi-Region Access Point that is configured to dynamically route requests to an S3 bucket in either US East (Ohio) or US West (Oregon). Your application sends a 10 GB of data through an S3 Multi-Region Access Point. In this case, the lowest latency bucket to your application will be the bucket in US East (Ohio).

Since your application is in US East (N. Virginia) and your lowest latency bucket is in US East (Ohio), your requests will automatically traverse the private AWS network from one AWS Region to another AWS Region. As a result, you will incur standard AWS cross-region data transfer charges, in addition to a S3 Multi-Region Access Point data routing cost. We calculate your cost as follows.

S3 Multi-Region Access Point data routing cost

The S3 Multi-Region Access Point data routing cost is $0.0033 per GB. In this example, 10 GB of data was routed by your S3 Multi-Region Access Point.

Total S3 Multi-Region Access Point data routing cost = $0.0033 \* 10 GB = $0.033

Data transfer charges from Amazon EC2 in US East (N. Virginia) to Amazon S3 in US East (Ohio)

The data transfer charge from US East (N. Virginia) to US East (Ohio) is $0.01 per GB. In this example, 10 GB of data went through your S3 Multi-Region Access Point and was routed over the private AWS network from your application in US East (N. Virginia), to an S3 bucket in US East (Ohio).

Total S3 data transfer cost = $0.01 \* 10 GB = $0.10

Total Charges:

S3 Multi-Region Access Point data routing cost = $0.033

S3 data transfer charges - US East (N. Virginia) to US East (Ohio) = $0.10

Total = $0.133

Example 3: Using S3 Multi-Region Access Points over the internet
You have an application that supports customers in North America, Europe, and Asia. These customers send and receive data over the internet to and from an S3 bucket in either US East (N. Virginia), or Europe (Ireland). You created an S3 Multi-Region Access Point to accelerate your application by routing customer requests to the S3 bucket closest to them.

One of your customers sends 10 GB over the internet into S3 from a client in North America. This request is automatically routed to the bucket in US East (N. Virginia). A second customer downloads 10 GB of data over the internet from S3 to a client in Europe. This request is automatically routed to the bucket in Europe (Ireland). A third customer downloads 10 GB of data over the internet from S3 to a client in Asia. This request is automatically routed to the bucket in Europe (Ireland) as well.

Since two of your customers are transferring data out of S3 over the internet you will incur standard AWS data transfer out charges, in addition to a S3 Multi-Region Access Point data routing cost. We calculate your cost as follows.

S3 Multi-Region Access Point data routing cost

The S3 Multi-Region Access Point data routing cost is $0.0033 per GB. In this example, 30 GB of data was routed by your S3 Multi-Region Access Point to your buckets.

Total S3 Multi-Region Access Point data routing cost = $0.0033 \* 30 GB = $0.099

S3 Multi-Region Access Point internet acceleration cost:

The 10 GB uploaded from a client in North America, through an S3 Multi-Region Access Point, to a bucket in North America will incur a charge of $0.0025 per GB.

The 10 GB downloaded from a bucket in Europe, through an S3 Multi-Region Access Point, to a client in Europe will incur a charge of $0.005 per GB.

The 10 GB downloaded from a bucket in Europe, through an S3 Multi-Region Access Point, to a client in Asia will incur a charge of $0.05 per GB.

Total S3 Multi-Region Access Point internet acceleration cost = $0.0025 _ 10 GB + $0.005 _ 10 GB + $0.05 \* 10 GB = $0.575

S3 data transfer OUT from Amazon S3 in Europe (Ireland) to internet

The Data Transfer out charge from Amazon S3 in Europe (Ireland) to internet is $0.09 per GB. In this example, 20 GB were transferred out; one to a client in Europe, and one to a client in Asia.

Total data transfer cost = $0.09 \* 20 GB = $1.80

Total Charges:

S3 Multi-Region Access Point data routing cost = $0.099

S3 Multi-Region Access Point internet acceleration cost = $0.575

S3 data transfer charges - Europe (Ireland) data transfer OUT to internet = $1.80

Total = $2.474

Example 4: Using S3 Multi-Region Access Points with cross-account buckets across AWS Regions
You have an application in US East (N. Virginia) and a S3 Multi-Region Access Point in AWS account 1 that is configured to dynamically route requests. You can route to an S3 bucket belonging to a separate AWS account 2 in US East (Ohio) or to an S3 bucket belonging to a separate AWS account 3 in US West (Oregon). Your application sends a 10 GB of data through an S3 Multi-Region Access Point. In this case, the lowest latency bucket to your application will be the bucket in US East (Ohio).

Since your application is in US East (N. Virginia) and your lowest latency bucket is in US East (Ohio), your requests will automatically traverse the private AWS network from one AWS Region to another AWS Region. As a result, you will incur standard AWS cross-Region data transfer charges, in addition to a S3 Multi-Region Access Point data routing cost. We calculate your cost as follows.

As an account owner that owns only the Multi-Region Access Point, but not the US East (Ohio) bucket, you incur the following charges:

S3 Multi-Region Access Point data routing cost:

The S3 Multi-Region Access Point data routing cost is $0.0033 per GB. In this example, 10 GB of data was routed by your S3 Multi-Region Access Point.

Total S3 Multi-Region Access Point data routing cost = $0.0033 \* 10 GB = $0.033

Total Charges:

S3 Multi-Region Access Point data routing cost = $0.033

The owner of the bucket in US East (Ohio) will only incur the following charges:

The data transfer charge from US East (N. Virginia) to US East (Ohio) is $0.01 per GB. In this example, 10 GB of data went through your S3 Multi-Region Access Point and was routed over the private AWS network from your application in US East (N. Virginia) to an S3 bucket in US East (Ohio).

Total S3 data transfer cost = $0.01 \* 10 GB = $0.10

Total Charges:

S3 data transfer cost = $0.10

The owner of the bucket in US West (Oregon) will not incur any data transfer costs or request costs as the current request is not being routed to their bucket.

Note:

The behavior for each request to a Multi-Region Access Point is determined by the respective bucket where the request lands. As a bucket owner, if your bucket is configured to be a Requester Pays bucket, the requester pays all of the cost associated to the endpoint usage, including the cost for requests and data transfer cost associated to both the bucket and the Multi-Region Access Point. Typically, you want to configure your buckets as requester pays buckets if you wish to share data but not incur charges associated with others accessing the data. To learn more, please visit S3 Requester Pays.

S3 Transfer Acceleration pricing
S3 Transfer Acceleration accelerates internet transfers between the client and a single S3 bucket. Pricing is based on the AWS edge location used to accelerate your transfer. S3 Transfer Acceleration pricing is in addition to Data Transfer pricing.

Each time you use S3 Transfer Acceleration to upload an object, we will check whether the service is likely to be faster than a regular Amazon S3 transfer. If we determine that it is not likely to be faster than a regular Amazon S3 transfer of the same object to the same destination AWS Region, we will not charge for that use of S3 Transfer Acceleration for that transfer, and may bypass the S3 Transfer Acceleration system for that upload.

Check your performance with the Amazon S3 Transfer Acceleration speed comparison tool.

Data Transfer IN to Amazon S3 from the Internet:
Accelerated by AWS Edge Locations in the United States, Europe, and Japan $0.04 per GB
Accelerated by all other AWS Edge Locations $0.08 per GB
Data Transfer OUT from Amazon S3 to the Internet:
Accelerated by any AWS Edge Location $0.04 per GB
Data Transfer between Amazon S3 and another AWS region:
Accelerated by any AWS Edge Location $0.04 per GB
For Data Transfers exceeding 500 TB/Month, please contact us.

Storage and bandwidth size includes all file overhead.

Rate tiers take into account your aggregate usage for Data Transfer Out to the Internet across all AWS services.

*** Data Transfer Out may be different from the data received by your application in case the connection is prematurely terminated by you, for example, if you make a request for a 10 GB object and terminate the connection after receiving the first 2 GB of data. Amazon S3 attempts to stop the streaming of data, but it does not happen instantaneously. In this example, the Data Transfer Out may be 3 GB (1 GB more than 2 GB you received). As a result, you will be billed for 3 GB of Data Transfer Out.

S3 Pricing Details
Except as otherwise noted, our prices are exclusive of applicable taxes and duties, including VAT and applicable sales tax. For customers with a Japanese billing address, use of AWS is subject to Japanese Consumption Tax. To learn more, visit our consumption tax FAQs.

Amazon S3 storage usage is calculated in binary gigabytes (GB), where 1 GB is 230 bytes. This unit of measurement is also known as a gibibyte (GiB), defined by the International Electrotechnical Commission (IEC). Similarly, 1 TB is 240 bytes, i.e. 1024 GBs.

For Reduced Redundancy Storage pricing please visit the S3 Reduced Redundancy detail page.

For S3 pricing examples, go to the S3 billing FAQs or use the AWS Pricing Calculator.

AWS Free Tier
As of July 15, 2025, new AWS customers will receive up to $200 in AWS Free Tier credits, which can be applied towards eligible AWS services, including Amazon S3. At account sign-up, you can choose between a free plan and a paid plan. The free plan will be available for 6 months after account creation. If you upgrade to a paid plan, any remaining Free Tier credit balance will automatically apply to your AWS bills. All Free Tier credits must be used within 12 months of your account creation date. To learn more about the AWS Free Tier program, refer to AWS Free Tier website and AWS Free Tier documentation.

S3 Encryption
Region:

Middle East (UAE)
Server-side encryption with Amazon S3 managed keys (SSE-S3) Free
Server-side encryption with customer provided keys (SSE-C) Free
Server-side encryption with keys stored in AWS Key Management Service (SSE-KMS) Free*
Dual-layer server-side encryption with keys stored in AWS Key Management Service (DSSE-KMS) $0.003 per gigabyte **
Amazon S3 automatically applies server-side encryption with Amazon S3 managed keys (SSE-S3) as a base layer of encryption to all new objects added to S3, at no additional cost and with no impact on performance. SSE-C also does not incur any additional S3 charges.

* For SSE-KMS, you pay AWS KMS charges to generate or retrieve the data key used for encryption and decryption. For pricing on AWS KMS, visit the AWS KMS pricing page. You can also optimize your SSE-KMS costs with Amazon S3 Bucket Keys.

** For DSSE-KMS, in addition to the charges for AWS KMS mentioned above, you pay an additional per gigabyte encryption fee for the second layer of encryption and decryption of data.

S3 bucket types
Amazon S3 supports four different bucket types: general purpose buckets, directory buckets, and table buckets, and vector buckets. S3 general purpose buckets are available in all AWS Regions. For Regional availability details, visit the S3 User Guide for directory buckets, table buckets, and vector buckets.

S3 general purpose buckets
Amazon S3 general purpose buckets are the original S3 bucket type, and a single general purpose bucket can contain objects stored across all storage classes except S3 Express One Zone.

First 2,000 general purpose buckets per account / Month Free
Over 2,000 general purpose buckets per account / Month $0.02 per additional general purpose bucket
S3 directory buckets
Amazon S3 directory buckets only allow objects stored in the S3 Express One Zone storage class, which provides faster data processing within a single Availability Zone.

Directory buckets Free
S3 table buckets
Amazon S3 table buckets are purpose-built for storing tabular data. They deliver up to 3x faster query performance and up to 10x higher transactions per second, making them specifically optimized for analytics workloads.

Table buckets Free
S3 vector buckets
Amazon S3 vector buckets are purpose-built for storing and querying vectors. Within a vector bucket, you use dedicated vector APIs to write vector data and query it based on semantic meaning and similarity.

Vector buckets Free
S3 Access Grants
Amazon S3 Access Grants map identities in directories such as Active Directory, or AWS Identity and Access Management (IAM) Principals, to datasets in S3. This helps you manage data permissions at scale by automatically granting S3 access to end-users based on their corporate identity. Additionally, S3 Access Grants log end-user identity, as well as the application used to access S3 data, in AWS CloudTrail. This helps to provide a detailed audit history down to the end-user identity for all access to the data in your S3 buckets.

Region:

US East (N. Virginia)
S3 Access Grants is priced on a per-request basis. You are charged a flat rate for all Access Grants requests, such as GetDataAccess to obtain credentials. Delete-related requests, such as DeleteAccessGrant, are free.

S3 Access Grants Requests (per 1,000 requests) $0.03

You pay for the storage management features and analytics (Amazon S3 Metadata, Amazon S3 Inventory, Amazon S3 Storage Class Analysis, Amazon S3 Storage Lens, and Amazon S3 Object Tagging) that are enabled on your account's buckets. S3 storage management and analytics are priced per feature as detailed in the following table. For pricing on Amazon CloudWatch metrics, visit the Amazon CloudWatch pricing page. For pricing on S3 data events in AWS CloudTrail, visit the AWS CloudTrail pricing page.

## Storage management
S3 Metadata pricing
Amazon S3 Metadata delivers queryable object metadata in near real time to organize your data and accelerate data discovery. This helps you to curate, identify, and use your Amazon S3 data for business analytics, real-time inference applications, and more.

Region:

Middle East (UAE)
S3 Metadata journal tables $0.30 per million updates **
S3 Metadata live inventory tables $0.10 per million objects per month ***(one-time backfill fee applies)
** Updates include new object uploads, changes to object metadata, and object deletes for journal tables. Updates also include one-time backfill of all objects for live inventory tables. Additional charges for Amazon S3 Tables will apply.

*** Monthly fee applicable only for buckets with greater than 1 billion objects.

S3 Metadata pricing example:
You upload 1,000,000 new images every month in a general purpose S3 bucket with an existing 200,000,000 objects that have S3 Metadata journal and live inventory table configuration enabled. You want to determine the total price for enabling the live inventory table, to generate your latest list of objects and metadata, and enabling the journal table to track the changes into your bucket. This example uses the US West (Oregon) Region.

Your charges would be calculated as follows:

S3 Metadata journal table ($/million updates)
S3 Metadata price for journal tables is $0.30 per million updates
Since you are providing 1,000,000 updates, your charges would be:
S3 Metadata charge: 1,000,000 \* $0.30/1,000,000 = $0.30

S3 Metadata live inventory table ($/million updates) - one time backfill charge
S3 Metadata price for one-time backfill of existing objects is $0.30 per million updates
Since you have existing 200,000,000 objects, your charges would be:
S3 Metadata charge: 200,000,000 \* $0.30/1,000,000 = $60.00

S3 Metadata live inventory table ($/million objects) - monthly charge
S3 Metadata live inventory price is $0.10 per million objects per month for buckets with objects greater than 1 billion. For buckets with fewer than 1 billion objects, there is no monthly cost for keeping your live inventory table up to date.
Since your general purpose S3 bucket has fewer than 1 billion objects, there is no monthly cost for keeping your live inventory table up to date.

Total charges:
Total charges for S3 Metadata include your journal table charges, the one-time backfill cost, and the monthly fee for live inventory tables for buckets with more than 1 billion objects. In this example, your monthly charges are calculated as follows:

S3 Metadata charges for the first month: $0.30 + $60.00 + $0.00 = $60.30
S3 Metadata monthly charges, for the second month onwards: $0.30 + $0.00 + $0.00 = $0.30

Note that separate charges for table storage, maintenance, and requests will apply.

S3 Inventory & S3 Object Tagging pricing
Region:

Middle East (UAE)
S3 Inventory** $0.0028 per million objects listed
S3 Object Tagging $0.0065 per 10,000 tags per month
** The files produced by S3 Inventory exports are stored in your specified S3 bucket, and are subject to S3 Standard storage charges.

S3 Batch Operations pricing
Region:

Middle East (UAE)
Batch Operations - Jobs $0.25 per job
Batch Operations - Objects $1.00 per million objects processed
Batch Operations - Manifest (optional) $0.015 per 1 million objects in the source bucket
** You are charged for S3 Batch Operations jobs, objects, manifests, and requests in addition to any charges associated with the operation that S3 Batch Operations performs on your behalf, including data transfer, requests, and other charges.

When S3 Batch Operations generates a manifest, you are charged for an S3 Batch Operations manifest containing a list of objects for Batch Operations to operate on.

Compute checksum operation pricing
The compute checksum operation provides a new way to verify the content of stored datasets. You can efficiently verify billions of objects and automatically generate integrity reports to prove that your datasets remain intact over time using S3 Batch Operations.

Region:

Middle East (UAE)

Price
Data processed $0.004 per GB
Compute checksum operation pricing example
You have 1,000,000 high-resolution images stored in the S3 Standard storage class, each with an average size of 2 MB. You want to verify the integrity of these images before processing them. This example uses the US East (N. Virginia) Region.
Your charges would be calculated as follows:

Amazon S3 Batch Operations charges
Job charge: S3 Batch Operations jobs cost $0.25 per job
Object charge: S3 Batch Operations charges $1 per million objects processed
Since you are processing 1,000,000 objects, your charges would be:
S3 Batch Operations Job charge: 1 job _ $0.25 = $0.25
S3 Batch Operations Object charge: 1,000,000 objects _ ($1 per million objects / 1,000,000) = $1.00
Total S3 Batch Operations charges: $1.25

Compute checksum operation charges
Compute checksum operation cost: $0.004 per GB of data processed
For 1,000,000 objects at 2 MB each, the total data processed is:
Total data processed: 1,000,000 objects _ 2 MB = 2,000,000 MB = 2,000 GB
Compute checksum operation charge: 2,000 GB _ $0.004 per GB = $8.00

Total charges:
Amazon S3 Batch Operations charges: $1.25
Compute checksum operation charges: $8.00
Total = $9.25

Storage insights
S3 Storage Lens pricing
Region:

Middle East (UAE)
S3 Storage Lens free metrics $0.00
S3 Storage Lens advanced metrics and recommendations*
Up to 25B objects monitored $0.20 per million objects monitored per month
Greater than 25B to 100B objects monitored $0.16 per million objects monitored per month
Greater than 100B objects monitored $0.12 per million objects monitored per month
* For S3 Storage Lens advanced metrics and recommendations, you will be charged object monitoring charges for each Storage Lens dashboard used. The Storage Lens advanced metrics and recommendations pricing includes 15-months data retention, 35 additional metrics across 4 categories (activity, advanced cost optimization, advanced data protection, and detailed status code metrics), prefix-level aggregation, and CloudWatch metrics support.

S3 Storage Class Analysis pricing
Region:

Middle East (UAE)
S3 Analytics Storage Class Analysis** $0.10 per million objects monitored per month
** The files produced by S3 Storage Class Analysis exports are stored in your specified S3 bucket, and are subject to S3 Standard storage charges.

Except as otherwise noted, our prices are exclusive of applicable taxes and duties, including VAT and applicable sales tax. For customers with a Japanese billing address, use of AWS is subject to Japanese Consumption Tax. To learn more, visit our consumption tax FAQs

Amazon S3 storage usage is calculated in binary gigabytes (GB), where 1 GB is 230 bytes. This unit of measurement is also known as a gibibyte (GiB), defined by the International Electrotechnical Commission (IEC). Similarly, 1 TB is 240 bytes, i.e. 1024 GBs.

For S3 pricing examples, go to the S3 billing FAQs or use the AWS Pricing Calculator.

S3 Cross-Region Replication, Same-Region Replication, and Replication Time Control
For Cross-Region Replication (CRR) and Same-Region Replication (SRR), you pay the S3 charges for storage in the selected destination S3 storage classes, for the primary copy, for replication PUT requests, and for applicable infrequent access storage retrieval charges. For CRR, you also pay for inter-region Data Transfer OUT from S3 to each destination region. When you use S3 Replication Time Control, you also pay a Replication Time Control Data Transfer charge and S3 Replication Metrics charges that are billed at the same rate as Amazon CloudWatch custom metrics.

Storage and PUT request pricing for the replicated copy is based on the selected destination AWS Regions, while pricing for inter-region data transfers is based on the source AWS Region. For more details on replication pricing, read the pricing FAQs.

S3 Replication Time Control data transfer* $0.015 per GB
* Amazon S3 Replication Time Control Data Transfer pricing is the same in all AWS Regions. Replication Time Control is available in all commercial AWS Regions, including the AWS China (Beijing) Region and the AWS China (Ningxia) Region, but not in the AWS GovCloud (US) Regions.

S3 Batch Replication
While live replication like CRR and SRR automatically replicates newly uploaded objects as they are written to your bucket, S3 Batch Replication allows you to replicate existing objects. S3 Batch Replication is built using S3 Batch Operations to replicate objects as fully managed Batch Operations jobs. Similar to SRR and CRR, you pay the S3 charges for storage in the selected destination S3 storage classes, for the primary copy, for replication PUT requests, and for applicable infrequent access storage retrieval charges. When replicating across AWS Regions, you also pay for inter-Region Data Transfer OUT from S3 to each destination Region. If an object already exists in the destination bucket, we will check if the destination object is in sync with the source object. If the metadata is not in sync and needs to be replicated, you will incur the replication PUT request charge but not the inter-Region Data Transfer OUT charge. If the metadata is in sync, Batch Replication will do nothing and you incur no charge. For more details on replication pricing, read the pricing FAQs.

In addition to these charges, you also pay the S3 Batch Operations charges for Batch Replication jobs. See the following table for details.

Finally, when replicating existing objects, you need to indicate what objects to replicate. You can do this by providing a list of objects to S3 yourself, or use an AWS-generated manifest where you can specify filters such as object creation date and replication status. If you use the manifest, there is a charge based on the number of objects in the source bucket.

Region:

Middle East (UAE)
Batch Operations - Jobs $0.25 per job
Batch Operations - Objects $1.00 per million objects processed
Batch Operations - Manifest (optional) $0.015 per 1 million objects in the source bucket
Note: For S3 Tables replication pricing, refer to the Tables tab.

S3 Object Lambda pricing
With S3 Object Lambda, you can add your own code to S3 GET, HEAD, and LIST requests to modify and process data as it is returned to an application. You can use custom code to modify the data returned by standard S3 GET requests to filter rows, dynamically resize images, redact confidential data, and much more. Additionally, you can use S3 Object Lambda to modify the output of S3 LIST requests to create a custom view of objects in a bucket and S3 HEAD requests to modify object metadata like object name and size. Powered by AWS Lambda functions, your code runs on infrastructure that is fully managed by AWS, eliminating the need to create and store derivative copies of your data or to run expensive proxies, all with no changes required to applications.

When you use S3 Object Lambda, your S3 GET, HEAD, and LIST requests invoke an AWS Lambda function that you define. This function will process your data and return a processed object back to your application. In the US East (N. Virginia) Region, you pay $0.0000167 per GB-second for the duration of your AWS Lambda function, and $0.20 per 1M AWS Lambda requests. You pay for requests based on the request type, which vary by storage class. For example, if the data is stored in S3 Standard, you pay $0.0004 per 1,000 requests for all S3 GET and HEAD requests, or $0.005 per 1,000 requests for all LIST requests. You also pay a $0.005 per-GB charge for the data S3 Object Lambda returns to your application. S3 request and Lambda prices depend on the AWS Region, and the duration and memory allocated to your Lambda function. All regional prices are on the AWS Lambda and Amazon S3 pricing pages.

Region:

Middle East (UAE)
Price
Data returned $0.005 per GB
S3 Object Lambda pricing example
You have 1,000,000 objects that contain historical log data, generated by many applications. Confidential log entries make up 50% of the data. These logs are stored in the S3 Standard storage class, and the average object size is 1000 KB. You are building an application that analyzes this data, but should not have access to confidential log entries.

You can use S3 Object Lambda to filter out confidential log entries. This filtering occurs as your logs are retrieved from S3 with standard S3 GET requests. The Lambda function to filter your data is allocated 512MB of memory, has a 1 second runtime, and returns filtered objects that are 500 KB in size (on average) back to your application. This example assumes one retrieval per month for each object. This example uses the US East (N. Virginia) Region.

Your charges would be calculated as follows:

Amazon S3 GET request charge

S3 GET requests from the S3 Standard storage class cost $0.0004 per 1,000 requests.

S3 GET Request cost: 1,000,000 requests \* $0.0004/1K requests = $0.40

AWS Lambda Charges

The Lambda compute cost is $0.0000167 per GB-second. GB-seconds are calculated based on the number of seconds that a Lambda function runs, adjusted by the amount of memory allocated to it.

The Lambda request price is $0.20 per 1 million requests.

Lambda compute charge: 1,000,000 requests _ 1 second _ 0.5 GB (512 MB/1024) memory allocated \* $0.0000167 per GB-second = $8.35

Lambda request charge = 1,000,000 requests \* $0.20 per 1 million requests = $0.20

Total Lambda cost = $8.35 + $0.20 = $8.55

S3 Object Lambda Charge
After the Lambda function filters the object, 500 KB is returned to the application at a cost of $0.005/GB of data returned.

Data Return Charge: 1,000,000 _ 500 KB _ $0.005/GB = $2.50

Total Charges:

Amazon S3 GET request charges = $0.40

AWS Lambda charges = $8.55

Amazon S3 Object Lambda charges = $2.50

Total = $11.45

S3 Select & S3 Glacier Select pricing
Region:

Middle East (UAE)
Data scanned (price per GB) Data returned (price per GB)
S3 Standard $0.00225 $0.0008
S3 Intelligent - Tiering $0.00225 $0.0008
S3 Standard - Infrequent Access $0.00225 $0.01
S3 Express One Zone n/a n/a
S3 Glacier Instant Retrieval $0.00225 $0.03
S3 Glacier Flexible Retrieval See below See below
S3 Glacier Deep Archive n/a n/a
S3 One Zone - Infrequent Access $0.00225 $0.01
