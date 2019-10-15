# AWS Cloud Practitioner courses

I wanted to take some good notes for anyone to refresh on their training before the Cloud Practitioner Exam. Below each section will be a few of the knowledge check questions. Try to answer them without referencing the notes above.

## Define what the cloud is and how it works

### Cloud computing

Instead of having to design and build your own data center, you allow the internet to scale your application as needed based on usage.

### Perks of cloud computing

Reduce risk(being agile), secure data(using common models or integrating security checks into deployment pipeline), scalability(resize resources as necessary ie. elasticity), plan for natural disaster(Low liability and multiple regions creating fault tolerance), experiment and innovative culture promotion.

### Three ways to use AWS

1. AWS Management Console
2. CLI - command line interface
3. SDK

## Knowledge Check

#### Which of the following terms refers to the power to scale computing resources up or down easily?

1. Economy
2. Elasticity
3. Efficiency
4. Expediency

## Differentiate between cloud computing and deployment models

### EC2 - Elastic Cloud Compute

Computer instance where you can choose hardware config, OS image, Port forwarding and service enabling (ssh, http).

### EBS - Elastic Block Store

Storage units for EC2 instances. Designed for being durable and available. Hard drive equivalent (ssh, magnetic hd) with snapshot config. Commonly used to store a database to keep database changes separate from OS hard disk.

## Knowledge Check

What are the benefits of using Amazon EC2 instance compared to physical servers in your infrastructure (select two)?

A [ ] - Pay only for the capacity you use
B [ ] - Resizable
C [ ] - The ability to have different storage requirements
D [ ] - The ability to hot-add additional RAM
E [ ] - Automatic automated backups

Answer: A, C

### S3 - Simple Storage service

1. Managed cloud storage service
2. Store virtually unlimited number of objects
3. Access any time from anywhere
4. Rich security controls

Data storage (images, videos etc.) that is accessed via your bucket (mediacenter) and a key (welcome.mp4) for example `mediacenter/welcome.mp4`

#### Common use cases

Storing application assets
Static Web Hosting
Backup and Disaster recovery
Staging area for big database

# Describe the AWS Cloud value proposition

# Describe the basic global infrastructure of the cloud

## Regions

Pick region close to where you're hosting to increase latency

## Availibilty zones

Physically distinct and independent infrastructure. UPS (uninteruptable power supply) and backup availability zones to never lose access to your services

## Edge Locations

Content delivery to end users. Edge locations forward your service to the end user quicker by having higher access in areas with high traffic

## Knowledge check

Which components of the AWS infrastructure can be described as multiple, isolated locations, within one geographic area?

regions
edge Locations
s3 buckets
availability zones

Answer: Availability zones

### Amazon Virtual Private Close (VPC)

Region based networking tool to control allowed internet gateways, subnets of both private and public resources.

### Security Groups

Measures to filter traffic to your AWS instances.
Using VPC's you can generate security groups that act as firewalls through a series of rules to access your instances.


## Knowledge Check

Which of the following statements is true of Amazon VPC

Each VPC is private, dedicated network connection from your premises to AWS
Each AWS account can have only one VPC associated with it
A VPC acts as a physical firewall for your cloud infrastructure
You can create many subnets in a VPC, though fewer is recommended to limit complexity

Answer: You can create many subnets in a VPC, though fewer is recommended to limit complexity

# Define the billing, account management, and pricing models for the AWS platform


# Module 3 Integrated Services

## Application load balancer

Second type of load balancer.

#### Use Cases

Applications in EC2 instances controlled by a single load balancer for applications in the EC2 instances. For example two EC2 instances forwarding an application and using a load balancer to forward each of those ec2 apps on a different port but on the same dns address

### Features

#### Path and host-based routing

Path - rules that forward requests to different target groups
Host - rules that forward requests to different target groups based on host name

## Auto Scaling

