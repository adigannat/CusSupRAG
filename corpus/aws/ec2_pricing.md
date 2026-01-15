# Amazon EC2 Pricing
Service: EC2
Doc: Pricing

Different ways of paying for Amazon EC2

On-Demand pricing
Request a quote
Purchase options
On-Demand Instances
On-Demand Instances offer pay-as-you-go compute capacity by the hour or second. No upfront payment or long-term commitment are required.

Savings Plan
Savings Plans can help you reduce your bill by up to 72% compared to On-Demand prices in exchange for a usage commitment.

Spot Instances
With Amazon EC2 Spot Instances, you can use spare Amazon EC2 capacity in the AWS Cloud. This capacity is available at a discount of up to 90% compared to On-Demand prices.

Capacity when/how you need it

On-Demand Capacity Reservations

Amazon EC2 Capacity Blocks for ML

Dedicated Hosts
On-Demand Capacity Reservations
With On-Demand Capacity Reservations, you can reserve compute capacity in a specific Availability Zone. You will have access to Amazon EC2 capacity when and for as long as you need it.

We recommend On-Demand Capacity Reservations for use cases like these:

Business-critical events

High-availability requirements

Disaster recovery

Learn about capacity reservation pricing

Amazon EC2 Capacity Blocks for ML
With Amazon EC2 Capacity Blocks for ML, you can reserve GPU instances in advance for your machine learning (ML) workloads.
We recommend EC2 Capacity Blocks for use cases like these:

Train and fine-tune ML models

Run experiments and build prototypes

Plan for spikes in demand for ML

Learn about EC2 Capacity Blocks pricing

Dedicated Hosts
A Dedicated Host is a physical Amazon EC2 server fully dedicated for your use. With Dedicated Hosts, you can use your existing server-bound software licenses. You can purchase them On-Demand (hourly) or as part of Savings Plans.
We recommend Dedicated Hosts for use cases like these:

Save on licensing costs

Run workloads on dedicated physical servers

Offload host maintenance to AWS and control your maintenance event schedules

Flexible usage with per-second billing
Per-second billing removes the cost of unused compute time from your bill. This particularly helps workloads that run over irregular time periods. Amazon EC2 usage is billed in one-second increments, with a minimum of 60 seconds. The same is true for provisioned storage for Amazon Elastic Block Store (Amazon EBS) volumes. Per-second billing applies to all purchase options. It's available across all Regions and Availability Zones for these instances:

Amazon Linux

Windows

Red Hat Enterprise Linux

Ubuntu

Ubuntu Pro

For details on related costs, see Amazon EC2 On-Demand Pricing.

Amazon EC2 On-Demand Pricing
Request a pricing quote
On-Demand Pricing
On-Demand Instances let you pay for compute capacity by the hour or second (minimum of 60 seconds) with no long-term commitments. This frees you from the costs and complexities of planning, purchasing, and maintaining hardware and transforms what are commonly large fixed costs into much smaller variable costs.

The pricing below includes the cost to run private and public AMIs on the specified operating system ("Windows Usage" prices apply to Windows Server 2003 R2, 2008, 2008 R2, 2012, 2012 R2, 2016, and 2019). Amazon also provides you with additional instances for Amazon EC2 running Microsoft Windows with SQL Server, Amazon EC2 running SUSE Linux Enterprise Server, and Amazon EC2 running Red Hat Enterprise Linux.

Notice: Red Hat has made an update to their cloud pricing model for Red Hat Enterprise Linux (RHEL). On July 1, 2024 pricing for EC2 RHEL changed to a per-vCPU-hour based pricing model. Learn about the new prices in the RHEL on AWS Pricing page.

Pricing is per instance-hour consumed for each instance, from the time an instance is launched until it is terminated or stopped. Each partial instance-hour consumed will be billed per-second for Linux, Windows, Windows with SQL Enterprise, Windows with SQL Standard, and Windows with SQL Web Instances, and as a full hour for all other OS types.

The vCPU number is the default and maximum number of vCPUs available for the specified EC2 instance type. You can specify a custom number of vCPUs when launching this instance type. Instance pricing will remain same as displayed above. For more details on valid vCPU counts and how to start using this feature, visit the Optimize CPUs documentation page.

Looking for T1, M1, C1, CC2, M2, CR1, CG1, I2, HS1, M3, C3, or R3 instances? See the Previous Generation Instances page.

