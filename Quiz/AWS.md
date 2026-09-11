
---
- **Hybrid deployment model** → Used when maintaining **legacy applications on premises**.
- **AWS global footprint** → Enables worldwide deployment → **True**.
- **One or more data centres** → **Region**.
- **AWS start offering IT infrastructure services** → **2006**.
- **Cloud computing definition** → On-demand, pay-as-you-go → **True**.
- **S3 hosting** → Only supports **Static Websites**.
- **S3 bucket default** → **Private**.
- **General purpose instance type** → **t2.micro**.
- **S3 storage type** → **Object Storage**.
- **Performance-sensitive storage class** → **S3 Standard**.
- **Multiple object variants in bucket** → **Versioning**.
- **Storage class in one Availability Zone** → **S3 One Zone**.
- **Service to create virtual machines** → **Amazon EC2**.
- **S3 bucket supports versioning** → **True**.
- **Maximum single object size in S3** → **5 TB**.
---


- **Amazon EC2 Instances utilize Intel® Xeon® processors** → **True**
- **Valid EC2 instance type** → **t2.micro**
- **AMI stands for** → **Amazon Machine Image**
- **Master image for creating EC2 instances** → **AMI**
- **Different types of EC2 instances** → **Compute Optimized, Storage Optimized, General Purpose**
- **Custom AMI can include applications** → **True**
- **EC2 instance type for compute-intensive workloads** → **Compute Optimized**
- **EBS volume attached to multiple instances at once** → **False**
- **Resize EBS volume on running EC2 instance** → **Without downtime**
- **Virtual server platform for creating/running VMs on AWS** → **EC2**

---

- **Monitoring resources helps in** → **Identify the unusual activities/optimize usage**
- **Database service that is key‑value pair or document database** → **Amazon DynamoDB**
- **AWS DynamoDB is a serverless NoSQL database** → **True**
- **Entity used for temporary access to resources** → **Role**
- **Database service compatible with PostgreSQL and MySQL** → **Amazon Aurora**
- **Manual scaling in EC2 Auto Scaling is done by** → **Adjusting Desired capacity**
- **CloudWatch component for creating and managing custom alarms** → **CloudWatch Alarms**
- **NOT a benefit of Amazon CloudWatch** → **Automated resource provisioning**
- **Service used for monitoring resources in AWS** → **Amazon CloudWatch**
- **AutoScaling increases/decreases the capacity of an EC2 instance automatically** → **True**

---
- **Shared storage for Linux workloads** → **Amazon EFS**
- **Database service supporting dynamic schema** → **Amazon DynamoDB**
- **CloudWatch can monitor custom metrics in addition to built‑in metrics** → **True**
- **Load balancer supporting content‑based routing** → **Application Load Balancer**
- **Infrastructure automation service** → **Amazon CloudFormation**
- **Messaging service based on pub/sub model** → **Amazon SNS**
- **Serverless computing service** → **Amazon Lambda**
- **AWS service for configuring CDN** → **Amazon CloudFront**
- **Service enabling asynchronous communication between services** → **Amazon SQS**
- **Serverless container orchestration service** → **AWS Fargate**

----
- **Permissions management** → Use **Groups** to simplify assigning similar permissions to many users.
- **Resource organization** → Use **Resource Groups** to organize and manage AWS resources.
- **Security best practices** → Avoid using the **root account** for daily activities; instead, remove unnecessary users, use roles, and grant least privilege.
- **Additional security layer** → **Multifactor Authentication (MFA)** adds protection beyond credentials.
- **Managed service (database)** → **Amazon RDS/S3** is the managed database service.
- **Shared responsibility model** → Customers secure what they deploy, while **AWS secures the global infrastructure**.
- **Access control** → **Amazon IAM** controls access to services and resources.
- **Single Sign-On (SSO)** → Enables authentication into multiple applications with one set of credentials.
- **AWS user** → A person or workload that uses AWS resources.
---
Here’s a **summary of the Security and Compliance – PostQuiz review page** you’re viewing:

### Key Takeaways (Score: 10/10 ✅)

1. **AWS IAM** → Primary purpose is **controlling access to AWS resources**.
2. **AWS Shield** → Protects applications against **DDoS attacks**.
3. **IAM Role** → Allows **temporary access** to AWS resources.
4. **AWS Artifact** → Provides access to **security and compliance documents**.
5. **AWS Inspector** → Used for **automated security assessments**.
6. **Shared Responsibility Model** → AWS is responsible for securing the **global infrastructure** → **True**.
7. **Permission Boundary** → Used to set **maximum permissions** for a user.
8. **IAM Roles for EC2** → Benefit: **Secure access to AWS services without storing credentials**.
9. **IAM Best Practices** → Delete **root user access keys** and enable **MFA**.
10. **IAM Policies** → Can be attached to **users, groups, and roles**.

📌 **Overall insight**: The quiz reinforces AWS’s **shared responsibility model**, highlights **IAM as the cornerstone of access control**, and emphasizes **security best practices** like MFA and avoiding root credentials.

---

Here’s a **summary of your current page (AWS Cloud Architecture Design Principles – PreQuiz)**:

### Key Points from the PreQuiz

1. **IAM (Identity and Access Management)** → Belongs to the **Security pillar** of the Well‑Architected Framework.
2. **Well‑Architected Framework** → Built on **5 pillars**: Security, Reliability, Performance Efficiency, Cost Optimization, and Operational Excellence.
3. **Security pillar** → Ensures information, systems, and assets are adequately protected.
4. **Reliability pillar** → Responsible for **automatic recovery** of workloads.
5. **Operational Excellence pillar** → Focuses on **streamlining operations** and continuous improvement.
6. **Cost Optimization pillar** → Best practice is to **regularly review and modify resources** to avoid waste.
7. **Performance Efficiency pillar** → Ensures high performance by using resources efficiently.
8. **AWS WAF** → Protects web applications from exploits (not for infrastructure review).
9. **Well‑Architected Framework purpose** → Helps build **secure, high‑performing, resilient, and efficient infrastructure**.
10. **On‑demand access** → Provides best practices developed by AWS architects.