Ensures you have correct number of EC2 instances available to handle the load. Monitor your resource performance using AMazon cloud watch. Creating a scaling policy tells auto-scaling when and how it will scale (up or down) based on application usage.

## Amazon Route 53

Create DNS Zones for your applications. 

## Knowledge Check

You have an app composed of individual services. You need to route a request to a service based on the content of the request. Which service do you use?

Amazon Route 53
AWS CloudTrail
EC2 Auto Scaling
Elastic Load Balancing

Answer: Elastic Load Balancing

## Amazon Relational Database Service (RDS)

Manages OS install and patches, backups, availability, scaling, etc. so you can focus on application performance. 

## AWS Lambda

Serverless computing. 
Use cases: Continuous scaling. Automated backups, IoT, serverless sites, etc.

## AWS Elastic Beanstalk

Platform as a service, quick deployment, reduce management complexity.

## Knowledge check

What's the first step to using AWS Lambda?

Deploy an OS image
Upload your Code 
Provision EC2 instances
Pay for estimated compute time

Answer: Upload your Code

## AWS simple notification service (SNS)

Pub/Sub messaging (email sms). Subscribe email or phone or other things to get notifications for amazon changes that you choose to subscribe to.

## Amazon CloudWatch

Metrics for your AWS services such as CPU utilization, status check failures, State changes, snapshots. Lets you set alarms that trigger other services. Can Stop,terminate, or reboot services. 

## Amazon CloudFront

Use multiple edge locations and regions to cache your application if your app is stored in a different region but your users are in another region or edge location.

## AWS CloudFormation

Simplify tasks of repeatably and predictable nature. Take in JSON or YAML formatted templates to spin up an ec2 instance. Similar to docker and using the depends on, you don't need to create the templates in order. Automate product operation of AWS tools.

## Knowledge Check

Which of the following best describes amazon CloudFront? 
Provides a common language for you to describe and provision all the infrastructure resources in your cloud environment
Speeds up the delivery of your content to viewers across the globe
Provides you with data and actionable insights to monitor your applications
Provides topics for high-throughput, push based, many to many messaging

Answer: Speeds up the delivery of your content to viewers across the globe

# Module 4 Architecture

## AWS Well-Architected Framework

5 Pillars - Security, Reliability, Performance efficiency, Cost optimization, Operational excellence

### Security

IAM - Identity and access management
Detective controls - integrate auditing controls of logs 
Infrastructure protection - allowing only those who are allowed through rules 
Data protection - data backup, replication, classification, encryption
Incident response - process made to respond and mitigate security incidents

#### Design Principles
Implement security at all layers 
Enable traceability - logs
Apply principle of least privelege - access controls and authentication
Focus on securing your system - 
Automate - scalability and cost efficiency

### Reliability

Ability of a system to recover from issues/failures

#### Best practices

Foundations
Change management
Failure management

#### Design Principles

Test recovery procedures - simulate failures and test reactions before an actual failure
Automatically recover - automate your recovery plans before they occur
Scale horizontally - fault tolerence using multiple small resources
Stop guessing capacity - 
Manage change in automation - 

### Performance Efficiency

Select customizable solutions - Ones where you can support scaling for the possible 
Review to continually innovate - always look at the newest tools to ensure you're using the best solution for your hosting
Monitor AWS services - Amazon Lambda and many more
Consider trade-offs - 

#### Design Principles

Democratize advanced tech
Go global in minutes
Use a serverless architecture
Experiment more often
Have mechanical sympathy

### Cost optimization

Continual process of refinement of a system to maximize ROI

Use cost-effective resources
Matching supply with demand 
Increase expenditure awareness
Optimize over time

#### Design Principles

Adopt a consumption model
Measure overall efficiency
Reduce spending on data center operations
Analyze and attribute expenditure
Use managed services

### Operational Excellence Pillar

Manage and automate changes
Respond to events
Define the standards to manage daily ops

## Fault Tolerance and High Availability

