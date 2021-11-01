# Code 401 - Read 03

## Revision

* Name 3 real world use cases where you’d want to change the request with custom middleware
Logger middleware that prints a simple log messages, a validation middleware that validates incoming cookies, a time stamper middleware that displays the timestamp of the HTTP request

* True or false: The route handler is middleware? True

* In what ways can a middleware function end the process and send data to the browser?
using next() or ending the request-response cycle by calling methods that implicitly call res.end such as res.end itself, res.send, res.render.

* At what point in the request lifecycle can you “inject” middleware?

In the middle of receiving a request and sending back a response, after creating the request and response object, since middlewares are used to process and manipulate this object. [source](https://iq.opengenus.org/middlewares-in-express/)

![middleware and wrrc](https://iq.opengenus.org/content/images/2019/08/Add-a-subheading--1-.png)

* What can cause express to error with “Request headers sent twice, cannot start a second response”
When several responses are being sent for the same request.

## Terms Documentation

* Middleware: is a function that execute during the lifecycle of a request to the express server to modify the req and res objects. Middlewares have access to the request object (req), the response object (res), and the next middleware function in the application's request-response cycle.

* Request Object: an object that represents the http request. It has properties for the request query string, parameters, body, HTTP headers, and so on. [source](https://www.javatpoint.com/expressjs-request)

* Response Object: an obkect that specifies the http response which is sent by the express server app when it gets an http request. [source](https://www.javatpoint.com/expressjs-response)

* Application Middleware: a middleware that is bound to the instance of the app object with app.use ot app.method

* Routing Middleware: a middleware that is bound to an instance of express.Router()

* Test Driven Development: software development process that relays on testing the software requirements against all test cases.

* Behavioral Testing: testing the external behavior of the program, also known as black box testing

## Preview

* Which 3 things had you heard about previously and now have better clarity on? next(), test(), and creating middlewares

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo? when to use app.use() exactly.

* What are you most excited about trying to implement or see how it works? next() and error jest testing
