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
