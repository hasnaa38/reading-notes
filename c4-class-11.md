# Code 401 - Read 11

## Revision

1. Why is access control important?
Because it defines and restricts access rights to system resources after a user's account credentials and identity have been authenticated and access to the system granted. For example, a particular user, or group of users, might only be permitted access to certain files after logging into a system, while simultaneously being denied access to all other resources.

The roles in RBAC refer to the levels of access that employees have to the network.

2. Describe an application that would need access control.
Course management systems like canvas: students can access their class material, marks, and profile info. Instructors can control the class material, grade students, and see their marks.

3. What is a role used for?
The roles in RBAC refer to the levels of access that employees have to the system network and resources.

4. Why is role based access control more scalable than discretionary or mandatory access control?

* Mandatory Access Control - access to resources is strictly controlled by the operating system based on system administrator configured settings. It is not possible under MAC enforcement for users to change the access control of a resource. IT is the strictest of all levels of control. The design of MAC was defined, and is primarily used by the government.
* Discretionary Access Control - allows each user to control access to their own data -they already own-. A hypothetical User A cannot, therefore, change the access control for a file that is owned by User B. User A can, however, set access permissions on a file that she owns. Under some operating systems it is also possible for the system or network administrator to dictate which permissions users are allowed to set in the ACLs of their resources. DAC is typically the default access control mechanism for most desktop operating systems.
* Role-based access control - restricts resources access based on a person's role within an organization and has become one of the main methods for advanced access control. Employees are only allowed to access the information necessary to effectively perform their job duties. Access can be based on several factors, such as authority, responsibility, and job competency. In addition, access to computer resources can be limited to specific tasks such as the ability to view, create, or modify a file.

RBAC is more scalable because it helps reducing the reduce administration complexity and the need for paperwork and password changes when an employee is hired or changes their role is reduced. RBAC can be used to add and switch roles quickly and implement them globally across operating systems, platforms and applications. It also reduces the potential for error when assigning user permissions. It also helps to integrate third-party users into your network easily by giving them pre-defined roles.

[source](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)

## Terms Documentation

* *Authorization* - a security mechanism to determine access levels or user/client privileges related to system resources based on the user's identity.
* *Role Based Access Control* - an approach of restricting system access to authorized users based on their role in an organization.
* *Capabilities* - permission sets that control access to areas and features within the server.

## Preview - Event Driven Applications

It is a logical pattern used to confine our programming within to avoid issues of complexity and collision. Every time you interact with a webpage through the UI, an event is happening. When you click a button a click event is triggered. When you press a key a key-down event is triggered. These events have associated functions that, when triggered, are executed to make a change to the UI in some way.

![Event Driven Programming](https://upload.wikimedia.org/wikipedia/commons/c/cb/Event_driven_programming_Simply_Explained.jpg)

Event-Driven Programming makes use of the following concepts:

* *Event Handler* - a callback function that will be called when an event is triggered.
* *Main Loop* - listens for event triggers and calls the associated event handler for that event.

### EventEmitter

EventEmitter is a Node.js native module that allows us to get started incorporating Event-Driven Programming to our projects. The EventEmitter class is accessed through the events module. Once imported we’ll need to create a new object from the class to start using it:

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

Now we can get started with Event-Driven Programming in Node.

First, we’ll write a function that will act as an event listener, then we can use EventEmitters `on` method to set the listener. Then we will use the EventEmitter `emit` method to trigger the event. We would want to trigger this event from within a login function inside of our project module.

### Removing Listeners

To remove event listeners from an event in EventEmitter, we can use the `removeListener` or `removeAllListeners` method. This could be for performance reasons (the event is no longer needed) or to avoid memory leaks.
