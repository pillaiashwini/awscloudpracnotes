# AWS Certified Cloud Practitioner Exam Preparation Workshop

## AWS Certified Cloud Practitioner Exam Details

* Covers foundational concepts for any technical role
* Proctored Exam
* 90 Minutes
* 65 Multiple Choice, Multiple Answer Questions



## Certification Areas of Focus

- Cloud Concepts :cloud:
- Security 
- Billing / Pricing
- Technology

# Overview

* Understanding AWS Infrastructure
* Reviewing the Shared Responsibility Model
* Examining the Economics of the Cloud
* Architecting Infrastructure on AWS
* Supporting Your AWS Infrastructure


## AWS Global Infrastructure

**Regions:**

- Based in a specific geographic region
- Made up of two or more Availability Zones (AZ’s)
- Offers a specific subset of AWS services

**Availability Zones**

- Made up of one or more data centers
- Low latency communication between availability zones
- Designed to isolate any failure to a single availability zone

**AWS Edge Locations**

- Used as nodes of a global content delivery network
- Allows AWS to serve content from locations closest to users
- Primarily used by Amazon CloudFront and related services

## Shared Responsibility Model

> Security and Compliance is a shared responsibility between AWS and the customer.

**Security of the cloud - AWS**

- [ ] Access & **Training** for Amazon Employees
- [ ] Global Data Centers & Underlying Network
- [ ] Hardware for Global Infrastructure
- [ ] Configuration Management for Infrastructure
- [ ] Patching Cloud Infrastructure & Services

**Security in the cloud - Customer**

- [ ] Individual Access to Cloud Resources & **Training**
- [ ] Data Security & Encryption (both in transit and at rest)
- [ ] Operating System, Network, and Firewall Configuration
- [ ] All Code Deployed onto Cloud Infrastructure
- [ ] Patching Guest OS and Custom Applications

## Economics of Cloud

**Capitalized Expenditure (CapEx)**

> When building a data center, an organization invests in upfront costs for the building, servers, and supporting equipment. 
> This type of expense to attain a fixed asset is referred to as a Capitalized Expenditure or CapEx.
> 

**Operating Expenditure (OpEx)**

> The regular day to day expenses of a business are considered Operating Expenditures or OpEx. After theinitial build of a data center, ongoing connectivity, utility, and maintenance costs would be considered OpEx.
> 


## AWS Cost Planning Tools

**AWS TCO Calculator**

Enables an organization to determine what could be saved by leveraging cloud infrastructure.