Data Transfer
The pricing below is based on data transferred "in" to and "out" of Amazon EC2.

Region:

Middle East (UAE)
Pricing
Data Transfer IN To Amazon EC2 From Internet
All data transfer in $0.00 per GB
Data Transfer OUT From Amazon EC2 To Internet
AWS customers receive 100GB of data transfer out to the internet free each month, aggregated across all AWS Services and Regions (except China and GovCloud). The 100 GB free tier for data transfer out to the internet is global and does not apply separately or individually to AWS Regions.
First 10 TB / Month $0.11 per GB
Next 40 TB / Month $0.085 per GB
Next 100 TB / Month $0.077 per GB
Greater than 150 TB / Month $0.055 per GB
Data Transfer OUT From Amazon EC2 To
Amazon CloudFront $0.00 per GB
AWS European Sovereign Cloud (Germany) $0.085 per GB
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
Asia Pacific (KDDI) - Osaka $0.085 per GB
Asia Pacific (KDDI) - Tokyo $0.085 per GB
Asia Pacific (SKT) - Daejeon $0.085 per GB
Asia Pacific (SKT) - Seoul $0.085 per GB
Canada (BELL) - Toronto $0.085 per GB
Europe (British Telecom) - Manchester $0.085 per GB
Europe (Vodafone) - Berlin $0.085 per GB
Europe (Vodafone) - Dortmund $0.085 per GB
Europe (Vodafone) - London $0.085 per GB
Europe (Vodafone) - Manchester $0.085 per GB
Europe (Vodafone) - Munich $0.085 per GB
Morocco (Casablanca) $0.08 per GB
Senegal (Dakar) $0.08 per GB
US East (Lenexa) $0.085 per GB
US East (Verizon) - Atlanta $0.085 per GB
US East (Verizon) - Boston $0.085 per GB
US East (Verizon) - Charlotte $0.085 per GB
US East (Verizon) - Chicago $0.085 per GB
US East (Verizon) - Dallas $0.085 per GB
US East (Verizon) - Detroit $0.085 per GB
US East (Verizon) - Houston $0.085 per GB
US East (Verizon) - Miami $0.085 per GB
US East (Verizon) - Minneapolis $0.085 per GB
US East (Verizon) - Nashville $0.085 per GB
US East (Verizon) - New York $0.085 per GB
US East (Verizon) - Tampa $0.085 per GB
US East (Verizon) - Washington DC $0.085 per GB
US West (Verizon) - Denver $0.085 per GB
US West (Verizon) - Las Vegas $0.085 per GB
US West (Verizon) - Los Angeles $0.085 per GB
US West (Verizon) - Phoenix $0.085 per GB
US West (Verizon) - San Francisco Bay Area $0.085 per GB
US West (Verizon) - Seattle $0.085 per GB
If the Data Transfer per month is greater than 500 TB / month, please contact us.

Rate tiers take into account your aggregate usage for Data Transfer Out to the Internet across Amazon EC2, Amazon S3, Amazon Glacier, Amazon RDS, Amazon Redshift, Amazon SageMaker, Amazon SES, Amazon SimpleDB, Amazon SQS, Amazon SNS, Amazon DynamoDB, AWS Storage Gateway, AWS CloudShell, and Amazon CloudWatch Logs.

AWS customers receive 100 GB of free data transfer out to the internet free each month, aggregated across all AWS Services and Regions (except China and GovCloud).

EU customers may request reduced data transfer rates for eligible use cases under the European Data Act. Please contact AWS Customer Support for more information.

AWS also offers eligible customers free data transfer out to the internet when they move all of their data off of AWS or all of their data off of a particular AWS service. Please check the FAQ for more information, or contact AWS Customer Support for more information.

Data Transfer within the same AWS Region
Data transferred "in" to and "out" from Amazon EC2, Amazon RDS, Amazon Redshift, Amazon DynamoDB Accelerator (DAX), Amazon ElastiCache instances, and Elastic Network Interfaces across Availability Zones in the same AWS Region is charged at $0.01/GB in each direction.

IPv4: Data transferred "in" to and "out" from public or Elastic IPv4 address is charged at $0.01/GB in each direction.

IPv6: Data transferred "in" to and "out" from an IPv6 address in a different VPC is charged at $0.01/GB in each direction.

For data transferred between a Local Zone and an Availability Zone within the same AWS Region, "in" to and "out" from Amazon EC2 in the Local Zone is charged at the following rate:

