# Code 401 - Read 07

## Revision

* Write the following steps in the correct order:
    1. Register your application to get a client_id and client_secret
    2. Ask the client if they want to sign in via a third party
    3. Redirect to a third party authentication endpoint
    4. Make a request to a third-party API endpoint
    5. Receive authorization code
    6. Make a request to the access token endpoint
    7. Receive access token

* What can you do with an authorization code?

To verify that the user is who they claim to be.

* What can you do with an access token?

To make API requests on behalf of a user.

* What’s a benefit of using OAuth instead of your own basic authentication?

It enables apps to obtain limited access to a user's data without giving away a user's password.

## Terms Documentation

* Client ID: the client's public identifier for apps. It must be unique and un-guessable across all clients that the authorization server handles.
* Client Secret: a secret known only to the application and the authorization server. It protects the apps resources by only granting tokens to authorized requestors.
* Authentication Endpoint: an authentication point that produces a mechanism to verify the identity of the connecting device. It ensures that only valid or authorized devices are connected to a server.
* Access Token Endpoint: a point where apps make a request to get an access token for a user.
* API Endpoint: a point at which an API connects with the software program.
* Authorization Code: a code that authorizes the user.
* Access Token: a tiny piece of code that contains information about the user, permissions, groups, and time frames is embedded within one token that passes from a server to a user's device.

## Preparation, Topic: << JSON Web Tokens - JWTs >>

### What is JSON Web Token?

JSON Web Token (JWT) is a standard that defines a way for transmitting information securely between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be:
    1. signed using a secret or a public/private key pair. Here, everyone can read the token's contents, but it can't be changed without the private key.
    2. encrypted

JWTs can be used for:

1. **Authorization**: Once the user is logged in, each request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

2. **Secure information exchange**: Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

### JWT structure

In its compact form, JWTs consist of three parts separated by dots (.), them being:

* **Header**: typically consists of two parts:
    1. the type of the token, which is JWT
    2. the signing algorithm being used

example:

```
{
  "alg": "HS256",
  "typ": "JWT"
}
```

* **Payload**: it contains the claims. Claims are statements about the user and additional data. There are three types of claims: registered, public, and private claims.

example:

```
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```

* **Signature**: used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is. To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

example:

```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```

* The output is three Base64-URL strings separated by dots that can be easily passed in HTML and HTTP environments that looks like this: xxxxx.yyyyy.zzzzz. Actual example:

![jwt example](https://cdn.auth0.com/content/jwt/encoded-jwt3.png)

### How do JWTs work?

Steps for obtaining a JWT to access APIs or resources:

1. The application/client requests authorization to the authorization server.
2. When the authorization is granted, the authorization server returns an access token to the application.
3. The application uses the access token to access a protected resource (like an API).

![obtaining JWTs f1](https://cdn2.auth0.com/docs/media/articles/api-auth/client-credentials-grant.png)

So, when the user successfully logs in using their credentials, a JWT will be returned:

![obtaining JWTs f2](https://www.vaadata.com/blog/wp-content/uploads/2016/12/JWT_tokens_EN.png)

Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the `Authorization` header using the Bearer schema. The header will look like this:

```
Authorization: Bearer <token>
```

The server's protected routes will check for a valid JWT in the `Authorization` header, if it's present, the user will be allowed to access protected resources.

* see this: [link](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
