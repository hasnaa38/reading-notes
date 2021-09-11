# Code 301 - Read 06

In this file, a summary of **Read: Class 06 - NODE.JS and Pair Programming** will be provided.

## NODE.JS

[Article](https://www.sitepoint.com/an-introduction-to-node-js/)

Additional resources:
* [The Relationship Between Node.Js and V8](https://www.knowledgehut.com/blog/web-development/nodejs-and-v8)
* [Node.js - Event Loop](https://www.tutorialspoint.com/nodejs/nodejs_event_loop.htm)
* [Asynchronous programming in Node.js](https://blog.risingstack.com/node-hero-async-programming-in-node-js/)

### What is node.js?

Node.js is a JavaScript runtime built based on Google Chrome’s V8 JavaScript engine. Node.js is a backend technology which has become popular because it enables a frontend developers with JavaScript skills to easily create full-stack apps.

A *JavaScript runtime* is a program that executes JavaScript on computers.

*Google Chrome’s V8 JavaScript Engine* is an open-source JavaScript engine that is responsible for compiling JavaScript directly to native machine code a computer can execute. In other words, it provides the runtime environment in which JavaScript executes. This engine runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi.

Node.js is built on top of the V8 engine; they took the V8 engine and enhanced it with various features to become a powerful server-side environment to run javaScript outside of the browser. Examples on Node.js additional functionalities include reading and editing local files, and doing HTTP requests.

A part of Node.js definition on their official website says:

> Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

*event-based* - as soon as Node.js starts its server, it initiates variables, declares functions and then waits for events to occur. In event-driven applications, there is generally a main loop that listens for events, and then triggers a callback function when one of those events is detected. Node.js uses events heavily which is one of the reasons why Node.js is fast compared to other backend technologies.

*non-blocking* - other backend technologies like PHP and ASP block the program from executing until a network request is completed. On the other hand, Node.JS sends requests and goes to the next line of code without waiting for it to complete; which is also one of the reasons why Node.js is fast compared to other backend technologies.

*Asynchronous I/O* is a form of input/output processing that permits/allows other processing to continue before an operation has finished.

### Questions

* What is npm?
It is a package manager that comes bundled with Node.

* What version of node are you running on your machine?
To check it, run `node --version` or `node -v`. Result: `v14.17.3`

* What version of npm are you running on your machine?
To check it, run `npm --version` or `npm -v`. Result: `7.22.0`

* What command would you type to install a library/package called ‘jshint’?
`npm install -g jshint`

* What is node used for?
It is used for running JavaScript on the server.
How? by running this command on the terminal: `node name_of_JS_file.js`

## Pair Programming

[Article](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

### What is pair programming, how it works?

Pair programming is when two developers sharing a single workstation interactively work on a code together. There are different styles for pair programming, commonly they involve two roles: the *Driver* and the *Navigator*.

* The Driver is the one handling the mechanics/physical side of the work, i.e; typing the code, managing the text editor, switching files, etc.

* The Navigator is the one responsible for guiding the Driver, i.e; thinking about the big picture, controlling the flow of the work, how an algorithm might be converted into code, while scanning for typos or bugs, etc. They are not supposed to write any code.

### Why pair programming?

learning coding is like learning a new language; it aquires the following skills:

* Listening - students listen to others guidance.
* Speaking - students explain out loud what the code should do.
* Reading - students write code themselves.
* Writing - students read code that others have written.

Pair programming touches on all four skills.

### Pair programming advantages

1. *Greater efficiency* - it might take a bit longer when two people focus on the same code block, however, studies show that it produces higher-quality code that doesn’t require later effort in troubleshooting and debugging. So, in the long-run, it would be more efficient than two people working on separate features.

2. Engaged collaboration* - When two programmers focus on the same code, it  becomes harder to procrastinate or get off track. Also, When two programmers work together, they can often find a solution together without the need to ask for additional help.

3. *Learning from fellow students* - each person has their unique approach to a specific problem. Pair programming exposes the different students to new approaches and maybe different experience levels.
 
4. Helps improving *social, and communication skills*. It also helps programmers in strengthening their ability to work with and learn from others. It also helps them to get familiar with how pairing works. Those skills help programmers to attract *job opportunities*.