[TCO Calculator](https://aws.amazon.com/tco-calculator/)

**AWS Simple Monthly Calculator**

Enables an organization to calculate the cost of running specific AWS infrastructure.

[Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html)

**AWS Cost Explorer**

User Interface for Exploring Your AWS Costs
Provides Breakdowns Including

- By Service
- By Cost Tag (This is important and can come up in the exam)

Provides Predictions for the Next Three Months of Costs
Gives Recommendations for Cost Optimization
Can Be Accessed via API

**AWS Organizations**

1. Allows organizations to manage multiple accounts under a single master account
1. Provides organizations with the ability to leverage Consolidated Billing for all accounts
1. Enables organizations to centralize logging and security standards across accounts

## Architecture on AWS

### **Well Architected Framework**

The Well Architected Framework is a collection of best practices across five key pillars for how to best create systems that create business value on AWS.

**Operational Excellence**
Running and monitoring systems for business value
**Security**
Protecting information and business assets
**Reliability**
Enabling infrastructure to recover from disruptions
**Performance Efficiency**
Using resources efficientlyto achieve business value
**Cost Optimization**
Achieving minimal costs for the desired value

Remember the Pillars => **O**pen **S**ource **R**equires **P**ersonal **C**ommitment

### **Reliability on AWS**

#### **Fault Tolerance**
Being able to support the failure of components within your architecture


#### **High Availability**
Keeping your entire solution running in the expected manner despite issues that may occur

### **AWS Disaster Recovery Approaches**

**Backup & Restore**
Backups of systems are stored to restore in a DR event
**Pilot Light**
Minimal resources are setup in AWS to support a DR event
**Warm Standb**y
Systems are running in AWS and can be scaled up for DR
**Multi-Site**
Systems are running in two regions and support users

## Supporting Your AWS Infrastructure

**AWS Basic Support**

* Provided for All AWS Customers Access to Trusted Advisor (7 Core Checks)
* 24x7 Access to Customer Service,Documentation, Forums, & Whitepapers
* Access to Personal Health Dashboard
* No Monthly Cost

**AWS Developer Support**

* Includes all Features of Basic Support Business Hours Access to Support Engineers
* Limited to 1 Primary Contact
* Starts at $29 per month (tied to AWS usage)

**AWS Business Support**

* Includes all Features of Developer Support
* Full Set of Trusted Advisor Checks
* 24x7 Phone, Email, and Chat Access to Support Engineers
* Unlimited Contacts
* Starts at $100 per month (tied to AWS usage)

**AWS Enterprise Support**

* Includes all Features of Business Support
* Includes Designated Technical Account Manager (TAM)
* Includes Concierge Support Team Starts at $15,000 per month (tied to
* AWS usage)

## Interacting with AWS Services

- Use the AWS Management Console
- Use the AWS CLI
- Use the AWS SDK (.NET, Java, Python etc.)

## Networking and Content Delivery

- Amazon Route 53 - DNS, Global Service, 100 % SLA
- Amazon VPC - Logically isolated section of AWS where you can launch AWS resources in a virtual network that you define
- Amazon Direct Connect - Establish dedicated network connection from your on-premises to AWS
- Amazon API Gateway - Fully managed API Management Service
- Amazon CloudFront - Content Delivery Network leveraging Edge locations
    - Includes advanced features like AWS Shied for DDoS
    - AWS WAF
- Elastic Load Balancing
    - Distributes traffic across multiple targes
    - Supports Multi-AZ architecture
    - Types
        - Application Load Balancer
        - Network Load Balancer
        - Classic Load Balancer

## Security on AWS

Identity and Access Management
- Controls access to AWS resources
- Manages both Authentication and Authorization
- Supports Identity Federation
    - Principals include
        - Users
        - Groups
        - Roles
- Policies in AWS IAM
    - JSON Document that defines permissions for an IAM Principal
    - Defines what services a principal can access and what actions can be taken on that service
    - ![](https://i.imgur.com/U0qYD2E.png)

### **IAM Best Practices**

**Multi-factor Authentication**

Provides additional security with either a physical or virtual device that generates a token for login

**Least Privilege Access**

Users should only be granted access to AWS resources that are required
for their current tasks

![](https://i.imgur.com/Tc1ANZK.png)

### Security in Amazon VPC

Security Groups - Firewall. Stateful
Network ACL's - Applied to Subnets. Not statefull
Flow Logs - Information around traffic within your VPC

Additional Security Services on AWS

CloudTrail - Enables logging of all actions (API) made within your AWS Account
AWS Shield - Provides detection of DDoS Attacks
AWS WAF - Protects Web Application from common exploits
AWS Inspector - Vulnerability Detection via agents installed on EC2


## Compute Services
- Amazon EC2 - Virtual Machines
- AWS Lambda - Serverless Functions as a Service
- Amazon ECS - Containerized Applications

## Purchase Options for EC2
- On-demand - Pay by the second or hour for instances launched
- Reserved - Purchase discount instances in advance for 1-3 years
- Spot - Leverage unused capacity in a region for large discount

### Tips

* If you have an instance that is consistent and always needed, you should purchase a Reserved Instance.
* If you have batch processing where the process can start and stop without affecting the job, you should leverage Spot Instances.
* If you have an inconsistent need for instances that cannot be stopped without affecting the job, leverage On-demand Instances.

## Container Management Services for AWS

 - Amazon ECS - Container Orchestration Service on AWS
 - AWS Fargate -Containerized Applications without managing Servers
 - Amazon EKS - Managed Kubernetes on AWS

## AWS Lambda

1. Enables the running of code withoutprovisioning infrastructure
1. Only charged for usage based on execution time
1. Can configure available memory from 128 MB to 3008 MB
1. Integrates with many AWS services
1. Enables event-driven workflows
1. Primary service for serverless architecture

**AWS Elastic Beanstalk**

* Automates the process of deploying and scaling workloads on EC2
* Supports a specific set of technologies
* Leverages existing AWS services
* Only pay for the other services youleverage
* Handles provisioning, load balancing, scaling, and monitoring

## Storage on AWS

### Amazon S3 
* Stores files in buckets
* Provides different storage classes for different use cases
* Stores data across multiple availabilityzones
* Enables URL access for files
* Can provide transfer acceleration foruploads using AWS edge locations
* Offers configurable rules for data lifecycle

### Amazon S3 Non-archival Storage Classes
S3 Standard is the default storage class and is for frequently accessed data.
S3 Intelligent-Tiering will move your data to the correct storage class based on usage.
S3 Standard-IA is for infrequently accessed data with the standard resilience.
S3 One Zone-IA is for infrequently access data that is only stored in one AZ

### Amazon Glacier

* Designed for archiving of data within S3 as separate storage classes
* Offers configurable retrieval times
* Can send files directly or through lifecycle rules in S3
* Provides two different storage classes
- **S3 Glacier**
    - Designed for archival data
    - 90 day minimum storage duration change
    - Can be retrieved in either minutes or hours
    - You pay a retrieval fee per GB retrieved
    - Over 5 times less expensive than S3 Standard storage class
- **S3 Glacier Deep Archive**
    - Designed for archival data
    - 180 day minimum storage duration change
    - Can be retrieved in hours
    - You pay a retrieval fee per GB retrieved
    - Over 23 times less expensive than S3 Standard storage class



## Amazon EC2 File Storage Services

### Amazon EBS
Persistent block storage for use with Amazon EC2
Enables redundancy within an AZ
Allows users to take snapshots of its data
Offers encryption of its volumes
Provides multiple volume types
- General purpose SSD
    - General Purpose SSD is a cost effective type designed for general workloads.
- Provisioned IOPS SSD
    - Provisioned IOPS SSD high performance volume for low latency applications.
- Throughput optimized HDD
    - Throughput Optimized HDD is designed for frequently accessed data
- Cold HDD
    - Cold HDD is designed for less frequently accessed workloads

### Amazon EFS
Elastic file system for use with Linux-based workloads

* Fully managed service
* Designed for Linux workloads
* Supports up to petabyte scale
* Stores data across multiple AZ’s
* Provides two different storage classes
* - Standard
* - Infrequent access
* Provides configurable lifecycle data rules

## AWS Storage Gateway

- Useful for Hybrid Scenarios
- AWS Storage Gateway connects an on-premises software appliance with cloud-based storage to provide seamless integration with data security features between your on-premises IT environment and the AWS storage infrastructure.
-  You can use the service to store data in the AWS Cloud for scalable and cost-effective storage that helps maintain data security.
-  AWS Storage Gateway offers 
    -  file-based, 
    -  volume-based, 
    -  and tape-based storage solutions

![](https://i.imgur.com/gTCYYjd.png)


## Databases on AWS

- Amazon RDS
- Amazon Aurora
- Amazon DynamoDB
- Amazon Redshift
- Amazon Elasticache
- AWS Database Migration Service

### Amazon Relational Database Service (RDS)

* Fully managed service for relationaldatabases
* Handles provisioning, patching, backup,and recovery of your database
* Supports deployment across multiple availability zones (multi-AZ)
* Some platforms support read replicas
* Launches into a VPC
* Provides both general purpose SSD and provisioned IOPS SSD drive options
* Platforms Include
    * MySQL
    * PostgresSQL
    * MariaDB
    * Oracle Database
    * SQL Server
    * Amazon Aurora

## Amazon DynamoDB

* Fully managed NoSQL database service
* Provides both key-value and document database
* Enables extremely low latency at virtually any scale
* Supports automated scaling based on configuration
* Offers in-memory cache with the DynamoDB Accelerator (DAX)

## Amazon Redshift

* Scalable data warehouse service
* Supports petabyte scale warehousing of data
* Leverages high performance disks and columnar storage
* Offers the ability to fully encrypt contents 
* Provides isolation with a VPC
* Enables querying of exabytes of data in Amazon S3 using Redshift Spectrum

## Amazon Elasticache

* Fully managed in-memory data stores
* Supports both Memcached and Redis
* Provides low latency in response times
* Enables scaling and replicas to meet application demand
* Handles common use cases including
    - Database layer caching
    - Session storage

## AWS Database Migration Service

Enables you to securely migrate data into AWS in an
efficient manner for both homogeneous and heterogeneous migrations either all at once or in a continual manner.

Whenever you want to 'migrate a database', DMS is your friend

## AWS App Integration Services

### Amazon SNS - Managed Pub / Sub Messaging Architecture
* Fully managed pub/sub messaging service
* Enables you to create decoupledapplications
* Organized according to topics
* Integrates with multiple AWS services
* Provides end user notifications across SMS,email, and push notifications

![](https://i.imgur.com/XW2Ybdc.png)

### Amazon SQS - Managed Message Queue Service

* Fully managed message queue service
* Enables you to build decoupled and fault tolerant applications
* Supports up to 256 KB data payload
* Allows messages to be store up to 14 days
* Provides two types of queues
* - Standard queue
* - FIFO queue (first in first out)

## Management & Governance Services

### AWS CloudTrail
 - Enables operational auditing of APIs of your AWS account

### AWS CloudFormation

- Provides infrastructure as code capabilities for AWS
- Managed service for provisioning infrastructure based on templates
- No additional charge
- Templates can be YAML or JSON
- Enables infrastructure as code
- Manages dependencies between resources
- Provides drift detection to find changes in your infrastructure

```yaml

Description: Creates an S3 bucket
Resources:
 SampleS3Bucket:
  Type: AWS::S3::Bucket
  Properties:
   BucketName: sample-s3-bucket
   
```
The code above if placed within a full CloudFormation template would create a single S3 bucket

### AWS CloudWatch

- Enables monitoring and metrics on your AWS resources
- Monitoring and management service
- Collects logs, metrics, and events from most AWS services 
- Enables alarms based on metrics
- Provides visualization capabilities for metrics
- Allows for custom dashboards based on collected metrics

## Additional Topics

### AWS Acceptable Use Policy

The AWS Acceptable Use Policy defines prohibited uses
of the services offered by AWS. All users of the platform are bound by this policy.

## AWS Marketplace

* Curated catalog of third-party solutions for customers to run on AWS
* Provides AMI’s, CloudFormation stacks, and SaaS based solutions
* Enables different pricing options to overcome licensing in the cloud
* Charges appear on your AWS bill

## AWS Large Scale Data Transfer Services

### AWS Snowball
Service to physically migrate petabyte scale data to AWS
![](https://i.imgur.com/OcKOYrH.png)


### AWS Snowmobile
Service to physically migrate exabyte scale data onto AWS

![](https://i.imgur.com/4TaHSny.png)

### AWS Teams

* AWS Enterprise Support - Support Engineers + TAMs
* AWS Solutions Architects - Help Customers Architect solutions on AWS
* AWS Professional Services - Paid Services team that help customer deploy solutions on AWS
* AWS Partner Network Technology Partners - They build products using AWS Services
* AWS Partner Network Consulting Partners - If a customer does not have in-house AWS Expertise, then they can leverage Consulting Partners


## Exam Review

### Reviewing Cloud Concepts

* Review how cloud platforms differ from traditional data centers
* Review how AWS organizes its infrastructure globally
* Understand how scalability differs in the cloud from traditional data centers
* Review CapEx and OpEx expenditures

### Reviewing Security

* Understand the Shared Responsibility Model from AWS
* Review highlighted best practices for securing your AWS account & resources
* Review options for securing traffic within a VPC
* Review IAM and identity types
* Understand Least Privilege Access

### Reviewing Billing & Pricing

* Review tools that help you understand AWS costs
* Understand the most cost-effective ways to leverage core services
* Review how costs differ from traditional data centers
* Review ways that organizations can manage and review costs
* Understand different support plan levels

### Reviewing Technology

* Write down AWS services we covered and a summary of each
* Implement basic solutions using the services we covered
* Review architectural principles for fault tolerance & high availability
* Analyze scalability approaches

## Testing Best Practices

* Take time to analyze each question for its intent
* Try the principal of eliminating incorrect options
* Review what is required for the answer on each question
* Skip a question if it takes too much time. Mark it for review if required
* Leverage the review capability
* Guess if you don’t know the answer after the review phase
* Examine the clock after each 10 questions
* Approximately 1.3 mins per question