📌 **Overall insight**: The PreQuiz reinforces the **five pillars of the Well‑Architected Framework**, mapping AWS services like IAM and WAF to their respective pillars, and highlights best practices for **security, reliability, cost optimization, and operational excellence**.

---
Here’s a **summary of your current page (AWS Cloud Architecture Design – PostQuiz)**:

### Key Takeaways from the PostQuiz

1. **Well‑Architected Framework Pillars**
    
    - Security → Protects data, systems, and assets.
    - Reliability → Ensures recovery from failures and meeting customer demands.
    - Performance Efficiency → Maximizes performance with AWS resources.
    - Cost Optimization → Minimizes costs while balancing other factors.
    - Operational Excellence → Streamlines operations, monitoring, and continuous improvement.
2. **Service Mapping**
    
    - **AWS IAM** → Security pillar.
    - **Amazon Transcribe** → Converts speech to text.
    - **AWS Snowcone** → Small, rugged, secure edge computing and data transfer device.
    - **AWS Well‑Architected Tool** → Provides plans and guidance using AWS best practices.
3. **Best Practices**
    
    - Cost Optimization → Turn off unused/underutilized resources; regularly review and modify usage.
    - Operational Excellence → Combination of processes, monitoring, and continuous improvement.
    - Reliability → Focuses on resilience and recovery.
    - Security → Identity management, protection, monitoring.
    - Performance Efficiency → Efficient resource utilization and scaling.

📌 **Overall insight**: The PostQuiz reinforces the **five pillars of the AWS Well‑Architected Framework**, connects AWS services (IAM, Transcribe, Snowcone, WAF) to their respective pillars, and highlights best practices for **cost control, resilience, security, and operational improvement**.

---
Here’s a **summary of your current page (AWS: Billing and Pricing – PreQuiz)**:

### Key Points from the PreQuiz

1. **Amazon EBS Pricing**
    
    - Includes **Volume**, **Data Transfer, and **Snapshot**.
    - **Data Transfer** is billed separately under networking, not part of EBS pricing.
2. **EC2 Pricing Models**
    
    - **On‑Demand** → Pay per hour/second, flexible but costlier.
    - **Reserved** → Lower cost with 1–3 year commitment.
    - **Savings Plan** → Flexible commitment with discounts.
    - **Spot** → Cheapest option, uses spare capacity but can be interrupted.
3. **AWS Free Tier**
    
    - Available for **12 months** after account creation.
4. **Tenancy Models**
    
    - **Shared** → Least expensive.
    - **Dedicated Instance** → More costly, hardware dedicated but not tied to a specific server.
    - **Dedicated Host** → Most expensive, entire physical server dedicated.
    - **Shadow** → Not an AWS model.
5. **Cost Factors**
    
    - Costs **vary between regions** (True).
    - In AWS, you **do not need to buy servers** to host applications (False).
    - Pricing models are designed to help customers achieve **Cost Saving**.
6. **AWS Budgets Integration**
    
    - Closely integrated with **AWS Cost Explorer** for cost and usage data.

📌 **Overall insight**: The PreQuiz emphasizes AWS pricing fundamentals — Free Tier duration, EC2 pricing models, EBS cost factors, tenancy models, and the importance of regional cost variation. It highlights how AWS pricing options and tools (like Cost Explorer) help customers **optimize costs and avoid unnecessary expenses**.

---
Here’s a **summary of your current page (AWS: Billing and Pricing – PostQuiz)**:

### Key Points from the PostQuiz

1. **EC2 Pricing**
    
    - **Spot Instances** → Cheapest option, up to 90% off On‑Demand.
    - **Reserved Instances** → Best for consistent workloads.
    - **On‑Demand** → Flexible but costlier.
    - **Dedicated Hosts** → Most expensive tenancy model, supports existing server‑bound licenses.
2. **EBS Pricing**
    
    - Based on **Volume**, **Data Stored**, and **Snapshots**.
    - **Data Transfer** billed separately.
3. **S3 Pricing**
    
    - Determined by **Storage**, **Requests & Retrievals**, and **Data Transfer**.
    - **Versioning** increases storage but not a separate pricing factor.
4. **AWS Tools**
    
    - **Cost Explorer** → Analyze usage, traffic, and spending.
    - **Simple Monthly Calculator** → Estimate monthly costs.
    - **TCO Calculator** → Compare AWS vs. on‑premises costs.
    - **AWS Budgets** → Integrated with Cost Explorer for tracking.
5. **Cloud Pricing Models**
    
    - Classified into **Pay‑as‑Use**, **Subscription Based**, and **Hybrid**.
    - Goal: **Cost Saving** for customers.
6. **Tenancy Models**
    
    - **Shared** → Least expensive.
    - **Dedicated Instance** → More costly, hardware dedicated but not tied to a specific server.
    - **Dedicated Host** → Most expensive, entire physical server dedicated.
7. **Other Key Points**
    
    - AWS Free Tier → Valid for **12 months**.
    - Costs vary by **Region**.
    - **Organizations** → Centrally manage multiple AWS accounts.

📌 **Overall insight**: The PostQuiz reinforces AWS pricing fundamentals — EC2, EBS, and S3 pricing factors, tenancy models, and the role of AWS tools (Cost Explorer, Budgets, Calculators). It emphasizes how AWS pricing models are designed to **optimize costs, provide flexibility, and support compliance needs**.

