# Code 401 - Read 36

## Revision

* What are the advantages of storing tokens in “Cookies” vs “Local Storage”

>>> Local storage is vulnerable because it's easily accessible using JavaScript and an attacker can retrieve your access token and use it later. However, while httpOnly cookies are not accessible using JavaScript, this doesn't mean that by using cookies, you are safe from XSS attacks involving your access token.

* Explain 3rd party cookies.

Third-party cookies are created by domains that are not the website (domain) that you are visiting. These are usually used for online-advertising purposes and placed on a website through adding scripts or tags. A third-party cookie is accessible on any website that loads the third-party server's code.

* How do pixel tags work?

The website operator or sender of an email adds the tracking pixel using a code in the website’s HTML code or email. This code contains an external link to the pixel server. If a user visits the destination website, the HTML code is processed by the client – usually the user’s browser. The browser follows the link and opens the (invisible) graphic. This is registered and noted in the server’s log files.

## Terms Documentation

* **cookies**: data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them.
* **authorization**: a security mechanism to determine access levels or user/client privileges related to system resources based on the user's identity.
* **access control**: the approach of restricting system access to authorized users based on their role in an organization.
* **conditional rendering**: displaying components based on a certain condition.

## Preview - Application State with Redux

Redux is an open-source JavaScript library for managing and centralizing application state.

Redux can be used with any frontend framework, such as React, Angular, or even Vue. In the end, you can implement the Redux pattern in any vanilla JS application.

It allows you to maintain a predictable state container for your JavaScript apps. This is important for consumer-facing applications where the interface changes based on user input.

Each **action** contains a type (also seen as an identifier) and a payload. Next, a reducer accepts the action and changes the state based on the received action type and payload.

**Reducers** are pure functions, which means they are predictable. A pure function returns the same output for the same input. You can use reducers to generate a new application state.

to notify our interface that the application state has changed, we can subscribe to data changes. Whenever the application state changes, we update the UI.

Redux takes away the responsibility from individual components to manage a state. Instead, we create a single store that handles our state management. On top of that, all communication regarding reading, updating, or creating data happens via the store.

### Redux cycle

1. Users interact with the interface and triggers an action
2. Action with/without payload is sent to a reducer using the dispatcher
3. Reducer checks if it handles the action and produces a new state based on the action and its payload
4. State changes are notified via subscription methods
5. UI renders again based on state changes received via the subscription method

![redux cycle](https://res.cloudinary.com/academind-gmbh/image/upload/f_auto,q_auto:eco/dpr_2.0,w_400,c_limit,g_center/v1/academind.com/content/tutorials/reactjs-redux-vs-context-api/redux-overview)

