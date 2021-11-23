# Code 401 - Read 19

## Revision

* Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server

Both have the ability to test and run RESTful CRUD operations

* List the AWS Database offerings and talk about the pros and cons of each:

    1. Purpose Built
    2. Performance at Scale
    3. Fully Managed
    4. Secure & Highly Available

    pros and cons: [source](https://matthewbonig.com/2019/06/28/dynamodb-pros-cons/)

* What’s the difference between a FIFO and a standard queue?

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing, also they ensure that the order in which messages are sent and received is strictly preserved

* How can the server be assured a message was properly received?

Listening for a received event from the client or using SQS to ensure message delivery

## Terms Documentation

* **Serverless API**: an API that is setup without permanent infrastructure. This doesn’t mean servers are no longer involved, rather, it means that servers are auto-created on a per-need basis to scale to the demands of your app.

[resource](https://nordicapis.com/the-benefits-of-a-serverless-api-backend/)

* **Triggers**: an event that starts the workflow and causes a program to be executed

* **Dynamo vs Mongo**: Both are NoSQL key-value databases

* **Dynamoose vs Mongoose**: both are modeling tools for DynamoDB/MongoDB

## Preview - AWS SQS vs SNS

### SQS

Simple Queue Service *SQS* is a fully managed message queuing service. Using SQS, you can send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available. Messages are not pushed to receivers, receivers have to poll or pull messages from it. Messages can't be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.

### SNS

Simple Notification Service *SNS* is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. Messages are pushed to subscribers as and when they are sent by publishers to SNS (immediately), unlike in SQS where polling inherently introduces some latency in message delivery.

![sqsVSsns](https://res.cloudinary.com/practicaldev/image/fetch/s--mQKEdtHk--/c_limit,f_auto,fl_progressive,q_80,w_880/https://dw71fyauz7yz9.cloudfront.net/video-upload__c8bc44f83cd41222de8ae55b55c63ef2/thumbs-video-upload__c8bc44f83cd41222de8ae55b55c63ef2-00001.png)
