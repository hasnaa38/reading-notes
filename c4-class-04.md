# Code 401 - Read 04

## Revision

* Name 3 advantages to Test Driven Development
1. Enhances the quality of the code.
2. The code is easier to maintain.
3. Helps documenting the code better.
Tests Driven Development means that tests are going to be performed on a single features at a time. Focusing on each feature and making sure its fully working before moving to the next one is what causes those advantages.

* In what case would you need to use beforeEach() or afterEach() in a test suite?
They are jest helper functions to handle the repeated runs of a piece of code before/after each test run. for many tests, you can use beforeEach and afterEach. So when you have multiple tests that require doing some work before/after each test run, write the code inside them.

* What is one downside of Test Driven Development
It slows down the coding process since you will need extra time to refactor the code to modularize it and write the test code.

* What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
An ES6 JS class is a template that defines an object and can be instantiated at runtime. A normal constructor/prototype is an object instance.
A child of an ES6 class is another definition template which extends the parent with new properties and methods, which in turn can be instantiated at runtime.
A child of a prototype is another object instance which delegates to the parent any properties that aren’t implemented on the child.

* Why REST?
1. REST uses the http protocol verbs that are simple and most of people know.
2. its stateless on the server-side. Stateless servers keep resources as long as they are handling a request, and they free the memory as soon as the request is processed.
3. RESTful APIs use JSON files as the data interchange format. JSON is much more compact and smaller in size compared to XML. It can also be parsed faster than XML.

## Terms Documentation

* functional programming: a programming paradigm built on the concept of composing pure functions to build software.

* object-oriented programming (OOP): a programming paradigm built on the concept of objects that contain both data and code to modify the data.

* class: a special function that encapsulates data and methods that manipulate data to create objects.

* super: a keyword used to access the object's parent and call functions on it.

* this: a  keyword refers to the object it belongs to. It has different values depending on where it is used.

* Test Driven Development (TDD): a software development approach in which test cases are developed to specify and validate what the code will do.

* Jest: a JavaScript testing framework used for creating, running, and structuring tests.

* Continuous Integration (CI): the practice of automating the integration of code changes from multiple contributors into a single software project.

* REST: n architectural style for providing standards between computer systems (like clients or servers) on the web, making it easier for systems to communicate with each other.

* Data Model: an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
SQL databases and env variables.
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
Using postgres with Heroku.
* What are you most excited about trying to implement or see how it works?
Configuring the environment variables using config.json file, using beforeAll and afterAll.