Fault tolerance - ability of a system to remain operational. Built in redundancy. 
High Avail - keeping your service available the most amount of time

### High Availability tools

Elastic Load Balancers - distribute incoming traffic. 
Elastic IP address - static IP addresses. Mask failures. Continues to access apps if an instance fails.
Route 53 - translate domain names to IP addresses. Geo-location routing, health checks, latency checks, etc.
Auto Scaling - terminate/launch instances.
Amazon CouldWatch - distributed statistics gathering system. Tracks metrics of infrastructure.

### Fault tolerant tools

Amazon Simple Queue Service (SQS) - email notification service etc.
Amazon Simple storage service (S3) - backup to storage of files 
Amazon Relational Database Service (RDS) - scaled, fault tolerant database, automate backups

## Web Hosting

Traditionally this would cost more because you have to maintain and manually control all the resources yourself. Amazon takes care of all of this reducing cost, handling traffic spikes, and testing resources. 

## Knowledge Check

Which of the following is NOT a pillar of the AWS Well-architected framework? 
Persistence
Operational Excellence
Security
Cost Optimization

Answer: Persistence

# Module 5 Security

## Shared Responsibility Model

Both you and AWS is responsible for security.
Layers of the app
- Physical - done by AWS to provide secure network
- Network - uses AWS network and compliant
- Hypervisor - AWS runs this to ensure we can run many instances without any concer
- Guest OS - AWS Has not control in this
- Application - AWS has no control into the app
- User Data - AWS has no control of user data

## Identity and Access Management (IAM)

User - Operator
Group - overlap of User and Role
Role - authentication method for a User. Temporary. Not permissions.
Policy Document - permissions, json, directly to a user or group of users, or a role

API call - put file in s3, they provide the file and hits an endpoint with credentials. IAM validates the user using info from group or user data, and then checks if the operation you're requesting is allowed by the policy documents.

If a hacker gets your info (username, password) and you have no 2FA, they could start deleting resources and threatening your organization in order to stop the data loss. Using IAM you can cut off all permissions and have a log of operations attempted to narrow down where the login was compromised will still protecting your system.

## Knowledge check

Your web app requires temp auth to use AEWS services. Which IAM entity should be used?

User
Role
MFA
Group

Answer: Role

## Amazon Inspector

Automated tool to inspect security vulnerabilities and deviations from best practices related to security.

Streamline security compliance, increase dev agility, enforce security standards, integrate security into devops. 

## AWS Shield

Managed DDoS protection service that safeguards apps running on AWS

DDoS mitigation challenges - complex setup and implementation, bandwidth limitations, manual intervention, time consuming, degraded performance etc.

Standard - auto protection of any resource or regions in AWS, quick detection, automated mitigation techniques, and self service (no need to engage AWS support)

## Security Compliance

### Shared Responsibility
AWS - Provide secure controlled platform and wide array of security features
Customer - Configure IT to support your ops

### Assurance programs

Certification/attestations
Legal support
Alignment/frameworks

AWS Perform security tests to their compliance certification rules.



## Knowledge Check

Which of the following is managed DDoS protection service?

Amazon Inspector
AWS Trusted Advisor
AWS Identity and Access Management
AWS Shield

Answer: AWS Shield

# Module 6 Pricing and Support

## Pricing Details

### Pay for
- Compute capacity
- Storage
- Outbound data transfer (aggregated)


### No charge for
- Inbound data transfer
- data transfer between services


## Amazon EC2
Cost factors
- Clock-second/hourly billing
  - Resources incur charges only when running
- Instance config
  - Physical capacity of the instance
  - Varies based on
    - AWS region
    - OS
    - number of coures
    - memory

### On-demand instances
- compute capacity by the hour and second
- min 60 secs

### Reserved instances
- low or no up-front payment instances reserved
- discount on hourly charge for that instance

### Spot instances
- bid for unused ec2 capacity

### Other considerations
#### Number of instances
- provision multiple instance to handle peak loads

