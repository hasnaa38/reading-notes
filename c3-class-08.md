# Code 301 - Read 08

In this file, a summary of **Read: Class 08 - APIs** will be provided.

[RESTful web API design](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

* What does REST stand for?

It is an architectural style for building web services.

* REST APIs are designed around resources. Resources can be any kind of object, data, or service that can be accessed by the client.

* What is an identifier of a resource? Give an example.

A URI that uniquely identifies that resource. Example: `http://localhost:8000/orders/1`.

* What are the most common HTTP verbs?

GET, POST, PUT, PATCH, and DELETE.

* What should the URIs be based on?

Resource, not HTTP verbs (operations performed on resources).

* Give an example of a good URI.

`http://localhost:8000/orders`

* What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

Web APIs that expose a large number of small resources, so they require a client application to send multiple requests to find all of the data that it requires.

* What status code does a successful GET request return?

200 (OK)

* What status code does an unsuccessful GET request return?

404 (Not Found).

* What status code does a successful POST request return?

201 (Created).

* What status code does a successful DELETE request return?

204 (No Content).
