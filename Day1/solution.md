# ☁️ AWS Day 1 – Cloud Computing Fundamentals

> Beginner-friendly notes covering AWS Pricing Models, Cloud Deployment Models, Cloud Service Models, and AWS History.

---

## 📚 Table of Contents

1. [AWS Pricing Models](#1-aws-pricing-models)
   - Pay-as-you-go
   - Reserved Instances
   - Spot Instances
2. [Compare Cloud Models](#2-compare-cloud-models)
   - On-Premises
   - Cloud
   - Hybrid Cloud
3. [Cloud Service Models](#3-cloud-service-models)
   - IaaS
   - PaaS
   - SaaS
4. [AWS History & Key Milestones](#4-aws-history--key-milestones)
5. [Important Interview Questions](#5-important-interview-questions)
6. [Day 1 Quick Revision](#6-day-1-quick-revision)

---

# 🎯 Tasks for Day 1

- Understand different AWS pricing models.
- Differentiate between On-Premises, Cloud, and Hybrid models.
- Learn about IaaS, PaaS, and SaaS with examples.
- Understand AWS history and important service launches.
- Learn why AWS became a leading cloud provider.

---

# 1. AWS Pricing Models

AWS (Amazon Web Services) offers different pricing models that help businesses reduce infrastructure costs and pay for the cloud resources they use.

For a **DevOps Engineer**, understanding AWS pricing is important because you need to select cost-effective resources while managing servers, storage, databases, and applications.

## 1.1 Pay-as-you-go Pricing Model

### Definition

Pay only for the resources you actually use. There is no need to make a long-term commitment or pay an upfront cost.

💡 **Real-world Example:**

It is similar to paying an electricity bill: the more electricity you consume, the more you pay.

### AWS Example

- You launch an AWS EC2 instance.
- You use it for 10 hours.
- You pay for those 10 hours of usage according to the instance's pricing.

### Advantages

- No long-term commitment.
- No upfront investment.
- Easy to scale resources up or down.
- Suitable for testing and development.

### Use Cases

- Development environments.
- Short-term projects.
- Applications with unpredictable workloads.

---

## 1.2 Reserved Instances (RI)

### Definition

You make a commitment to use a particular AWS resource for a longer period, generally **1 year or 3 years**, in exchange for discounted pricing.

### Example

Suppose:

- On-Demand EC2 cost = ₹10 per hour.
- You need the server continuously for one year.
- You purchase a Reserved Instance.
- AWS offers a discounted rate based on the commitment.

You can save money compared with On-Demand pricing.

### Advantages

- Lower costs than On-Demand in suitable cases.
- Predictable pricing.
- Suitable for workloads with consistent usage.

### Use Cases

- Production servers.
- Databases running continuously.
- Applications with predictable workloads.

---

## 1.3 Spot Instances

### Definition

Spot Instances allow you to use unused AWS EC2 capacity at significantly discounted prices.

However, AWS can interrupt your Spot Instance when it needs the capacity back.

### How Does It Work?

AWS has thousands of physical servers. Sometimes, many servers have unused capacity.

AWS offers this unused capacity to customers at lower prices through Spot Instances.

### Example

Suppose:

- On-Demand EC2 price = ₹10/hour.
- Spot Instance price = ₹3/hour.

You can save money by using Spot Instances.

However, AWS may interrupt your instance when capacity is needed.

### Advantages

- Significant cost savings.
- Useful for large-scale computing.
- Good for flexible workloads.

### Disadvantages

- Instances can be interrupted.
- Not suitable for applications that cannot tolerate interruptions.
- Requires interruption-handling mechanisms.

### Use Cases

- Batch processing.
- Data analysis.
- CI/CD build agents.
- Automated testing.
- Stateless application.

---

### 🎯 Interview Question

**Q. What is the difference between On-Demand, Reserved, and Spot Instances?**

**Answer:**

- On-Demand: Pay for the resources you use without long-term commitment.
- Reserved: Commit for a longer period to get discounted pricing.
- Spot: Use unused AWS capacity at a lower price, but instances can be interrupted.

---

# 2. Compare Cloud Models

There are three major infrastructure deployment models used by organizations:

1. On-Premises
2. Cloud
3. Hybrid Cloud

## 2.1 On-Premises Model

### Definition

On-premises means an organization manages and maintains its own IT infrastructure, including physical servers, storage, networking equipment, and security systems within its own premises.

### Example

A bank maintains its own data center to store customer information and run banking applications.

### Advantages

- Complete control over hardware and infrastructure.
- Greater control over data security and privacy.
- Customization according to business requirements.
- No dependency on an external cloud provider.

### Disadvantages

- High initial investment in hardware and software.
- Requires an IT team for maintenance.
- Scaling resources takes more time.
- Organization is responsible for backups and disaster recovery.

### When Is It Appropriate?

- Government organizations handling sensitive data.
- Banks and financial institutions.
- Organizations with strict security and compliance requirements.
- Enterprises that already have their own data centers.

---

## 2.2 Cloud Model

### Definition

Cloud computing means using computing resources such as servers, storage, databases, and networking over the internet instead of maintaining physical infrastructure.

These resources are provided by cloud service providers such as:

- AWS
- Microsoft Azure
- Google Cloud

### Example

A startup hosts its website on AWS EC2 instead of purchasing physical servers.

### Advantages

- Low initial investment.
- Pay-as-you-go pricing.
- Easy and fast scalability.
- Access resources from anywhere through the internet.
- Cloud provider manages the physical infrastructure.

### Disadvantages

- Dependency on internet connectivity.
- Less control over physical infrastructure.
- Ongoing subscription or usage costs.
- Potential security and compliance concerns if not configured properly.

### When Is It Appropriate?

- Startups and small businesses.
- Web and mobile application development.
- Companies with changing workloads.
- Businesses that need quick deployment and scalability.

---

## 2.3 Hybrid Cloud Model

### Definition

A hybrid cloud is a combination of on-premises infrastructure and cloud computing.

It allows organizations to use both environments and move data or applications between them when required.

### Example

A bank stores sensitive customer information in its private data center but hosts its website and less-sensitive applications on AWS.

### Advantages

- Combines the benefits of on-premises and cloud.
- Sensitive data can remain on private infrastructure.
- Provides flexibility and scalability.
- Helps organizations gradually migrate to the cloud.
- Supports disaster recovery and backup.

### Disadvantages

- Complex infrastructure management.
- Requires skilled IT professionals.
- Integration between systems can be difficult.
- Security management across multiple environments can be challenging.

### When Is It Appropriate?

- Large enterprises with existing data centers.
- Banks and financial institutions.
- Government projects with strict data requirements.
- Organizations migrating gradually from on-premises to cloud.

---

---

# 3. Cloud Service Models

There are three major cloud service models:

1. IaaS – Infrastructure as a Service
2. PaaS – Platform as a Service
3. SaaS – Software as a Service

The main difference between them is **how much responsibility the cloud provider manages and how much responsibility the customer manages**.

---

## 3.1 IaaS (Infrastructure as a Service)

### Definition

IaaS provides basic IT infrastructure such as virtual machines, storage, and networking over the internet.

The cloud provider manages:

- Physical hardware.
- Networking.
- Virtualization.

The customer manages:

- Operating system.
- Applications.
- Data.
- Configurations.

### Example

Suppose you want to host a Java application.

Instead of purchasing a physical server, you rent a virtual machine from AWS using EC2.

You install:

- Linux operating system.
- Java.
- Apache or Nginx.
- Your Java application.

AWS manages the physical server, but you manage the operating system and application.

### AWS Examples

#### 1. Amazon EC2 (Elastic Compute Cloud)

- Provides virtual machines.
- You can install Linux or Windows.
- You control CPU, RAM, storage, and OS configuration.
- Used for hosting applications and websites.

#### 2. Amazon EBS (Elastic Block Store)

- Provides block storage for EC2 instances.
- Stores application data and operating system files.
- You can increase storage according to requirements.

#### 3. Amazon VPC (Virtual Private Cloud)

- Provides an isolated virtual network.
- Allows you to configure subnets, route tables, and security groups.
- Helps control network communication.

### Advantages

- High control over infrastructure.
- Flexible resource configuration.
- Easy scalability.
- Pay-as-you-go pricing.

### When to Use IaaS?

- When you need control over the operating system.
- When hosting custom applications.
- When migrating existing servers to the cloud.
- When running Docker or Kubernetes workloads.

---

## 3.2 PaaS (Platform as a Service)

### Definition

PaaS provides a ready-to-use platform for developing, running, and deploying applications without managing the underlying infrastructure and operating system.

The cloud provider manages:

- Infrastructure.
- Operating system.
- Runtime environment.

Developers mainly focus on:

- Application code.
- Data.

### Example

Suppose you want to deploy a Spring Boot application.

With IaaS, you need to:

1. Create an EC2 instance.
2. Install Linux.
3. Install Java.
4. Configure the environment.
5. Deploy your application.

With PaaS, the provider manages much of this infrastructure and runtime work.

You mainly focus on writing and deploying your application.

### AWS Examples

#### 1. AWS Elastic Beanstalk

- Deploys applications without manually managing servers.
- Supports Java, Python, Node.js, PHP, and other platforms.
- Automatically manages provisioning, deployment, and application health monitoring.

#### 2. AWS Lambda

- Runs code without requiring you to manage servers.
- Automatically scales based on incoming requests or events.
- You pay based on execution and resource consumption.

> **Note:** Lambda is commonly classified as serverless computing and is often grouped with PaaS in introductory cloud-service comparisons. More precisely, it is FaaS (Function as a Service).

#### 3. AWS App Runner

- Deploys web applications and APIs from source code or container images.
- Automatically handles infrastructure provisioning, deployment, and scaling.
- Developers focus on application development.

### Advantages

- No need to manage physical servers.
- Faster application development.
- Less infrastructure management.
- Automatic scaling and deployment capabilities.

### When to Use PaaS?

- When developing web applications.
- When deploying APIs and microservices.
- When you want to focus on application development.
- When you don't want to manage operating systems and servers.

⭐ **Important Interview Point:**

In PaaS, the cloud provider manages the infrastructure, operating system, and runtime environment, while developers mainly focus on application development.

---

## 3.3 SaaS (Software as a Service)

### Definition

SaaS provides ready-to-use software applications over the internet.

Users don't need to install, manage, or maintain the underlying infrastructure or application platform.

The cloud provider manages almost everything, including:

- Servers.
- Operating systems.
- Application software.
- Updates and maintenance.
- Infrastructure security.

The customer simply uses the software through a web browser or application.

### Example

Suppose you want to send professional emails.

Instead of setting up your own email server, installing software, and managing storage, you can use Gmail.

Simply log in and start sending emails.

### AWS Examples

#### 1. Amazon QuickSight

- Cloud-based business intelligence service.
- Creates dashboards and visual reports.
- Helps organizations analyze business data.

#### 2. Amazon Connect

- Cloud-based contact center solution.
- Helps businesses manage customer calls and interactions.
- No need to build and maintain a traditional contact center infrastructure.

#### 3. Amazon Managed Grafana

- Managed visualization and monitoring service.
- Creates dashboards for application and infrastructure monitoring.
- AWS manages the underlying Grafana infrastructure.

### Other Real-World SaaS Examples

| Software | Purpose |
|---|---|
| Gmail | Email service |
| Microsoft 365 | Office applications |
| Salesforce | Customer Relationship Management (CRM) |

### Advantages

- No infrastructure management.
- Accessible through the internet.
- Automatic software updates.
- Subscription-based pricing.
- Easy to use.

### When to Use SaaS?

- When you need ready-made software.
- When you don't want to manage servers or applications.
- When businesses need email, CRM, or collaboration tools.
- When employees need access to software from different locations.

⭐ **Important Interview Point:**

In SaaS, the cloud provider manages the application and underlying infrastructure. The customer simply uses the ready-made software.

---

### ⭐ Easy Way to Remember

- **IaaS = Rent Infrastructure**
- **PaaS = Rent Platform**
- **SaaS = Use Software**

### 🎯 Interview Question

**Q. What is the difference between IaaS, PaaS, and SaaS?**

**Answer:**

IaaS provides basic infrastructure such as virtual machines, storage, and networking. PaaS provides a ready-to-use platform for developing and deploying applications. SaaS provides complete software applications that users can access over the internet.

---

# 4. AWS History & Key Milestones

## 4.1 What is AWS?

AWS (Amazon Web Services) is a cloud computing platform provided by Amazon.

It offers services such as:

- Computing.
- Storage.
- Databases.
- Networking.
- Security.
- Artificial Intelligence.
- Serverless Computing.

### When Did AWS Start?

AWS was publicly launched on **March 14, 2006**, with Amazon S3 as its first publicly launched cloud service.

Interestingly, Amazon had introduced Amazon Simple Queue Service (SQS) in preview in November 2004, before the public launch of AWS.

A few months after S3, Amazon introduced EC2, allowing customers to rent virtual servers over the internet.

---

## 4.2 Important AWS Service Launches

### 1. Amazon S3 (2006)

**Full Form:** Simple Storage Service

- Provides object storage.
- Used to store images, videos, documents, backups, and application data.

### 2. Amazon EC2 (2006)

**Full Form:** Elastic Compute Cloud

- Provides virtual machines.
- Used to host websites, applications, and databases.

### 3. AWS Lambda (2014)

- Runs code without managing servers.
- Automatically scales based on events and requests.
- Used for serverless applications and automation.

### 4. Amazon EKS (2017)

**Full Form:** Elastic Kubernetes Service

- Provides managed Kubernetes.
- Used to deploy and manage containerized applications.

### 5. Amazon Bedrock (2023)

- Provides access to foundation models.
- Used to build generative AI applications.

---

## 4.3 How Did AWS Become the No. 1 Cloud Provider?

AWS became the leading cloud infrastructure provider through several important factors.

### 1. Early Entry into Cloud Computing

AWS entered the public cloud market in 2006, giving it an early advantage over many competitors.

### 2. Wide Range of Services

AWS expanded from basic storage and computing into:

- Databases.
- Networking.
- Security.
- Analytics.
- Machine Learning.
- Artificial Intelligence.

### 3. Pay-as-you-go Pricing

Customers can pay for the resources they consume instead of investing heavily in physical servers.

### 4. Global Infrastructure

AWS expanded its global network of Regions and Availability Zones, helping businesses deploy applications closer to their customers.

### 5. Scalability and Reliability

AWS provides services that allow organizations to scale resources according to demand and build highly available applications.

### 6. Strong Customer and Partner Ecosystem

Startups, enterprises, developers, and technology partners helped expand AWS adoption.

---

## 4.4 Current Market Position

According to Synergy Research Group, AWS maintained its leading position in the global cloud infrastructure market in **Q2 2026**, with approximately 28% market share.

Its major competitors were:

| Cloud Provider | Market Share |
|---|---:|
| AWS | 28% |
| Microsoft Azure | 20% |
| Google Cloud | 15% |

> ⚠️ **Note:** These market-share figures are reproduced from the source notes. Verify the latest Synergy Research Group report before using them in a presentation or publication.

---

# 5. Important Interview Questions

### Q1. What is AWS?

**Answer:** AWS (Amazon Web Services) is a cloud computing platform provided by Amazon that offers services such as computing, storage, databases, networking, and security over the internet.

### Q2. What are the three major AWS pricing models covered in these notes?

**Answer:**
1. Pay-as-you-go.
2. Reserved Instances.
3. Spot Instances.

### Q3. What are Spot Instances?

**Answer:** Spot Instances allow users to access unused AWS EC2 capacity at discounted prices. However, AWS can interrupt them when it needs the capacity back.

### Q4. What are Reserved Instances?

**Answer:** Reserved Instances provide discounted pricing in exchange for a longer-term commitment, generally one or three years.

### Q5. What is the difference between Cloud and On-Premises?

**Answer:** On-Premises means an organization manages its own physical infrastructure, while Cloud means it uses computing resources provided by a cloud service provider over the internet.

### Q6. What is Hybrid Cloud?

**Answer:** Hybrid Cloud combines on-premises infrastructure and cloud computing, allowing organizations to use both environments.

### Q7. What are IaaS, PaaS, and SaaS?

**Answer:**
- IaaS: Infrastructure as a Service.
- PaaS: Platform as a Service.
- SaaS: Software as a Service.

### Q8. Give examples of AWS IaaS services.

**Answer:** Amazon EC2, Amazon EBS, and Amazon VPC.

### Q9. Give examples of AWS PaaS services.

**Answer:** AWS Elastic Beanstalk, AWS Lambda, and AWS App Runner.

### Q10. Give examples of AWS SaaS services.

**Answer:** Amazon QuickSight, Amazon Connect, and Amazon Managed Grafana.

### Q11. When was AWS publicly launched?

**Answer:** AWS was publicly launched on March 14, 2006, with Amazon S3.

### Q12. What is Amazon S3?

**Answer:** Amazon S3 (Simple Storage Service) is an object storage service used to store files such as images, videos, documents, backups, and application data.

### Q13. What is Amazon EC2?

**Answer:** Amazon EC2 (Elastic Compute Cloud) provides virtual machines that can be used to host applications, websites, and databases.

### Q14. What is AWS Lambda?

**Answer:** AWS Lambda is a serverless computing service that runs code without requiring users to manage servers.

### Q15. What is Amazon EKS?

**Answer:** Amazon EKS (Elastic Kubernetes Service) is a managed Kubernetes service used to deploy and manage containerized applications.

---

# 6. Day 1 Quick Revision

## AWS Pricing Models

| Model | Remember This |
|---|---|
| Pay-as-you-go | Pay for what you use |
| Reserved Instances | Long-term commitment for discounted pricing |
| Spot Instances | Use unused capacity at lower prices; can be interrupted |

## Cloud Deployment Models

| Model | Remember This |
|---|---|
| On-Premises | Own physical infrastructure |
| Cloud | Infrastructure provided by a cloud provider |
| Hybrid | Combination of On-Premises and Cloud |

## Cloud Service Models

| Model | Remember This | AWS Examples |
|---|---|---|
| IaaS | Infrastructure | EC2, EBS, VPC |
| PaaS | Application Platform | Elastic Beanstalk, Lambda, App Runner |
| SaaS | Ready-to-use Software | QuickSight, Connect, Managed Grafana |

## Important AWS Launches

| Year | AWS Service | Purpose |
|---|---|---|
| 2006 | Amazon S3 | Object Storage |
| 2006 | Amazon EC2 | Virtual Machines |
| 2014 | AWS Lambda | Serverless Computing |
| 2017 | Amazon EKS | Managed Kubernetes |
| 2023 | Amazon Bedrock | Generative AI Applications |

---

## ⭐ Most Important Points to Remember

1. **Pay-as-you-go:** Pay only for the resources you use.
2. **Reserved Instances:** Commit for a longer period to get discounted pricing.
3. **Spot Instances:** Use unused EC2 capacity at discounted prices, but interruptions are possible.
4. **On-Premises:** Organization manages its own physical infrastructure.
5. **Cloud:** Cloud provider provides computing resources over the internet.
6. **Hybrid Cloud:** Combination of On-Premises and Cloud.
7. **IaaS:** Customer manages the operating system and applications.
8. **PaaS:** Provider manages infrastructure and runtime; developers focus on code.
9. **SaaS:** Provider manages the software; customers use the ready-made application.
10. **AWS Public Launch:** March 14, 2006.
11. **Amazon S3:** Object Storage.
12. **Amazon EC2:** Virtual Machines.
13. **AWS Lambda:** Serverless Computing.
14. **Amazon EKS:** Managed Kubernetes.
15. **Amazon Bedrock:** Generative AI Applications.

---