#### Load balancing
- Use Elastic load balancing to distribute traffic
- Monthly cost based on:
  - hours load balancers run
  - data load balancer processes

### Product options
#### Monitoring
- Amazon CloudWatch
#### Auto Scaling
Auto scaling...


## Amazon S3
### Cost considerations
#### Storage classes
Standard
- 99.99999999999% durability
- 99.99% avail

SIA 
- same durability
- 99.9% availability

Storage Cost
- number and size of objects
- type of storage

Requests
- PUTS get different rates than GETS
- number of requests
### Amazon EBS
Volume types
- General purposed SSD
- Provisioned IOPS SSD
- Magnetic

Snapshots
- Added cost per GB-month of data stored
- Data Transfer
  - inbound free
  - outbound tiered for discounts

## Amazon RDS
Cost efficient and resizeable capacity
### Cost factors
- clock-hour billing - charges when running
- db characteristics - Engine, size, memory
- DB purchase type - on-demand (by hour), reserved(up front), etc.
- provisioned storage 
  - no additional storage for 100% of storage
  - backups terminated DB instance billed GB/month
- Deployment type
  - storage and I/O charges vary
  - single avail
  - multi avail zones

## Amazon CloudFront

Hosting content to serve to multiple regions

## AWS Trusted Advisor

Cost Optimization, Performance, Security, Fault Tolerance

Saved over 500 million for customers

## AWS Support Plans

Plans to help your needs and hosting. 

## Knowledge Check

Which of the following statements best describes AWS Trusted Advisor?

A. A tool that estimates the cost savings when using AWS and provides a detailed set of reports
B. A tool that helps customers estimate their monthly AWS bill more efficiently
C. A tool that enables you to view and analyze your costs and usage
D. A tool that provides you real time guidance to help you provision your resources following AWS best practices.

Answer - D. A tool that provides you real time guidance to help you provision your resources following AWS best practices



# End of modules
## Recommend resources to review before exam

- https://d0.awsstatic.com/whitepapers/aws-overview.pdf
- https://d1.awsstatic.com/whitepapers/AWS_Cloud_Best_Practices.pdf
- https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf
- https://media.amazonwebservices.com/AWS_TCO_Web_Applications.pdf
- https://aws.amazon.com/premiumsupport/plans/
  

Take some practice exams and then go get your certificate!

https://aws.amazon.com/certification/certified-cloud-practitioner/

# Continued Notes from Pluralsight AWS Certification course

Regions contain 2 or more availability zones

## Shared Responsibility

AWS is responsible for security of the cloud.
- Access and Training for Amazon employees
- Global Data Centers and Underlying Network
- Hardware for Global Infrastructure
- Configuration Management for Infrastructure
- Patching cloud Infrastructure and Services

Customer is responsible for security in the cloud
- Individual Access to cloud resources and training
- Data security and encryption (in transit and at rest)
- Operating System, Network, and Firewall configuration
- All code deployed onto cloud infrastructure
- Patching Guest OS and Custom Applications

## Economics of the Cloud

### Capitalized Expenditure (CapEx)

Building a Data center, upfront costs for the building, servers, and support equipment. Expense to attain a fixed asset.

### Operating Expenditure (OpEx)

Regular day to day expenses of a business. Ongoing connectivity, utility, maintenance costs.

AWS takes care of the potential unused CapEx and up-front costs.  Managed scaling for OpEx. 

### AWS Cost Explorer

User Interface for exploring your AWS Costs
Provides breakdowns including
- By service
- By cost tag

Provides predictions for the next three months of cost
Gives recommendations for cost optimization
Can be accessed via API

### AWS Organizations

Allows organizations to manage multiple accounts under a single master account
Provides orgs with the ability to leverage consolidated billing for all accounts
Enables organzations to centralize logging and security standards across accounts

## Architecture on AWS

### Well Architected Framework

