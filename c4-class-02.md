# Code 401 - Read 02

## Revision

1. What’s the difference between PUT and PATCH?
Both of them are http verbs that modifies the server's resources.
*PUT* replaces the entire resource with the new request body. So if a partial update was intended, the request body should contain all the fields along with the updates. Otherwise, the request will replace the entire resource with the new edits only.
*PATCH* can be used for partial updates without modifying the other fields.

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server:
[Stoplight](https://stoplight.io/), [Mocky](https://designer.mocky.io/), [MockServer](https://www.mock-server.com/)

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

    **Swagger** is a specification (set of rules) for a format describing REST APIs. The format is both machine-readable and human-readable. Swagger HTTP status code descriptions:

* *200* - OK
* *400* - Bad request. User ID must be an integer and larger than 0.
* *401* - Authorization information is missing or invalid.
* *404* - A user with the specified ID was not found.
* *5XX* - Unexpected error.

    **APIDoc.js** is an API documentation generator. APIDoc.js HTTP status code descriptions:

* *200* - Successful request and response
* *400* - Malformed parameters or other bad request.

4. Compare and contrast SOAP and ReST:

SOAP - Simple Object Access Protocol, its a protocol that was designed to ensure that programs built on different platforms and programming languages could exchange data in an easy manner. SOAP passes data in XML format.

ReST - Representational State Transfer, it is an architectural pattern for exchanging data between the client and server. REST permits data mostly in a JSON format, but can use plain text, HTML, XML, etc. A web service can be treated as a RESTful service if it follows the constraints of being
a Stateless, cacheable client Server with a layered system and a uniform interface. A ReSTful web server can use SOAP as its underlying protocol for web services.

## Terms Documentation

* Web Server - a computing system that stores, processes, and delivers resources for the web.

* Express - a backend web application framework for Node.js, designed for building web apps and APIs.

* Routing - a mechanism where HTTP requests are being sent to the code that handles them.

* WRRC - Web Request/Response Cycle, the cycle describes how web apps actually works: server contain all the required resources, clients need some of them to show web pages, so clients requests resources from the servers and the servers process those requests and send responses.  

## Preview

* Which 3 things had you heard about previously and now have better clarity on? continuous integration, testing with jest, and throwing errors.
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo? routing, middlewares, and error handling.
* What are you most excited about trying to implement or see how it works? routing.