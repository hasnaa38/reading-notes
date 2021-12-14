# Code 401 - Read 34

## Revision

* How do bearer tokens work?

a bearer token is an authentication method that relies on the fact that all services receive a token as proof that the application is allowed to access the assets on the server. The name *Bearer authentication* can be understood as: give access to the bearer of this token.

The bearer token is a cryptic string, usually issued by the server in response to a login request. The server usually generates it using a trusted third party service. The client must send this token in the Authorization header when making requests to protected resources: `Authorization: Bearer <token>`

[more](https://swagger.io/docs/specification/authentication/bearer-authentication/)

* Describe express middleware

>>> Middleware literally means anything you put in the middle of one layer of the software and another. Express middleware are functions that execute during the lifecycle of a request to the Express server. Each middleware has access to the HTTP request and response for each route (or path) it’s attached to. In fact, Express itself is compromised wholly of middleware functions. Additionally, middleware can either terminate the HTTP request or pass it on to another middleware function using next (more on that soon). This “chaining” of middleware allows you to compartmentalize your code and create reusable middleware.

[source](https://developer.okta.com/blog/2018/09/13/build-and-understand-express-middleware-through-examples)
[more](https://blog.logrocket.com/express-middleware-a-complete-guide/)

* What is a JWT?

JSON Web Token (JWT) is a standard that defines a way for transmitting information securely between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be:
    1. signed using a secret or a public/private key pair. Here, everyone can read the token's contents, but it can't be changed without the private key.
    2. encrypted

JWTs can be used for:

1. **Authorization**: Once the user is logged in, each request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

2. **Secure information exchange**: Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

## Terms Documentation

* **role based access control**: an approach of restricting system access to authorized users based on their role in an organization

* **http cookies**: http cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them
