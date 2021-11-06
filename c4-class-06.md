# Code 401 - Read 04

## Revision

### Singleton

Its a design pattern which restricts a class to instantiate its multiple objects. Through this design pattern, the singleton class ensures that it’s only instantiated once, and can provide easy access to the single instance. Singletons are sometimes considered to be an alternative to global variables or static classes.

The Singleton pattern can be used with Node modules as a way of defining a class in a way that only one instance of the class is created in the complete execution of a program. It is used where only a single instance of a class is required to control the action throughout the execution.

Singleton classes are used for logging, driver objects, caching and database connections.

## Terms Documentation

* **Router Middleware** - a piece of code that manages http requests and responses.

* **Dynamic Module Loading** - a mechanism by which a computer program can, at run time:
    1. load a library into memory
    2. retrieve the addresses of functions and variables contained in the library
    3. execute those functions or access those variables
    4. unload the library from memory

* **Singleton Pattern** - a design pattern which restricts a class to instantiate its multiple objects.

* **CRUD -> REST Method Matches** - Create <-> POST, Read <-> GET, Update <-> PUT, Delete <-> DELETE

* **Mock Testing** - creating a fake version of an external or internal service that can stand in for the real one, helping tests to run more quickly and more reliably.

## Preparation Materials

### [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

Desktop applications and almost every web service need to store a collection of user data and the passwords, that has to be stored using a hashing algorithm. Hashing is a way for protecting and ensuring the integrity of data or password. Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible.

The benefit of hashing is that if someone could hack the database, they will be left with hashed passwords, not the actual plaintext passwords. However, there are some weaknesses in cryptographic hash algorithm that allows an attacker to calculate the original value of a hashed password, as explained below:

* **Brute Force attack**: Hashes can't be reversed, so instead of reversing the hash of the password, an attacker can simply keep trying different inputs until he does not find the right now that generates the same hash value, called brute force attack.
General-purpose hash function designed for speed,, using a modern computer one can crack a 16 Character Strong password in less than an hour.

* **Hash Collision attack**: Hash functions have infinite input length and a predefined output length, so there ia a possibility of two different inputs to produce the same output hash. MD5, SHA1, SHA2 are vulnerable to Hash Collision Attack.

To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact. Such algorithms are PBKDF2 and BCrypt, both of these algorithms use a technique called *Key Stretching*.

#### Bcrypt

Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (aka security factor), which allows you to determine how expensive the hash function will be.

The work factor value determines how slow the hash function will be, means different work factor will generate different hash values in different time span, which makes it extremely resistant to brute force attacks. As computers become faster, you can increase the work factor to make the attack slower.

This hashing algorithm is implemented in a number programming languages like PHP, Java, Ruby, C#, C etc.

**[node.bcrypt.js](https://www.npmjs.com/package/bcrypt)** is a library to help you hash passwords.

### [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

Basic access authentication (BA) is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. HTTP BA implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, it uses standard fields in the HTTP header. The header is in the form of `Authorization: Basic <credentials>`, where credentials is the Base64 encoding of ID and password joined by a single colon `:`.

The A mechanism does not provide confidentiality protection for the transmitted credentials. Therefore, basic authentication (hashing or encrypting) is typically used in conjunction with HTTPS to provide confidentiality.

When the *server* wants the user agent to authenticate itself towards the server after receiving an unauthenticated request, it must send a response with a `HTTP 401 Unauthorized` status line and a `WWW-Authenticate` header field.

![http ba](https://media.springernature.com/original/springer-static/image/prt%3A978-1-4419-5906-5%2F8/MediaObjects/978-1-4419-5906-5_8_Part_Fig1-111_HTML.gif)

When the *client* wants to send authentication credentials to the server, it may use the `Authorization` header field. This filed is constructed as follows:

1. The username and password are combined with a single colon `:`. This indicates that the username itself cannot contain a colon.
2. The resulting string is encoded into an octet sequence.
3. The resulting string is encoded using a variant of Base64.
4. The authorization method and a space (e.g. "Basic ") is then appended to the encoded string.

![BA auth header field](https://i.stack.imgur.com/8lhG6.png)

Since the BA field has to be sent in the header of each HTTP request, the web browser needs to cache credentials for a reasonable period of time to avoid constantly prompting the user for their username and password.

HTTP does not provide a method for a web server to instruct the client to "log out" the user, i.e, clear cached credentials. However, there are a number of methods to do so. One of them is redirecting the user to a URL on the same domain, using credentials that are intentionally incorrect.

### [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

**Authentication** is the process of verifying that an entity is whom it claims to be. Authentication is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

**Session Management** is a process by which a server maintains the state of an entity interacting with it. Sessions are maintained on the server by a session identifier which can be passed back and forward between the client and server when transmitting and receiving requests.

#### Authentication General Guidelines

* User IDs should be:

1. Unique
2. Case-insensitive

For high-security applications, usernames could be assigned and secret instead of user-defined public data.

* Implement password strength controls properly. The following characteristics define a strong password:

   1. Password length - the minimum length of the passwords should be enforced by the application. Passwords shorter than 8 characters are considered to be weak. The maximum password length should not be set too low, as it will prevent users from creating passphrases. A common maximum length is 64 characters due to limitations in certain hashing algorithms.
   2. Do not silently truncate passwords.
   3. Allow usage of all characters including unicode and whitespace.
   4. Ensure credential rotation when a password leak, or at the time of compromise identification.
   5. Include password strength meter to help users create more complex passwords and block common and previously breached passwords

* Implement secure password recovery mechanism

* Store passwords using the right cryptographic technique

* Transmit passwords over TLS or other strong transport protocols. Failure to utilize a strong transport for the login landing page allows an attacker to modify the login form action, causing the user's credentials to be posted to an arbitrary location. Failure to utilize a strong transport for authenticated pages after login enables an attacker to view the un-encrypted session ID and compromise the user's authenticated session.

* Require re-authentication for sensitive features. Without this countermeasure, an attacker may be able to execute sensitive transactions without needing to know the user's current credentials. Additionally, an attacker may get temporary physical access to a user's browser or steal their session ID to take over the user's session.
