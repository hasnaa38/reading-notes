# Code 401 - Read 17

## Revision

* Describe “The Cloud”

The cloud is all of the things we can access remotely over the Internet. When something is in the cloud, it means it's stored on Internet servers instead of a computer's hard drive.

* What is a container (as it relates to computers and servers)?

A standard unit of software that packages all of the necessary elements and dependencies so that an application can run quickly and reliably in any environment. In this way, containers virtualize the operating system and run anywhere, from a private data center to the public cloud or even on a developer's personal laptop.

[resource](https://cloud.google.com/learn/what-are-containers)

* What is auto-scaling?

A cloud computing technique for dynamically allocating computational resources depending on the load to a server farm or pool. It enables organizations to scale cloud services such as server capacities or virtual machines up or down automatically, based on defined situations such as traffic ir utilization levels.

[resource](https://avinetworks.com/glossary/auto-scaling/)

* What is bandwidth?

The transmission rate of data across a network measured in bits per second. It represents the capacity of network connection. The minimum bandwidth requirement for Cloud Computing is 80kbps per user.

* How do cloud providers compute service costs?

To set a price, cloud providers determine the expense to maintaining the network. They start by calculating costs for network hardware, network infrastructure maintenance, and labor. These expenses are added together and then divided by the number of rack units a business will need for its cloud.

[resource](https://expedient.com/knowledgebase/blog/2015-05-01-how-the-cost-of-cloud-computing-is-calculated/)

## Terms Documentation

* **Server Instances**: a virtual machine (server) which runs a workloads in the cloud.

* **Containers**: a standard unit of software that packages all of the necessary elements and dependencies so that an application can run quickly and reliably in any environment.

* **Cloud Services**: the infrastructure, platforms, or software that are hosted by third-party providers and made available to users through the internet.

* **Cloud Architecture**: the architecture that defines the technology components that are combined to build a cloud, where resources are pooled through virtualization technology and shared across a network.

* **AWS**: a cloud computing platform provided by Amazon that offers an organization tools such as compute power, database storage and content delivery services. It includes a mixture of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.

* **EC2/Beanstalk vs Heroku**: both are cloud services used for deploying, monitoring, and scaling web applications and services. Both have comparable features and pricing, but one big difference is that Heroku’s pricing takes exponential price jumps as one adds common additional features, where-as AWS pricing is fairly linear. On the other hand, Heroku is generally simpler to get up and running as AWS has a fairly steep initial learning curve.

[resource](https://rubygarage.org/blog/heroku-vs-amazon-web-services)

## Preview - AWS: S3 and Lambda

### AWS S3

Amazon S3 has a simple web services interface that you can use . It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites.

Amazon Simple Storage Service (Amazon S3) - an object storage service to to store, protect, and retrieve any amount of data, at any time, from anywhere on the web. It offers high scalability, data availability, security, and performance. It also provides management features so that developers can optimize, organize, and configure access to their data to meet their specific business, organizational, and compliance requirements.

### AWS Lambda Basics

It is a compute service that lets developers run code without provisioning or managing servers. Lambda runs your code on a high-availability compute infrastructure and performs all of the administration of the compute resources, including server and operating system maintenance, capacity provisioning and automatic scaling, code monitoring and logging. In short, Lambda allows running code for virtually any type of application or backend service just by writing code in one of the languages that Lambda supports.

### AWS Lambda Functions

A function is a resource that can be invoked to run a code in Lambda. A function has code to process the events passed into the function or that other AWS services send to the function.

### CDN

Content Delivery Network (CDN) - a geographically distributed group of servers which work together to provide fast delivery of Internet content. CDNs cache content such as videos, when a user requests some content, the CDN routes the request to the edge location that provides the lowest latency. If the content is already cached in that edge location, the CDN delivers it immediately. If the content is not currently in that edge location, the CDN retrieves it from your origin, and distributes it to the user.