Region:

US East (Atlanta)
Data transferred between a Local Zone and an Availability Zone within the same AWS Region, "in" to and "out" from Amazon EC2 in the Local Zone Pricing
Data transfer in $0.01
Data transfer out $0.01
Data transferred between Amazon EC2, Amazon RDS, Amazon Redshift, Amazon ElastiCache instances, and Elastic Network Interfaces in the same Availability Zone is free.

Data transferred directly (see endpoints) between Amazon S3, Amazon EBS direct APIs\*, Amazon Glacier, Amazon DynamoDB, Amazon SES, Amazon SQS, Amazon Kinesis, Amazon ECR, Amazon SNS or Amazon SimpleDB and Amazon EC2 instances in the same AWS Region is free. If other AWS services are in the path of your data transfer, you will be charged their associated data processing costs. These services include, but are not limited to, PrivateLink endpoints, NAT Gateway and Transit Gateway.

\*For Amazon EBS direct APIs, data transfer charges will apply if FIPS Endpoints are used.

Data transferred "in" to and "out" from Amazon Classic and Application Elastic Load Balancers using private IP addresses, between EC2 instances and the load balancer in the same AWS VPC is free.

In case of AWS Transit Gateway peering, data transferred "out" from each Transit Gateway using private IP addresses, is charged at $0.01/GB in the same AWS Region.

In case of AWS Transit Gateway and AWS Cloud WAN peering, data transferred "out" from Transit Gateway using private IP addresses, is charged at $0.01/GB and data transferred "in" to and "out" from Cloud WAN using private IP addresses is charged at $0.01/GB in the same AWS Region.

Except as otherwise noted, our prices are exclusive of applicable taxes and duties, including VAT and applicable sales tax. For customers with a Japanese billing address, use of AWS is subject to Japanese Consumption Tax. Learn more about AWS tax policies.

EBS-Optimized Instances
EBS-optimized instances enable EC2 instances to fully use the IOPS provisioned on an EBS volume. EBS-optimized instances deliver dedicated throughput between Amazon EC2 and Amazon EBS, with options between 500 and 4,000 Megabits per second (Mbps) depending on the instance type used. The dedicated throughput minimizes contention between Amazon EBS I/O and other traffic from your EC2 instance, providing the best performance for your EBS volumes. EBS-optimized instances are designed for use with both Standard and Provisioned IOPS Amazon EBS volumes. When attached to EBS-optimized instances, Provisioned IOPS volumes can achieve single digit millisecond latencies and are designed to deliver within 10% of the provisioned IOPS performance 99.9% of the time.

For Current Generation Instance types, EBS-optimization is enabled by default at no additional cost. For Previous Generation Instances types, EBS-optimization prices are on the Previous Generation Pricing Page.

The hourly price for EBS-optimized instances is in addition to the hourly usage fee for supported instance types.

Elastic IP Addresses
All In-use and Idle Elastic IP addresses are charged. To see public IPv4 address prices, visit the VPC pricing page.

Carrier IP Addresses
Region:

US East (Verizon) - Atlanta
You can have one Carrier IP (CIP) address associated with a running instance in a Wavelength Zone at no charge. If you associate additional CIPs with that instance, you will be charged for each additional CIP associated with that instance per hour on a pro rata basis.

To ensure efficient use of Carrier IP addresses, we impose a small hourly charge when these IP addresses are not associated with a running instance or when they are associated with a stopped instance or unattached network interface.

$0.005 per additional IP address associated with a running instance per hour on a pro rata basis
$0.005 per Carrier IP address not associated with a running instance per hour on a pro rata basis
$0.00 per Carrier IP address remap for the first 100 remaps per month
$0.10 per Carrier IP address remap for additional remaps over 100 per month
Except as otherwise noted, our prices are exclusive of applicable taxes and duties, including VAT and applicable sales tax. For customers with a Japanese billing address, use of AWS is subject to Japanese Consumption Tax. Learn more about AWS tax policies.

Elastic Load Balancing
To see prices, visit the Elastic Load Balancing page.

On-Demand Capacity Reservations
On-Demand Capacity Reservations are priced exactly the same as their equivalent (On-Demand) instance usage. If a Capacity Reservation is fully utilized, you only pay for instance usage and nothing towards the Capacity Reservation. If a Capacity Reservation is partially utilized, you pay for the instance usage and for the unused portion of the Capacity Reservation. Learn more about On-Demand Capacity Reservations.

