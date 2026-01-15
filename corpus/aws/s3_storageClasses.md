# Amazon S3 Storage Classes
Service: S3
Doc: Storage Classes

## Amazon S3 Intelligent-Tiering storage class
Automates storage cost savings by moving data when access patterns change

## Overview
Amazon S3 Intelligent-Tiering is the only cloud storage class that delivers automatic storage cost savings when data access patterns change, without performance impact or operational overhead. The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering monitors access patterns and automatically moves objects that have not been accessed to lower-cost access tiers. Since the launch of S3 Intelligent-Tiering in 2018, customers have saved more than $6 billion in storage costs by using S3 Intelligent-Tiering as compared to Amazon S3 Standard.

S3 Intelligent-Tiering is the ideal storage class for data with unknown, changing, or unpredictable access patterns, independent of object size or retention period. You can use S3 Intelligent-Tiering as the default storage class for virtually any workload, especially data lakes, data analytics, new applications, and user-generated content.

## Benefits

Automatic savings
Automatic savings by optimizing storage costs based on access patterns

First and only
First and only cloud storage that automatically optimizes costs

99.999999999%
11 9s of durability

Lowest cost
Lowest cost storage in the cloud with opt-in Deep Archive access tier

Amazon S3 Intelligent-Tiering
The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering monitors access patterns and automatically moves objects that have not been accessed to lower-cost access tiers. S3 Intelligent-Tiering delivers automatic storage cost savings in three low-latency and high-throughput access tiers. For data that can be accessed asynchronously, you can choose to activate automatic archiving capabilities within the S3 Intelligent-Tiering storage class. There are no retrieval charges in S3 Intelligent-Tiering. If an object in the Infrequent or Archive Instant Access tier is accessed later, it's automatically moved back to the Frequent Access tier. No additional tiering charges apply when objects are moved between access tiers within the S3 Intelligent-Tiering storage class.

More on S3 Intelligent-Tiering
Frequent, Infrequent, and Archive Instant Access tiers have the same low-latency and high-throughput performance of S3 Standard
The Infrequent Access tier saves up to 40% on storage costs
The Archive Instant Access tier saves up to 68% on storage costs
Opt-in asynchronous archive capabilities for objects that become rarely accessed
Archive Access and Deep Archive Access tiers have the sameperformance as S3 Glacier Flexible Retrieval and S3 Glacier Deep Archive and save up to 95% for rarely accessed objects
Designed for durability of 99.999999999% of objects across multiple Availability Zones and for 99.9% availability over a given year
No operational overhead, no lifecycle charges, no retrieval charges, and no minimum storage duration

How it works - S3 Intelligent-Tiering

Automatic access tiers

The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. S3 Intelligent-Tiering automatically stores objects in three access tiers: one tier optimized for frequent access, a lower-cost tier optimized for infrequent access, and a very-low-cost tier optimized for rarely accessed data. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering moves objects that have not been accessed for 30 consecutive days to the Infrequent Access tier for savings of 40%; and after 90 days of no access, they're moved to the Archive Instant Access tier with savings of 68%. If the objects are accessed later, S3 Intelligent-Tiering moves the objects back to the Frequent Access tier. To save even more on rarely accessed storage, view the additional diagrams to see the opt-in asynchronous Archive and Deep Archive Access tiers in S3 Intelligent-Tiering.

There are no retrieval charges in S3 Intelligent-Tiering. S3 Intelligent-Tiering has no minimum eligible object size, but objects smaller than 128 KB are not eligible for auto tiering. These smaller objects may be stored, but they'll always be charged at the Frequent Access tier rates and don't incur the monitoring and automation charge. See the Amazon S3 Pricing page for more information. To learn more, visit the S3 Intelligent-Tiering user guide.

Opt-in asynchronous Deep Archive Access tier

The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. S3 Intelligent-Tiering automatically stores objects in three access tiers: one tier optimized for frequent access, a lower-cost tier optimized for infrequent access, and a very-low-cost tier optimized for rarely accessed data. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering moves objects that have not been accessed for 30 consecutive days to the Infrequent Access tier for savings of 40%; and after 90 days of no access, they're moved to the Archive Instant Access tier with savings of 68%. To save more on data that doesn't require immediate retrieval, you can activate the optional asynchronous Deep Archive Access tier. When turned on, objects not accessed for 180 days are moved to the Deep Archive Access tier with up to 95% in storage cost savings. If the objects are accessed later, S3 Intelligent-Tiering moves the objects back to the Frequent Access tier. If the object you are retrieving is stored in the optional Deep Archive tier, before you can retrieve the object you must first restore a copy using RestoreObject. For information about restoring archived objects, see Restoring Archived Objects.

