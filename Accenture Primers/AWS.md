Public Cloud → Application is hosted completely on the cloud.
Hybrid → Mix of cloud + on‑prem.
On‑prem → Entirely local servers.
Private → Dedicated cloud for one organization, not fully public.

- **Infrastructure as a Service (IaaS)** →  provides virtualized computing resources.
- **Platform as a Service (PaaS)** →  provides development platforms and tools.
- **Software as a Service (SaaS)** →  delivers software applications over the internet.
- **CaaS (Containers as a Service)** → Focuses on container orchestration; OS is abstracted.

#### Cloud Service:
Cloud computing means using **remote servers on the internet** to
- Store data
- Run applications
- Process information
- Host websites
#### 🚀 Key Features of AWS

1. Pay-as-You-Go Pricing
	1. Pay only for what you use
	2. No upfront hardware cost
2. Scalability
	1. Increase or decrease resources anytime
	2. Handles traffic spikes easily
3. Global Infrastructure
	1. Data centers in many countries
	2. Faster performance worldwide
4. High Security
	1. Data encryption
	2. Firewalls & access control
	3. Compliance with global standards
5. Reliability
	1. Backup systems
	2. High availability
	3. Disaster recovery options

#### Major AWS Services:
1. Compute
	1. EC2 – Virtual servers
	2. Lambda – Run code without servers (serverless)
 2. Storage
	1. S3 – Object storage
	2. EBS – Disk storage for servers
3. Databases
	1. RDS – Relational databases
	2. DynamoDB – NoSQL database
 4. Networking
	1. VPC – Private network
	2. CloudFront – Content delivery
 5. AI & Analytics
	1. SageMaker – Machine learning
	2. Athena – Data analysis

#### Clouding Computing Model:

IaaS
PaaS
SaaS

#### Cloud Deployment Models:

On-Premises
Public Cloud
Hybrid 

#### Benefits:
1. Capital 
2. Pay as you go 
3. Scale advantage
4. Capacity/Scalability
5. Speed & Agility
6. Focus Advantage
7. Easy Global Deployment
8. Less Latency as Regional Centers

Availability Zones
Region Selection 
Edge Locations - Caching
### AWS Management interfaces:
1. **AWS CLI** → Valid interface, command-line tool to manage AWS.
2. **AWS Management Console** → Valid interface, web-based GUI.
3. **AWS SDK** → Valid interface, provides APIs for programming languages.

- **Region** → An AWS Region is a geographic area that contains multiple Availability Zones, each made up of one or more data centers.
- **Origin** → Refers to the source server for content delivery (e.g., CloudFront), not data centers.
- **Availability Zone** → A single or group of data centers within a region, but the option “consists of one or more data centers at a broader level refers to **Region**.
---
#### AWS S3:
Amazon S3  - 
- object level storage
- 5 tb single object size - unlimited storage
- 99.99% durable
- granular access to bucket & object
- Event triggers
- Bucket Folder object

Amazon S3 access control  
- Default
- public 
- Access policy
Amazon S3 bucket properties  
- Transfer Acceleration  Object Lock  Requester pays  Static Website Hosting
- Bucket Versioning  Sever Access Logging  Tags  Event Notifications  Encryption

S3 common Usage
- 1  2  3  4  Backup and Storage  Website Hosting  Media Hosting  Software Delivery

Amazon S3 glacier
- Low cost data archival  
- Long term backup  
- Retrieval Options
	- Standard 3 to 5 hours  
	- Bulk 5 to 12 hours  
	- Expedited 1-5 minutes
- Glacier Archive & Vaults:
- An archive is any object such as a photo, video or document.
- A vault is a container for storing archives.
- AMAZON S3 Storage Classes


---

#### AWS Cloud:

- Amazon EC2  
	- » Application Server  » Web Server  » Game Server  » Mail Server  » File Server  » Proxy Server  » Gateway Server  » Media Server
	- Benefits:
- Amazon EC2 instance Types  
- Amazon Machine Images (AMI)  
- Amazon Elastic Block Store (EBS)
---
#### Virtual Private Cloud

- A VPC is a virtual network dedicated to an AWS account  
- Requires IPv4 address space ( IPv6 address range optional) 
- Creates specific CIDR range for your resources  
- Strict access rules for inbound and outbound traffic

- VPC & Subnets
- Route Table
- Internet Gateway
- NAT Gateway
- Elastic IP addresses
- Elastic Network Interfaces
- Security Groups
- Network ACLs

##### Monitoring & Autoscaling
- AMAZON Cloudwatch
- Elastic Load Balancer
- Application load Balancer
- Network Load Balancer

###### AMAZON Databases:

---
Deployment:

Automate Deployment

AWS CloudFormation
AWS Elastic Beansalk 
AWS Direct Connect
AWS lambda
Amazon EFS
Amazon SNS
Amazon CloudFront

---
#### Security & Compliance
- ₪ AWS Artifact  ₪ AWS Certificate Manager  ₪ Amazon Cloud Directory  ₪ AWS CloudHSM  ₪ Amazon Cognito  ₪ AWS Firewall Manager  ₪ Amazon Guard Duty  ₪ AWS IAM  ₪ Amazon Inspector  ₪ AWS KMS  ₪ AWS Organizations  ₪ AWS Shield  ₪ AWS Secrets Manager  ₪ AWS Single Sign-On  ₪ AWS WAF

- Explain Security shared responsibility model in AWS  
- Explain Authentication and Authorization  
- Describe security and compliance  
- Describe DDoS mitigation
- 


---

AWS WAF:

- WAF
- 6 pillars of WAF
- WAF tool
---
#### Pricing Models & Application Support
- AWS Pricing 
- AWS Cost Estimation Tool
- Pricing Concepts
- EC2 Pricing Models
- AWS Free Tier
- AWS Price Calc
- AWS Cost Explorer
- Trusted Advisor
- AWS Support