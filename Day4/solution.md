# 🎯 Tasks for Day 4

---

# Task 1

# AWS RDS, DynamoDB & AWS Lambda

## 1. AWS RDS (Relational Database Service)

### What is AWS RDS?

AWS RDS is a managed relational database service provided by Amazon Web Services.

AWS RDS allows you to run databases like MySQL and PostgreSQL on AWS without managing all the underlying server maintenance yourself.

### Supported Database Engines

AWS RDS supports several database engines:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Amazon Aurora

### How Does AWS RDS Work?

Suppose you are developing an e-commerce application.

Your application needs to store:

- Customer details
- Product information
- Orders
- Payment records

You can create an RDS database and connect your application to it.

The application sends SQL queries to RDS to store and retrieve information.

### Practical Example

Imagine you have a Java Spring Boot application running on an EC2 instance.

You can:

1. Create an RDS MySQL database.
2. Configure the database username and password.
3. Allow the EC2 instance to access RDS through security groups.
4. Configure your Spring Boot application with the RDS endpoint.
5. Start storing application data in RDS.

**Important:** RDS is a managed database service, but you are still responsible for database configuration, access management, and many database-level tasks.

---

## 2. AWS DynamoDB (NoSQL Database)

### What is AWS DynamoDB?

Amazon DynamoDB is a fully managed NoSQL database service provided by AWS.

DynamoDB is a database that stores data without requiring a traditional relational table structure with fixed columns and relationships.

### Important Concepts

1. **Table:** A collection of items.
2. **Item:** An individual record in a table.
3. **Attribute:** A property of an item, such as Name, Age, or UserID.
4. **Partition Key:** An attribute used to determine where an item is stored.
5. **Sort Key:** An optional attribute used to organize items with the same partition key.

### Practical Example

Suppose you are developing a food delivery application.

You need to store:

- User information
- Restaurant information
- Order status
- Delivery tracking information

DynamoDB can store and retrieve this information quickly.

For example, whenever a customer checks an order's delivery status, the application can retrieve the latest status from DynamoDB.

---

## 3. AWS Lambda (Serverless Computing)

### What is AWS Lambda?

AWS Lambda is a serverless computing service provided by AWS.

It allows you to run your code without provisioning or managing servers.

**In simple words:**

AWS Lambda executes your code automatically when a particular event occurs. You don't need to manage the underlying server.

### How Does AWS Lambda Work?

Lambda follows an event-driven execution model.

**Example:**

Suppose a user uploads an image to an S3 bucket.

The process works like this:

1. A user uploads an image to S3.
2. S3 generates an event.
3. The event triggers an AWS Lambda function.
4. Lambda executes your code.
5. Your code resizes the image and saves the processed image.

You don't need to keep an EC2 server running for this task.

### Practical Example

Suppose you have an application that sends an email whenever a customer places an order.

You can use:

- **DynamoDB:** To store order information.
- **AWS Lambda:** To execute the order-processing logic.
- **Amazon SES:** To send the email.

When a new order is created, an event can trigger Lambda to process it.

---

## Conclusion

| AWS Service | Purpose | Example |
|---|---|---|
| AWS RDS | Relational Database | MySQL, PostgreSQL |
| DynamoDB | NoSQL Database | Order status, user sessions |
| AWS Lambda | Serverless Computing | Image processing, automation |

These three AWS services help developers build scalable and reliable cloud applications.

---

