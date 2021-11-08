# Code 401 - Read 09

## Revision

* When is Basic Authorization used vs. Bearer Authorization?

**Basic Authorization** is a simple authentication method that creates a username and password style authentication for HTTP requests. This technique uses a header called Authorization, with a base64 encoded representation of the username and password. Depending on the use case, HTTP Basic Auth can authenticate the user of the application, or the app itself.
[source](https://nordicapis.com/the-difference-between-http-auth-api-keys-and-oauth/)

This method is one of the least secure authentication mechanisms. Therefore, it can be used when the connection is guaranteed to be secure, for example, server-to-server connection or a house LAN that has its own in-LAN server.

**Bearer Authorization** is a token-based authentication method relies on the fact that all services receive a token as proof that the application is allowed to call the service. The token is issued by a third party that can be trusted by both the application and service.
[source](https://nordicapis.com/the-difference-between-http-auth-api-keys-and-oauth/)

This method can be used to verify a client-web server connection.

[Additional](https://stackoverflow.com/questions/34013299/web-api-authentication-basic-vs-bearer)

* What does the JSON Web Token package do?

It gives us the ability to implementation jwt's in our code.

* What considerations should we make when creating and storing a SECRET?

1. It should be unique for the application
2. Store it as environment variables
3. Don't share it publicly
4. Encrypt it
5. Restrict API access and permissions

[Additional](https://blog.gitguardian.com/secrets-api-management/)

## Terms Documentation

* **encryption** - the process of converting human-readable plaintext to incomprehensible text, so that only authorized parties can understand the information.
* **token** - a secure format used to transmit sensitive information between two parties in a compact and self-contained manner. Tokens are often used to strengthen authentication processes.
* **bearer** - a token-based authentication method relies on the fact that all services receive a token as proof that the application is allowed to call the service.
* **secret** - a private key that is known by both communication parties. [Additional](https://stackoverflow.com/questions/31309759/what-is-secret-key-for-jwt-based-authentication-and-how-to-generate-it)
* **JSON Web Token** - a standard that defines a way for transmitting information securely between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

## Preparation, Topic: << Role-Based Access Control >>

It is the approach of restricting system access to authorized users based on their role in an organization.
With the proper implementation of RBAC, the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.

### RBAC variations:

1. *Access control lists (ACL)* - defining access rights by a given user or user group, to a specific object, such as a document. Example: allowing users from one department to make changes to a document, while only allowing users from other departments to read the document.
2. *Attribute-based access control (ABAC)* - sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.

### RBAC implementation

1. Inventory the systems: list what resources you have for which you need to control access.
2. Analyze the workforce and create roles: group your workforce members into roles with common access needs. Keep them as simple and stratified as possible.
3. Assign people to roles: now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.
4. Never make one-off changes: only apply changes when necessary.
5. Audit: periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role.