- Operational Excellence - running and monitoring systems for business value
- Security - Protecting Info and business assets
- Reliability - Enabling infrastructure to recover from disruptions
  - Fault tolerance
  - High availability
- Performance Efficiency - Using resources efficiently to achieve business value
- Cost optimization - Achieving minimal costs for the desired value

### AWS Disaster Recovery Approaches
- Backup and Restore 
- Pilot Light - minimal resources are setup in AWS to support a DR event
- Warm Standby - Systems are running in AWS and can be scaled up for DR
- Multi-Site - systems are running on two regions and support users

### Basic Support

Provided for all aws customers
Access to Trusted Advisor (only 7 core checks)
24 x 7 access to customer service, documentation, forums, and whitepapers

### Developer Support

Includes all features of basic support
Business hours access to support engineers
$29 per month(tied to usage)
Limited to 1 Primary contact

### Business Support

Include all Developer support
Full set of Trusted Advisor Checks
24 x 7 phone, email, and chat access to support engineers
Unlimited contacts
$100 per month(tied to usage)

### Enterprise Support
Includes all Business support
Include Designated Technical Account Manager (TAM)
Includes concierge support team
$15000 per month (tied to usage)

## AWS Services

#### AWS Console

Users leverage browser to configure resources

#### AWS CLI

Command line access

#### AWS SDK

Programmatic access

### Networking and Content Delivery 

#### Amazon Route 53

DNS service(yes service-ception).High availability service(service goes down and you can still provide same level of service).  

#### Amazon VPC

Enables virtual networks
Supports IPv4 and IPv6
Supports public and private subnets
Can utilize NAT for private subnets
Enables connection to your data center
Can connect to other VPC's
Supports private connections to many AWS services

#### Amazon Direct Connect

Easy to establish a dedicated network connection from your premises to AWS.

#### Amazon API Gateway


#### Amazon CloudFront

Content delivery network
Enables users to get content from closest server to them
Supports static and dynamic content
Uses AWS edge locations
Includes advanced security features 
- AWS Shield for DDoS
- AWS WAF (firewall)

#### Amazon Elastic Load Balancing
Distribute traffic across multiple targets
Supports one or more availability zones but only one region
Three types
- Application load balancer
- Network LB
- Classic LB

## Security on AWS

Security and compliance is a shared responsibility between AWS and the customer

### AWS Identity and Access Management (IAM)

Control access to services
Free
Manage both authentication and authorization
Support Identity federation

Users - physical user accounts
Groups - manage permissions for group of IAM users
Roles - assume permissions for a task

Policies in AWS IAM
JSON doc that defines permissions for an AWS IAM identity (principal)
Defines both AWS services that the identity can access and what actiosn they can perform

##### Best practices in IAM
MFA - multi-factor auth
Least Privilege Access - only users who are granted access that require it for their current tasks should have it

#### Security in Amazon VPS

Security Groups - Enables firewall-like controls for resource within VPC
Network ACL's - controls inbound and outbound traffic for subnets within VPC
Flow logs - captures info arround traffic within your VPC

##### Additional Security Services

- AWS CloudTrail - logging of all actions taken within your AWS account
- AWS Shield - Provides detection and mitigation of DDoS attacks
- AWS Web Application Firewall - configurable web app for common exploitations

### Compute Services on AWS

#### Amazon EC2

OS and additional software are provided in a AMI (Amazon machine image)
Resources are provided by instance type
Instances can store data in two ways
- Instance store
  - only available while instance is running
- Elastic Block Store (EBS)
  - persistent storage

Types 
- General Purpose
- Comput, Memory, and Storage
- Accelerated computing

Scaling
- Vertical Scaling - some down time
- Horizontal Scaling - launch instances to help scaling
  - Auto-Scaling Group - 
    - set of EC2 instances
    - Min/Max # of instances
    - Health checks on each instance
    - Scaling policies that define scaling behavior
    - Exists within 1 or more availability zones in a single region
  - Elastic Load Balancer

#### AWS Lambda

