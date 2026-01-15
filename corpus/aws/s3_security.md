# Amazon S3 Security and Access Management
Service: S3
Doc: Security and Access Management

Unmatched security, compliance, and audit capabilities

## Overview
Store your data in Amazon S3 and secure it from unauthorized access with encryption features and access management tools. S3 encrypts all object uploads to all buckets. S3 is the only object storage service that allows you to block public access to all of your objects at the bucket or the account level with S3 Block Public Access. S3 maintains compliance programs, such as PCI-DSS, HIPAA/HITECH, FedRAMP, EU Data Protection Directive, and FISMA, to help you meet regulatory requirements. AWS also supports numerous auditing capabilities to monitor access requests to your S3 resources.

S3 Block Public Access
With a few clicks in the S3 management console or AWS Organizations console, you can apply S3 Block Public Access to every bucket in your account-both existing and any new buckets created in the future-and make sure that there is no public access to any object. For organizations with multiple AWS accounts, you can centrally manage these settings across all member accounts using AWS Organizations Policies. All new buckets have Block Public Access enabled by default. To restrict access to all existing buckets in your account, you can enable Block Public Access at the account level. If you manage multiple AWS accounts, you can enable Block Public Access at the organization level using AWS Organizations Policies to centrally control settings across all member accounts. S3 Block Public Access settings override S3 permissions that allow public access, making it easy for the account administrator or organization administrator to set up a centralized control to prevent variation in security configuration regardless of how an object is added or a bucket is created.

S3 Object Lock
Amazon S3 Object Lock blocks object version deletion during a customer-defined retention period so that you can enforce retention policies as an added layer of data protection or for regulatory compliance. You can migrate workloads from existing write-once-read-many (WORM) systems into Amazon S3, and configure S3 Object Lock at the object- and bucket-levels to prevent object version deletions prior to pre-defined Retain Until Dates or Legal Hold Dates.

S3 Object Ownership
Amazon S3 Object Ownership disables Access Control Lists (ACLs), changing ownership for all objects to the bucket owner and simplifying access management for data stored in S3. When you configure the S3 Object Ownership Bucket owner enforced setting, ACLs will no longer affect permissions for your bucket and the objects in it. All access control will be defined using resource-based policies, user policies, or some combination of these. ACLs are automatically disabled for new buckets. You can use S3 Inventory to review ACLs usage in your buckets before enabling S3 Object Ownership when migrating to IAM-based buckets policies. For more information, see Controlling Object Ownership.

Identity and Access Management
By default, all Amazon S3 resources-buckets, objects, and related subresources-are private: only the resource owner, an AWS account that created it, can access the resource. Amazon S3 offers access policy options broadly categorized as resource-based policies and user policies. You may choose to use resource-based policies, user policies, or some combination of these to manage permissions to your Amazon S3 resources. By default, an S3 object is owned by the account that created the object, including when this account is different than the bucket owner. You can use S3 Object Ownership to disable Access Control Lists and change this behavior. If you do, each object in a bucket is owned by the bucket owner. For more information, see Identity and access management in Amazon S3.

More features

Amazon Macie
Discover and protect sensitive data at scale in Amazon S3 with Amazon Macie. Macie automatically provides you with a full inventory of your S3 buckets by scanning buckets to identify and categorize the data. You receive actionable security findings enumerating any data that fits these sensitive data types, including personal identifiable information (PII) (e.g. customer names and credit cards numbers), and categories defined by privacy regulations, such as GDPR and HIPAA. Macie also automatically and continually evaluates bucket-level preventative controls for any buckets that are unencrypted, publicly accessible, or shared with accounts outside of your organization, allowing you to quickly address unintended settings on buckets.

Encryption
Amazon S3 automatically encrypts all object uploads to all buckets. For object uploads, Amazon S3 supports server-side encryption with four key management options: SSE-S3 (the base level of encryption), SSE-KMS, DSSE-KMS, and SSE-C, as well as client-side encryption. Amazon S3 offers flexible security features to block unauthorized users from accessing your data. Use VPC endpoints to connect to S3 resources from your Amazon Virtual Private Cloud (Amazon VPC). Use S3 Inventory to check the encryption status of your S3 objects (see storage management for more information on S3 Inventory).

AWS Trusted Advisor
Trusted Advisor inspects your AWS environment and then makes recommendations when opportunities exist to help close security gaps.

Trusted Advisor has the following Amazon S3-related checks: logging configuration of Amazon S3 buckets, security checks for Amazon S3 buckets that have open access permissions, and fault tolerance checks for Amazon S3 buckets that don't have versioning enabled, or have versioning suspended.

AWS PrivateLink for S3
Access Amazon S3 directly as a private endpoint within your secure, virtual network with AWS PrivateLink for S3. Simplify your network architecture by connecting to S3 from on-premises or in the cloud using private IP addresses from your Virtual Private Cloud (VPC). You no longer need to use public IPs, configure firewall rules, or configure an internet gateway to access S3 from on-premises.

Verify data integrity
Choose from four supported checksum algorithms (SHA-1, SHA-256, CRC32, or CRC32C) to check data integrity on your upload and download requests. Automatically calculate and verify checksums as you store or retrieve data from Amazon S3, and access the checksum information at any time using the GetObjectAttributes S3 API or an S3 Inventory report.