T2/T3/T4g Unlimited Mode Pricing
For T4g instances in Unlimited mode, CPU Credits are charged at $0.04 per vCPU-Hour for Linux, RHEL and SLES.

For T2 and T3 instances in Unlimited mode, CPU Credits are charged at:

$0.05 per vCPU-Hour for Linux, RHEL and SLES, and
$0.096 per vCPU-Hour for Windows and Windows with SQL Web
The CPU Credit pricing is the same for all instance sizes, for On-Demand, Spot, and Reserved Instances, and across all regions.

See Unlimited Mode documentation for details on when CPU Credits are charged.

Amazon CloudWatch
To see prices, visit the Amazon Cloudwatch Pricing page.

Amazon Elastic Block Store
To learn more, visit the EBS Pricing Page.

Amazon EC2 Auto Scaling
Auto Scaling is enabled by Amazon CloudWatch and carries no additional fees. Each instance launched by Auto Scaling is automatically enabled for monitoring and the applicable Amazon Cloudwatch charges will be applied.

AWS GovCloud Region
AWS GovCloud is an AWS Region designed to allow U.S. government agencies and contractors to move more sensitive workloads into the cloud by addressing their specific regulatory and compliance requirements. For pricing and more information on the new AWS GovCloud Region, please visit the AWS GovCloud Web Page.

- Your usage for the Free Tier is calculated each month across all regions except the AWS GovCloud region, and automatically applied to your bill - unused monthly usage will not roll over. Does not include Amazon EC2 running IBM, or the AWS GovCloud Region. See offer terms for more details and other restrictions.
  \*\* Rate tiers take into account your aggregate usage for Data Transfer Out to the Internet across Amazon EC2, Amazon S3, Amazon Glacier, Amazon RDS, Amazon Redshift, Amazon SageMaker, Amazon SES, Amazon SimpleDB, Amazon SQS, Amazon SNS, Amazon DynamoDB, AWS Storage Gateway, AWS CloudShell, and Amazon CloudWatch Logs.

(Amazon EC2 is sold by Amazon Web Services, Inc.)

AMD SEV-SNP
Amazon EC2 supports AMD Secure Encrypted Virtualization-Secure Nested Paging (AMD SEV-SNP), a feature on AMD EPYC(TM) processors, on M6a, C6a, and R6a instance types. For more information about AMD SEV-SNP and pricing, refer to this documentation.

When you launch an Amazon EC2 instance with AMD SEV-SNP turned on, you are charged an additional hourly usage fee that is equivalent to 10 percent of the On-Demand hourly rate for the selected instance type.

This AMD SEV-SNP usage fee is a separate charge to your Amazon EC2 instance usage. Reserved Instances, Savings Plans, and operating system usage don't impact this fee

Compute and EC2 Instance Savings Plans
Savings Plans are a flexible pricing model that offer low prices on Amazon EC2, AWS Lambda, and AWS Fargate usage, in exchange for a commitment to a consistent amount of usage (measured in $/hour) for a 1 or 3 year term. When you sign up for a Savings Plan, you will be charged the discounted Savings Plans price for your usage up to your commitment. AWS offers two types of Savings Plans:

Compute Savings Plans

Compute Savings Plans provide the most flexibility and help to reduce your costs by up to 66%. These plans automatically apply to EC2 instance usage regardless of instance family, size, AZ, Region, OS or tenancy, and also apply to Fargate or Lambda usage. For example, with Compute Savings Plans, you can change from C4 to M5 instances, shift a workload from EU (Ireland) to EU (London), or move a workload from EC2 to Fargate or Lambda at any time and automatically continue to pay the Savings Plans price.

EC2 Instance Savings Plans

EC2 Instance Savings Plans provide the lowest prices, offering savings up to 72% in exchange for commitment to usage of individual instance families in a Region (e.g. M5 usage in N. Virginia). This automatically reduces your cost on the selected instance family in that region regardless of AZ, size, OS or tenancy. EC2 Instance Savings Plans give you the flexibility to change your usage between instances within a family in that region. For example, you can move from c5.xlarge running Windows to c5.2xlarge running Linux and automatically benefit from the Savings Plan prices.

