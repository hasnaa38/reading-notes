# Code 401 - Read 18

## Revision

* What are serverless functions?

Function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

* Describe how a CDN works:

They work by caching content in geographically distributed servers. When a user requests some content, the CDN routes the request to the edge location that provides the lowest latency. If the content is already cached in that edge location, the CDN delivers it immediately. If the content is not currently in that edge location, the CDN retrieves it from your origin, and distributes it to the user.

## Terms Documentation

* **Serverless Functions**: functions hosted and maintained on infrastructure by cloud computing companies.

* **Cloud Storage**: a way for storing data securely online so that it can be accessed anytime from any location and easily shared with those who are granted permission. Cloud storage also offers a way to back up data to facilitate recovery off-site.

* **CDN**: Content Delivery Network is a geographically distributed group of servers which work together to provide fast delivery of Internet content.

## Preview - AWS API Gateway, DynamoDB and Dynamoose

### AWS API Gateway

API Gateway is an AWS service for creating, publishing, maintaining, monitoring, and securing REST, HTTP, and WebSocket APIs at any scale. Developers can create APIs that access AWS or other web services, as well as data stored in the AWS cloud.

API Gateway creates RESTful APIs that:

1. Are HTTP-based.
2. Implement standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE.
3. Enable stateless client-server communication.

### AWS DynamoDB

Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-region replication, in-memory caching, and data export tools. It can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

### Dynamoose

Dynamoose is a modeling tool for Amazon’s DynamoDB that was heavily inspired by Mongoose.

Dynamoose key features:

1. Type safety
2. Supports high level API
3. Easy to use syntax
4. Ability to transform data before saving or retrieving documents
5. Strict data modeling (validation, required attributes, and more)
6. Support for DynamoDB Transactions
7. Powerful Conditional/Filtering Support
8. Callback & Promise support
