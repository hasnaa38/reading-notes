# Code 401 - Read 16

## Revision

* Describe the Web-Request-Response-Cycle:

The basis of all web interactions is requesting and receiving information between 2 parties: a client and a server. The way information flows through this system is known as the Web-Request-Response-Cycle or WRRC, in which clients send requests to servers asking for information. Upon receiving a request, servers send responses back to the client.

![wrrc](http://curriculum-content.s3.amazonaws.com/how-the-web-works/Image_17_ComputerServer.png)

[resource1](https://backend.turing.edu/module2/lessons/how_the_web_works_http), [resource2](https://medium.com/@jen_strong/the-request-response-cycle-of-the-web-1b7e206e9047)

* Explain what a “server” is, as it relates to the WRRC:

A server is a computing hardware or software that provides functionality for other programs or devices (called clients). Servers can provide various functionalities (services), such as sharing data or resources among multiple clients, or performing computation for a client.

Servers receives and reads HTTP requests from the clients then generates and sends an HTTP response to that request back to the client.

* What does it mean to “deploy” an application?

The process of the running an application on a server or device so it becomes available to end users.

[resource](https://xebia.com/blog/so-what-is-a-deployment-really/)

## Terms Documentation

* **Server**: a computing hardware or software that provides functionality/services for clients; such as sharing data or resources among multiple clients, or performing computation for a client.

* **Pub/Sub**: an architectural design pattern that provides a framework for exchanging messages (events) between publishers and subscribers. This pattern involves the publisher and the subscriber relying on a message broker that relays messages from the publisher to the subscribers. The host (publisher) publishes messages (events) to a channel that subscribers can then sign up to.
[more](https://cloud.google.com/pubsub/docs/overview)

* **WRRC**: the way information flows during web interactions, in which clients send requests to servers asking for information. Upon receiving a request, servers send responses back to the client.

## Preview - AWS: Cloud Servers

Amazon Web Services (AWS) is a cloud computing platform provided by Amazon that offers an organization tools such as compute power, database storage and content delivery services. It includes a mixture of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings. AWS is separated into more than 100 different services; each can be configured in different ways based on the user's needs. Users should be able to see configuration options and individual server maps for an AWS service.

### AWS EC2

Elastic Compute Cloud (EC2) is one of AWS services that provides secure, resizable compute capacity in the cloud. It is a basic virtual machine with customizable hardware components and an OS. The system allows developers to run applications various virtual computers on the public cloud.

EC2 greatly eases the process of scaling up or down, can be integrated into several other services, and comes with a plan where you only pay for how much you use it.

### AWS Elastic Beanstalk

It is an easy-to-use service provided by AWS for deploying, managing, and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. Developers simply upload their application to the AWS cloud, and then let the AWS Beanstalk provision and handle the deployment, from configuration, capacity provisioning, load balancing, auto-scaling, and health monitoring.