Every type of compute usage has a Savings Plan rate and On Demand rate. Below you can see the Savings Plan rates and On Demand rates for every type of offering. You will be charged the Savings Plans rates on the committed usage and any usage beyond the commitment will be charged at regular On Demand rates.

\*Only virtual u-type instances on Shared and Dedicated Instance tenancy can be covered by Savings Plans.

Notice: Red Hat has made an update to their cloud pricing model for Red Hat Enterprise Linux (RHEL). On July 1, 2024 pricing for EC2 RHEL changed to a per-vCPU-hour based pricing model. Learn about the new prices in the RHEL on AWS Pricing page.

Compute Savings Plans for Amazon EC2
Compute Savings Plans apply to EC2 Instance usage regardless of instance family, size, AZ, AWS Region, OS or tenancy.

Select a location type and region
Location Type

AWS Region
Region

Middle East (UAE)
Select terms for your Compute Savings Plans
Term length

1 year
Payment options

No Upfront
Select an operating system and tenancy to view rates
Operating system

Linux
Tenancy

Shared
Viewing 283 available instances

1
2
3
4
5
6
7
...
15

Instance name
Savings Plans rate
Savings over On-Demand
On-Demand rate
Region
Operating system
Tenancy
t4g.nano
$0.0042
18%
$0.0051
Middle East (UAE)
Linux
Shared
t4g.micro
$0.0084
18%
$0.0102
Middle East (UAE)
Linux
Shared
t4g.small
$0.0167
18%
$0.0204
Middle East (UAE)
Linux
Shared
t4g.medium
$0.0335
18%
$0.0408
Middle East (UAE)
Linux
Shared
t4g.large
$0.0669
18%
$0.0816
Middle East (UAE)
Linux
Shared
t4g.xlarge
$0.1338
18%
$0.1632
Middle East (UAE)
Linux
Shared
t4g.2xlarge
$0.2676
18%
$0.3264
Middle East (UAE)
Linux
Shared
t3.nano
$0.0051
19%
$0.0063
Middle East (UAE)
Linux
Shared
t3.micro
$0.0103
18%
$0.0125
Middle East (UAE)
Linux
Shared
t3.small
$0.0205
18%
$0.0251
Middle East (UAE)
Linux
Shared
t3.medium
$0.0411
18%
$0.0502
Middle East (UAE)
Linux
Shared
t3.large
$0.0821
18%
$0.1003
Middle East (UAE)
Linux
Shared
t3.xlarge
$0.1643
18%
$0.2006
Middle East (UAE)
Linux
Shared
t3.2xlarge
$0.3285
18%
$0.4013
Middle East (UAE)
Linux
Shared
m8g.medium
$0.04443
19%
$0.05502
Middle East (UAE)
Linux
Shared
m8g.large
$0.08886
19%
$0.11004
Middle East (UAE)
Linux
Shared
m8g.xlarge
$0.17772
19%
$0.22008
Middle East (UAE)
Linux
Shared
m8g.2xlarge
$0.35544
19%
$0.44016
Middle East (UAE)
Linux
Shared
m8g.4xlarge
$0.71088
19%
$0.88032
Middle East (UAE)
Linux
Shared
m8g.8xlarge
$1.42176
19%
$1.76064
Middle East (UAE)
Linux
Shared

Compute Savings Plans for AWS Fargate
Please make the following selections to view Savings Plan rates for Fargate

Select a location type and region
Location Type

AWS Region
Region

Middle East (UAE)
Select terms for your Compute Savings Plans
Term length

1 year
Payment options

No Upfront
Select an Operating System and CPU Architecture to view rates
Operating system

Linux
CPU Architecture

X86
Viewing 2 Fargate resources

1

Resource
Savings Plans rate
Savings over On-Demand
On-Demand rate
Region
Operating system
CPU Architecture
per GB per hour
$0.00493
15%
$0.0058
Middle East (UAE)
Linux
X86
per vCPU per hour
$0.04471
15%
$0.0526
Middle East (UAE)
Linux
X86

Compute Savings Plans for AWS Lambda
Please make the following selections to view Savings Plan rates for Lambda

Select a location type and region
Location Type

AWS Region
Region

Middle East (UAE)
Select terms for your Compute Savings Plans
Term length

1 year
Payment options

No Upfront
Viewing 4 available instances

1

