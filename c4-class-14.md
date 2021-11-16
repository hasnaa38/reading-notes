# Code 401 - Read 14

## Revision

* What’s the difference between a FIFO and a standard queue?

Standard queues guarantee that a message is delivered at least once. Duplicates can be introduced into the queue.
FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing: they ensure a message is delivered exactly once and remains available until a consumer processes and deletes it. They also provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.

* How can the server be assured a message was properly received?

It waits for an acknowledgment or a received event from the client.

* What classic design pattern is best represented by event driven programming?

The observer pattern, which is a pattern in which the server maintains a list of its dependents, and will keep notifying them automatically of any state changes, usually by calling one of their methods.

* How do you test an event driven system?

By emitting events and checking the results.

## Terms Documentation

* **FIFO Queue**: a queue that operates on a first-in, first-out (FIFO) principle. This means that the request is processed in the order in which it arrives. FIFO queues can be used for storing messages in transit between application components. FIFO queues are designed to ensure that the order in which messages are sent and received is strictly preserved and that each message is processed exactly once.

* **Pub/Sub**: an architectural design pattern that provides a framework for exchanging messages (events) between publishers and subscribers. This pattern involves the publisher and the subscriber relying on a message broker that relays messages from the publisher to the subscribers. The host (publisher) publishes messages (events) to a channel that subscribers can then sign up to.
[more](https://cloud.google.com/pubsub/docs/overview)

## Preview - SQS and SNS

Simple Queue Service *SQS* is a fully managed message queuing service. Using SQS, you can send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available. Messages are not pushed to receivers, receivers have to poll or pull messages from it. Messages can't be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.

Simple Notification Service *SNS* is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. Messages are pushed to subscribers as and when they are sent by publishers to SNS (immediately), unlike in SQS where polling inherently introduces some latency in message delivery.

![sqsVSsns](https://res.cloudinary.com/practicaldev/image/fetch/s--mQKEdtHk--/c_limit,f_auto,fl_progressive,q_80,w_880/https://dw71fyauz7yz9.cloudfront.net/video-upload__c8bc44f83cd41222de8ae55b55c63ef2/thumbs-video-upload__c8bc44f83cd41222de8ae55b55c63ef2-00001.png)