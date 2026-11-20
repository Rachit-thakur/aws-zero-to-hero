# 🎯 Tasks for Day 1

1. **Understand AWS Pricing Models**
   - Learn about the different pricing models offered by AWS (Pay-as-you-go, Reserved Instances, Spot Instances, etc.).

AWS Pricing Models

AWS (Amazon Web Services) offers different pricing models that help businesses reduce infrastructure costs and pay for the cloud resources they use.

For a DevOps Engineer, understanding AWS pricing is important because you need to select cost-effective resources while managing servers, storage, databases, and applications.

Let's understand the different pricing models in simple language with practical examples and interview points.
1. Pay-as-you-go Pricing Model
Meaning: Pay only for the resources you actually use. There is no need to make a long-term commitment or pay an upfront cost.

It is similar to paying an electricity bill: the more electricity you consume, the more you pay.

Example:
- You launch an AWS EC2 instance.
- You use it for 10 hours.
- You pay for those 10 hours of usage (according to the instance's pricing).
Advantages:
- No long-term commitment.
- No upfront investment.
- Easy to scale resources up or down.
- Suitable for testing and development.
Use cases:
- Development environments.
- Short-term projects.
- Applications with unpredictable workloads.
Interview point: Pay-as-you-go means you pay only for the cloud resources you consume, without making a long-term commitment.
2. Reserved Instances (RI)
Meaning: You make a commitment to use a particular AWS resource for a longer period, generally 1 year or 3 years, in exchange for discounted pricing.

Example:

Suppose:
- On-demand EC2 cost = ₹10 per hour.
- You need the server continuously for one year.
- You purchase a Reserved Instance.
- AWS offers a discounted rate based on the commitment.
You can save money compared with On-Demand pricing.

Advantages:
- Lower costs than On-Demand in suitable cases.
- Predictable pricing.
- Suitable for workloads with consistent usage.
Use cases:
- Production servers.
- Databases running continuously.
- Applications with predictable workloads.
Important: Reserved Instances are primarily a billing discount model for EC2 and certain other AWS services. They are not necessarily physical servers reserved exclusively for you.
3. Spot Instances
Meaning: Spot Instances allow you to use unused AWS EC2 capacity at significantly discounted prices.

However, AWS can interrupt your Spot Instance when it needs the capacity back.

AWS has thousands of physical servers. Sometimes, many servers have unused capacity. AWS offers this unused capacity to customers at lower prices through Spot Instances.

Example:

Suppose:
- On-Demand EC2 price = ₹10/hour.
- Spot Instance price = ₹3/hour.
You can save money by using Spot Instances.

However, AWS may interrupt your instance when capacity is needed.

Advantages:
- Significant cost savings.
- Useful for large-scale computing.
- Good for flexible workloads.
Disadvantages:
- Instances can be interrupted.
- Not suitable for applications that cannot tolerate interruptions.
- Requires interruption-handling mechanisms.
Use cases:
- Batch processing.
- Data analysis.
- CI/CD build agents.
- Automated testing.
- Stateless applications.

---

**Compare Cloud Models**
   - Differentiate between **On-premises**, **Cloud**, and **Hybrid** models.  
   - Write when each model is most appropriate (e.g., startups, enterprises, government projects).

Compare Cloud Models: On-Premises, Cloud, and Hybrid
There are three major infrastructure deployment models used by organizations: On-Premises, Cloud, and Hybrid Cloud.
1. On-Premises Model
Definition:
On-premises means an organization manages and maintains its own IT infrastructure, including physical servers, storage, networking equipment, and security systems within its own premises.

Example: A bank maintains its own data center to store customer information and run banking applications.

Advantages:
- Complete control over hardware and infrastructure.
- Greater control over data security and privacy.
- Customization according to business requirements.
- No dependency on an external cloud provider.
Disadvantages:
- High initial investment in hardware and software.
- Requires an IT team for maintenance.
- Scaling resources takes more time.
- Organization is responsible for backups and disaster recovery.
When is it appropriate?
- Government organizations handling sensitive data.
- Banks and financial institutions.
- Organizations with strict security and compliance requirements.
- Enterprises that already have their own data centers.
2. Cloud Model
Definition:
Cloud computing means using computing resources such as servers, storage, databases, and networking over the internet instead of maintaining physical infrastructure.

These resources are provided by cloud service providers such as AWS, Microsoft Azure, and Google Cloud.

Example: A startup hosts its website on AWS EC2 instead of purchasing physical servers.

Advantages:
- Low initial investment.
- Pay-as-you-go pricing.
- Easy and fast scalability.
- Access resources from anywhere through the internet.
- Cloud provider manages the physical infrastructure.
Disadvantages:
- Dependency on internet connectivity.
- Less control over physical infrastructure.
- Ongoing subscription or usage costs.
- Potential security and compliance concerns if not configured properly.
When is it appropriate?
- Startups and small businesses.
- Web and mobile application development.
- Companies with changing workloads.
- Businesses that need quick deployment and scalability.
3. Hybrid Cloud Model
Definition:
A hybrid cloud is a combination of on-premises infrastructure and cloud computing. It allows organizations to use both environments and move data or applications between them when required.

Example: A bank stores sensitive customer information in its private data center but hosts its website and less-sensitive applications on AWS.

Advantages:
- Combines the benefits of on-premises and cloud.
- Sensitive data can remain on private infrastructure.
- Provides flexibility and scalability.
- Helps organizations gradually migrate to the cloud.
- Supports disaster recovery and backup.
Disadvantages:
- Complex infrastructure management.
- Requires skilled IT professionals.
- Integration between systems can be difficult.
- Security management across multiple environments can be challenging.
When is it appropriate?
- Large enterprises with existing data centers.
- Banks and financial institutions.
- Government projects with strict data requirements.
- Organizations migrating gradually from on-premises to cloud.

---

**Explore Service Models**
   - Learn about **IaaS**, **PaaS**, and **SaaS** with 2–3 examples for each.
   - Explain how AWS provides these services (e.g., EC2 = IaaS, Lambda = PaaS, WorkMail = SaaS).


Cloud computing provides services through the internet. These services are mainly divided into three models:
1. IaaS – Infrastructure as a Service
2. PaaS – Platform as a Service
3. SaaS – Software as a Service
The main difference between them is how much responsibility the cloud provider manages and how much responsibility the customer manages.

Let's understand each model with examples from AWS and real-world applications.
1. IaaS (Infrastructure as a Service)
Definition
IaaS provides basic IT infrastructure such as virtual machines, storage, and networking over the internet.

The cloud provider manages the physical hardware, networking, and virtualization, while the customer manages the operating system, applications, data, and configurations.
Example
Suppose you want to host a Java application.

Instead of purchasing a physical server, you rent a virtual machine from AWS using EC2.

You install:
- Linux operating system.
- Java.
- Apache or Nginx.
- Your Java application.
AWS manages the physical server, but you manage the operating system and application.
AWS Examples
1. Amazon EC2 (Elastic Compute Cloud)
- Provides virtual machines.
- You can install Linux or Windows.
- You control CPU, RAM, storage, and OS configuration.
- Used for hosting applications and websites.
2. Amazon EBS (Elastic Block Store)
- Provides block storage for EC2 instances.
- Stores application data and operating system files.
- You can increase storage according to requirements.
3. Amazon VPC (Virtual Private Cloud)
- Provides an isolated virtual network.
- Allows you to configure subnets, route tables, and security groups.
- Helps control network communication.
Advantages
- High control over infrastructure.
- Flexible resource configuration.
- Easy scalability.
- Pay-as-you-go pricing.
When to use IaaS?
- When you need control over the operating system.
- When hosting custom applications.
- When migrating existing servers to the cloud.
- When running Docker or Kubernetes workloads.
2. PaaS (Platform as a Service)
Definition
PaaS provides a ready-to-use platform for developing, running, and deploying applications without managing the underlying infrastructure and operating system.

The cloud provider manages the infrastructure, operating system, and runtime environment. Developers mainly focus on application code and data.
Example
Suppose you want to deploy a Spring Boot application.

With IaaS, you need to:
- Create an EC2 instance.
- Install Linux.
- Install Java.
- Configure the environment.
- Deploy your application.
With PaaS, the provider manages much of this infrastructure and runtime work.

You mainly focus on writing and deploying your application.
AWS Examples
1. AWS Elastic Beanstalk
- Deploys applications without manually managing servers.
- Supports Java, Python, Node.js, PHP, and other platforms.
- Automatically manages provisioning, deployment, and application health monitoring.
2. AWS Lambda
- Runs code without requiring you to manage servers.
- Automatically scales based on incoming requests or events.
- You pay based on execution and resource consumption.
Lambda is commonly classified as serverless computing and is often grouped with PaaS in introductory cloud-service comparisons. More precisely, it is FaaS (Function as a Service).

3. AWS App Runner
- Deploys web applications and APIs from source code or container images.
- Automatically handles infrastructure provisioning, deployment, and scaling.
- Developers focus on application development.
Advantages
- No need to manage physical servers.
- Faster application development.
- Less infrastructure management.
- Automatic scaling and deployment capabilities.
When to use PaaS?
- When developing web applications.
- When deploying APIs and microservices.
- When you want to focus on application development.
- When you don't want to manage operating systems and servers.
3. SaaS (Software as a Service)
Definition
SaaS provides ready-to-use software applications over the internet. Users don't need to install, manage, or maintain the underlying infrastructure or application platform.

The cloud provider manages almost everything, including:
- Servers
- Operating systems
- Application software
- Updates and maintenance
- Infrastructure security
The customer simply uses the software through a web browser or application.
Example
Suppose you want to send professional emails.

Instead of setting up your own email server, installing software, and managing storage, you can use Gmail.

Simply log in and start sending emails.
AWS Examples
1. Amazon QuickSight
- Cloud-based business intelligence service.
- Creates dashboards and visual reports.
- Helps organizations analyze business data.
2. Amazon Connect
- Cloud-based contact center solution.
- Helps businesses manage customer calls and interactions.
- No need to build and maintain a traditional contact center infrastructure.
3. Amazon Managed Grafana
- Managed visualization and monitoring service.
- Creates dashboards for application and infrastructure monitoring.
- AWS manages the underlying Grafana infrastructure.
Other Real-World SaaS Examples
- Gmail – Email service.
- Microsoft 365 – Office applications.
- Salesforce – Customer relationship management (CRM).
Advantages
- No infrastructure management.
- Accessible through the internet.
- Automatic software updates.
- Subscription-based pricing.
- Easy to use.
When to use SaaS?
- When you need ready-made software.
- When you don't want to manage servers or applications.
- When businesses need email, CRM, or collaboration tools.
- When employees need access to software from different locations.

---

*AWS History & Key Milestones**
   - Learn about the *evolution of AWS* — when it started, its major launches (like EC2, S3, Lambda, etc.), and how it became the #1 cloud provider.
   - Share 3–4 key milestones as a carousel or post on LinkedIn.

   AWS History & Key Milestones
1. What is AWS and When Did It Start?

AWS (Amazon Web Services) is a cloud computing platform provided by Amazon. It offers services such as computing, storage, databases, networking, security, artificial intelligence, and serverless computing.

AWS was publicly launched on March 14, 2006, with Amazon S3 as its first publicly launched cloud service.

Interestingly, Amazon had introduced Amazon Simple Queue Service (SQS) in preview in November 2004, before the public launch of AWS.

A few months after S3, Amazon introduced EC2, allowing customers to rent virtual servers over the internet.

Understanding Important Launches
1. Amazon S3 (2006)
- Full form: Simple Storage Service.
- Provides object storage.
- Used to store images, videos, documents, backups, and application data.
2. Amazon EC2 (2006)
- Full form: Elastic Compute Cloud.
- Provides virtual machines.
- Used to host websites, applications, and databases.
3. AWS Lambda (2014)
- Runs code without managing servers.
- Automatically scales based on events and requests.
- Used for serverless applications and automation.
4. Amazon EKS (2017)
- Full form: Elastic Kubernetes Service.
- Provides managed Kubernetes.
- Used to deploy and manage containerized applications.
5. Amazon Bedrock (2023)
- Provides access to foundation models.
- Used to build generative AI applications.

How Did AWS Become the No. 1 Cloud Provider?
AWS became the leading cloud infrastructure provider through several important factors.
1. Early Entry into Cloud Computing
AWS entered the public cloud market in 2006, giving it an early advantage over many competitors.
2. Wide Range of Services
AWS expanded from basic storage and computing into databases, networking, security, analytics, machine learning, and AI.
3. Pay-as-you-go Pricing
Customers can pay for the resources they consume instead of investing heavily in physical servers.
4. Global Infrastructure
AWS expanded its global network of Regions and Availability Zones, helping businesses deploy applications closer to their customers.
5. Scalability and Reliability
AWS provides services that allow organizations to scale resources according to demand and build highly available applications.
6. Strong Customer and Partner Ecosystem
Startups, enterprises, developers, and technology partners helped expand AWS adoption.
Current Market Position
According to Synergy Research Group, AWS maintained its leading position in the global cloud infrastructure market in Q2 2026, with approximately 28% market share.

Its major competitors were:
- Microsoft Azure: 20%
- Google Cloud: 15%

---