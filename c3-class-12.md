# Code 301 - Read 12

In this file, a summary of **Read: Class 12 - CRUD** will be provided.

## Status Codes Based On REST Methods

[Which HTTP Status Code to Use for Every CRUD App](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

In your own words, describe what each group of status code represents:

* 100’s =  it tells the client that the header part of its request has been received and the server will try to to comply and respond to its request.

* 200’s = *success codes* - they tell the client that its request was accepted.

* 300’s = *redirection codes* - they tell the client that the resource they are requesting is unavailable at the expected location anymore.

* 400’s = *client error codes* - they represent invalid requests a client sent to a server.

* 500’s = *server error codes* - they indicate problems with overwhelmed servers or unreachable servers behind proxies.

* What is a status code 202? its shown in the case of asynchronous processing of a request, and it means that the request has met all validation requirements at the time of sending.

* What is a status code 308? it is the *permanent redirect*, which tells the client not to use the current URL anymore and to use another URL to access the resource.

* What code would you use if an update didn’t return data to a client? 204 *no content*.

* What code would you use if a resource used to exist but no longer does? if we don’t know where it went: 410 *Gone*. If we do, 308 *permanent redirect*.

* What is the ‘Forbidden’ status code? 403 - the client has authorized or doesn't need to authorize itself, but still has no permissions to access the resource.