Usage Type
Unit
Savings Plans rate
Savings over On-Demand
On-Demand rate
Requests
per 1M requests
$0.25
0%
$0.25
Duration
per GB per second
$0.0000182
12%
$0.0000206667
Provisioned Concurrency
per GB per second
$0.0000045
12%
$0.0000051108
Duration (Provisioned Concurrency)
per GB per second
$0.0000105
12%
$0.0000119251

Instance Family Savings Plan rates
EC2 Instance Savings Plans apply to EC2 usage on a specific instance family in a specific AWS Region regardless of AZ, size, OS, or tenancy.

Select a location type and region
Location Type

AWS Region
Region

Middle East (UAE)
Select terms for your EC2 Instance Savings Plans
Term length

1 year
Payment options

No Upfront
Instance family

m5
Select a OS and tenancy to view rates
Operating system

Linux
Tenancy

Shared
Viewing 9 available instances

1

Instance name
Savings Plans rate
Savings over On-Demand
On-Demand rate
Operating system
Tenancy
m5.large
$0.074
37%
$0.118
Linux
Shared
m5.xlarge
$0.148
37%
$0.235
Linux
Shared
m5.2xlarge
$0.297
37%
$0.471
Linux
Shared
m5.4xlarge
$0.593
37%
$0.942
Linux
Shared
m5.8xlarge
$1.186
37%
$1.883
Linux
Shared
m5.12xlarge
$1.78
37%
$2.825
Linux
Shared
m5.16xlarge
$2.373
37%
$3.766
Linux
Shared
m5.24xlarge
$3.559
37%
$5.65
Linux
Shared
m5.metal
$3.559
37%
$5.65
Linux
Shared

Amazon EC2 Spot Instances Pricing
Try Amazon EC2 for Free
## How does Amazon EC2 Spot Instances pricing work?

With Spot Instances, you pay the Spot price that's in effect for the time period your instances are running. Spot Instance prices are set by Amazon EC2 and adjust gradually based on long-term trends in supply and demand for Spot Instance capacity. To learn more about pricing, visit the Spot Instance history page. The following table displays the Spot price for each region and instance type (updated every 5 minutes).

Spot Instances are available at a discount of up to 90% off compared to On-Demand pricing. To compare the current Spot prices against standard On-Demand rates, visit the Spot Instance Advisor.

Note that you can now run Linux based RHEL and SUSE AMIs on Spot Instances. Learn more.

Spot Instance Prices
Note: T4g and T3 instances launch as unlimited by default. If you launch T4g or T3 Spot Instances as unlimited and plan to use them immediately and for a short duration, with no idle time for accruing CPU credits, you will incur charges for surplus credits. If the average CPU usage over a 24-hour period exceeds the baseline, you will also incur charges for surplus credits. We recommend that you launch your T4g or T3 Spot Instances in standard mode to avoid paying higher costs. For more information, see Surplus Credits Can Incur Charges and Spot Instance limits.

The prices displayed below are the lowest prices per instance type in the region. For more information on Spot Instances pricing and to see the current price for each instance type and Availability Zone, please refer to Spot Instance pricing history in the EC2 User Guide.

Notice: Red Hat has made an update to their cloud pricing model for Red Hat Enterprise Linux (RHEL). On July 1, 2024 pricing for EC2 RHEL changed to a per-vCPU-hour based pricing model. Learn about the new prices in the RHEL on AWS Pricing page.

Select a location type and region
Location Type

AWS Region
Region

Middle East (UAE)
Instance Family

All

1
2
3
4
5
6
7
...
28

## Instance Type
Linux/UNIX Usage
Windows Usage
Instance Family
c5.12xlarge $0.8944 $2.5432 Compute Optimized - Current Generation
c5.18xlarge $0.5386 $3.6922 Compute Optimized - Current Generation
c5.24xlarge $1.1475 $5.0904 Compute Optimized - Current Generation
c5.2xlarge $0.1862 $0.4238 Compute Optimized - Current Generation
c5.4xlarge $0.3325 $0.8473 Compute Optimized - Current Generation
c5.9xlarge $0.7289 $1.9083 Compute Optimized - Current Generation
c5.large $0.0421 $0.1066 Compute Optimized - Current Generation
c5.metal $1.1389 $5.088 Compute Optimized - Current Generation
c5.xlarge $0.0807 $0.2118 Compute Optimized - Current Generation
c5d.12xlarge $0.6535 $2.5923 Compute Optimized - Current Generation

- Windows(R) is not currently available for Cluster Compute or Cluster GPU Instances