There are no retrieval charges in S3 Intelligent-Tiering. S3 Intelligent-Tiering has no minimum eligible object size, but objects smaller than 128 KB are not eligible for auto tiering. These smaller objects may be stored, but they'll always be charged at the Frequent Access tier rates and don't incur the monitoring and automation charge. See the Amazon S3 Pricing page for more information. To learn more, visit the S3 Intelligent-Tiering user guide.

Both opt-in asynchronous Archive Access tiers
The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. S3 Intelligent-Tiering automatically stores objects in three access tiers: one tier optimized for frequent access, a lower-cost tier optimized for infrequent access, and a very-low-cost tier optimized for rarely accessed data. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering moves objects that have not been accessed for 30 consecutive days to the Infrequent Access tier for savings of 40%; and after 90 days of no access, they're moved to the Archive Instant Access tier with savings of 68%. To save more on data that doesn't require immediate retrieval, you can activate the optional asynchronous Archive Access and Deep Archive Access tiers. When turned on, objects not accessed for 90 days are moved directly to the Archive Access Tier (bypassing the automatic Archive Instant Access tier) for savings of 71%, and the Archive Deep Archive Access tier after 180 days with up to 95% in storage cost savings. If the objects are accessed later, S3 Intelligent-Tiering moves the objects back to the Frequent Access tier. If the object you are retrieving is stored in the optional Archive Access or Deep Archive tiers, before you can retrieve the object you must first restore a copy using RestoreObject. For information about restoring archived objects, see Restoring Archived Objects.

There are no retrieval charges in S3 Intelligent-Tiering. S3 Intelligent-Tiering has no minimum eligible object size, but objects smaller than 128 KB are not eligible for auto tiering. These smaller objects may be stored, but they'll always be charged at the Frequent Access tier rates and don't incur the monitoring and automation charge. See the Amazon S3 Pricing page for more information. To learn more, visit the S3 Intelligent-Tiering user guide.

## Amazon S3 Express One Zone storage class
Fastest cloud object storage for performance-critical applications

## What is S3 Express One Zone?
Amazon S3 Express One Zone is a high-performance, single-Availability Zone storage class purpose-built to deliver consistent single-digit millisecond data access for your most frequently accessed data and latency-sensitive applications. S3 Express One Zone delivers data access speed up to 10x faster and request costs up to 80% lower than S3 Standard. While you have always been able to choose a specific AWS Region to store your S3 data, with S3 Express One Zone you can select a specific AWS Availability Zone within an AWS Region to store your data. You can choose to co-locate your storage and compute resources in the same Availability Zone to further optimize performance, which helps lower compute costs and run workloads faster. With S3 Express One Zone, data is stored in a different bucket type-an S3 directory bucket-which can support up to 2 million requests per second. Additionally, you can use S3 Express One Zone with AWS Partner solutions and other AWS services to accelerate your machine learning and analytics workloads. With S3 Express One Zone, storage automatically scales up or down based on your consumption and need, and you no longer need to manage multiple storage systems for low-latency workloads.

## Benefits

Accelerate performance-critical applications
Improve access times for applications by up to 10x compared to the Amazon S3 Standard storage class with consistent single-digit millisecond request latency to run performance-intensive workloads faster.

Lower total cost of ownership
With the fastest data access, more efficient use of compute resources, and lower API request costs, you can access your most frequently accessed datasets at a lower overall TCO.

Scale simply without provisioning
Elastically scale to process millions of requests per minute, without any pre-provisioning or modification of existing applications, and use familiar existing Amazon S3 APIs.

## How it works
Get started by creating an S3 directory bucket in the Availability Zone of your choosing. You can choose to co-locate your storage and Amazon Elastic Compute Cloud (EC2), Amazon Elastic Kubernetes Service (EKS), and Amazon Elastic Container Service (ECS) compute resources to further optimize performance. You can either upload new objects directly into S3 Express One Zone or copy data from other storage classes using the Import button - a fully managed and trackable method of copying existing objects from a general purpose bucket or prefix in the same AWS Region to a directory bucket. Use your directory buckets with artificial intelligence and machine learning (AI/ML) services and applications and open source frameworks such as PyTorch to accelerate performance-critical workloads and reduce overall total cost of ownership (TCO) through lower latency, quicker processing times and lower compute costs, and lower API request costs.

## Use cases

AI/ML

Machine learning and artificial intelligence training
Accelerate model training and development by significantly improving data access speeds to process model datasets more quickly.

Analytics

Interactive data analytics
Accelerate query speed to gain insights from analytics on petabytes of data through faster processing speed with high-throughput and the lowest latency storage in the cloud.

Streaming

Accelerate log and media-streaming applications with single-digit millisecond request latency and capabilities like appending data to existing objects.

HPC

High performance computing (HPC)
Complete compute-intensive HPC workloads quickly with fast, highly scalable storage that can be co-located with your compute resources.

Media
Media content workloads
Respond to ever-shorter visual effects (VFX), rendering, and transcoding timelines with storage that scales with your compute.
