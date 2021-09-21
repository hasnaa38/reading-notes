# Code 301 - Read 14

In this file, a summary of **Read: Class 14 - Authentication** will be provided.

## OAuth

[What is OAuth? How the open authorization framework works](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

* What is OAuth?

OAuth is a framework that allows websites and services to share assets among users. It provides secure, third-party, user-agent, delegated authorization. OAuth open-standard authorization protocol/framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing initial credentials.

*Authentication* is the process of a user/subject proving its ownership of a presented identity, by providing a password or some other uniquely owned or presented factor. Simply: it is the process of verifying who a user is.

*Authorization* is the process of letting a subject access resources after a successful authentication. Simply: it is the process of verifying what they have access to.

OAuth (Open AUTHorization) is about authorization in particular and not directly about authentication.

Most OAuth scenarios represent two unrelated sites or services trying to accomplish something on behalf of users or their software. The three have to work together involving multiple approvals for the completed transaction to get authorized.
An example is when you try to log into a website and it offers one or more opportunities to log in using another website or service, for example, signing into instagram using your facebook account.

Note: OAuth only works using HTTPS.

* Give an example of what using OAuth would look like.

It is like a car’s valet key, which can be used to allow a valet to temporarily drive and park a car, but it doesn’t allow him full, unlimited access like a regular key. OAuth essentially allows the user to give another website/service a limited access authentication token for authorization to additional resources.

* How does OAuth work? What are the steps that it takes to authenticate the user?

Assuming the user has already signed into one website and required access to another unrelated site/service:

1. Using OAuth, the first website connects to the second website on behalf of the user, providing the user’s verified identity.
2. The second site generates a one-time token and a one-time secret unique to the request.
3. The first site gives this token and secret to the user's client software.
4. The client’s software presents the request token and secret to their authorization provider.
5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After that, the client is asked to approve the authorization transaction to the second website.
6. The client approves a particular transaction type at the first website.
7. The user is given an approved access token.
8. The user gives the approved access token to the first website.
9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
10. The second website lets the first website access their site on behalf of the user.
11. The user receives a successfully completed transaction occurring.

![Steps simplified](https://pattern-match.com/images/blog/content/OAuth2-abstract-flow-diagram.svg)

* What is OpenID?

It is another security technology that is about authentication (ie. proving who you are) not authorization (ie. to grant access to services without having to deal with the original authentication).

### Authorization and Authentication flows

[Authentication and Authorization Flows](https://auth0.com/docs/authorization/flows)

* What is the difference between authorization and authentication?

*Authentication* is the process of a user/subject proving its ownership of a presented identity, by providing a password or some other uniquely owned or presented factor. Simply: it is the process of verifying who a user is.

*Authorization* is the process of letting a subject access resources after a successful authentication. Simply: it is the process of verifying what they have access to.

* What is Authorization Code Flow?

Used to exchange an authorization code for a token. Why? Because web apps server-side source code is not publicly exposed.
During this exchange, you must also pass along your application's Client Secret, which must always be kept secure, and you will have to store it in your client.

How it works:

![Authorization Code Flow](https://images.ctfassets.net/cdy7uua7fh8z/2nbNztohyR7uMcZmnUt0VU/2c017d2a2a2cdd80f097554d33ff72dd/auth-sequence-auth-code.png)

* What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

When public clients request Access Tokens, some additional security concerns are posed that are not mitigated by the Authorization Code Flow alone.

The PKCE Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the *Code Verifier*. Additionally, the calling app creates a transform value of the Code Verifier called the *Code Challenge* and sends this value over HTTPS to retrieve an *Authorization Code*. This way, a malicious attacker can only intercept the Authorization Code, and they cannot exchange it for a token without the Code Verifier.

How it works:

![PKCE](https://images.ctfassets.net/cdy7uua7fh8z/3pstjSYx3YNSiJQnwKZvm5/33c941faf2e0c434a9ab1f0f3a06e13a/auth-sequence-auth-code-pkce.png)

* What is Implicit Flow with Form Post?

It is a method of implementing web sign-in without obtaining, maintaining, using, and protecting a secret in your application. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls.

How it works:

![Implicit Flow](https://images.ctfassets.net/cdy7uua7fh8z/6m0uE4E7Hpzbdhyh9dEuYK/e36c910ff47a7540bf27e23c02822624/auth-sequence-implicit-form-post.png)

* What is Client Credentials Flow?

Machine-to-machine applications, like services running on your back-end, the system authenticates and authorizes the app rather than a user. Therefore, machines use this method to pass along their Client ID and Client Secret to authenticate themselves and get a token.

How it works:

![Client Credentials Flow](https://images.ctfassets.net/cdy7uua7fh8z/2waLvaQdM5Fl5ZN5xUrF2F/8c5ddae68ac8dd438cdeb91fe1010fd1/auth-sequence-client-credentials.png)

* What is Device Authorization Flow?

Rather than authenticate the user directly, this method allows the device to ask the user to go to a link on their computer or smartphone and authorize the device.

How it works:

![Device Authorization Flow](https://images.ctfassets.net/cdy7uua7fh8z/1A6jpG3W1H6SC9ZK92NyKd/40af53209f90a7c392f621f329fb4424/auth-sequence-device-auth.png)

* What is Resource Owner Password Flow?

It is a method which requests users to provide their credentials (username and password), typically using an interactive form.

How it works:

![Resource Owner Password Flow](https://images.ctfassets.net/cdy7uua7fh8z/4EeYNcnVX1RFcTy5z4lP4v/c3e4d22e6f8bf558caf07338a7388097/ROP_Grant.png)