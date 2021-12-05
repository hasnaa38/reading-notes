# Code 401 - Read 26

## Revision

* Name 5 Javascript UI Frameworks (other than React):

    1. Angular
    2. Vue
    3. Solid
    4. Vaadin
    5. Syncfusion

    [more](https://webix-ui.medium.com/10-top-javascript-ui-frameworks-libraries-for-2021-88b1fef943ec)

* What’s the difference between a framework and a library?

A framework is a supporting structure that gives shape to your application. In which, you have to fill the structure accordingly with your application's code. The framework defines the concept but the application defines the fundamental functionality that end-users care about.
Examples of frameworks: Web application system, Plug-in manager, GUI system.

>> A framework embodies some abstract design, with more behavior built in. In order to use it you need to insert your behavior into various places in the framework either by sub-classing or by plugging in your own classes. The framework's code then calls your code at these points.

A library performs specific, well-defined operations. 
Examples of libraries: Network protocols, compression, image manipulation, string utilities, regular expression evaluation, math. Operations are self-contained.

A library is essentially a code written by a developer that you can call/import when you are building your project. Each call does some work and return control to the client.

[more](https://dev.to/rohitrana/what-is-the-difference-between-library-vs-framework-174n)

![difference1](https://lh3.googleusercontent.com/proxy/_4d73lEXvR5WRBi0h4HzBKyd6gnjmm4ywMeZY_QAqxDZKckj6dVbOfU8_Ydf504cyFabNtVAqMTKVBW7mCFHG1qa5vOqM5cQfAwukbsw7coRag)

![difference2](https://lh3.googleusercontent.com/proxy/MmbgBPcSKHIjSqRgeDyO0UPrygsj0PlHXDYDNzzVZ97Y7H__4Mdw3TIHmLDWYOfx5A7dPDRIC_hBBl6z6bB9sUXFQefGhBdI0bdyGBO_ow3ikbPTN-vRavc_)

## Terms Documentation

* **Rendering**: the process of transforming a react components into DOM nodes that a browser can understand and display its content on the screen. React DOM takes care of updating the DOM to match the React elements.

* **Templates**: sets of ready-to-use parts of code built using React technology for the development of dynamic UIs. React templates simplify the process of web development by providing working units of code for developers, so they don’t need to write a code from scratch.

* **State**: a plain JavaScript object of a set of observable properties that React uses to control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.

## Preview - Component Based UI

### react hello world

React is an open-source JavaScript library created by Facebook used for building user interfaces specifically for single-page applications. It’s used for handling the view layer for web and mobile apps. React also allows us to create reusable UI components.

[Link](https://reactjs.org/docs/hello-world.html)
[more](https://www.c-sharpcorner.com/article/what-and-why-reactjs/)

### introducing JSX

JSX stands for JavaScript XML. It is a syntax extension of JavaScript that allows us to directly write HTML in React (within JavaScript code). After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

[Link](https://reactjs.org/docs/introducing-jsx.html)

### rendering elements

Rendering is the process of transforming a react components into DOM (Document Object Model) nodes that a browser can understand and display its content on the screen.

React elements are plain objects unlike DOM elements. React creates a virtual representation of what the DOM should look like called the Virtual DOM. Thus; manipulating React elements is much faster than DOM manipulation.

React DOM takes care of updating the DOM to match the React elements.

Whenever any changes is been made to a running React application, React will batch all of these changes together in its Virtual DOM, then compare this representation with the actual DOM, find what needs to be updated, and then make the smallest possible changes to the real DOM to keep them in sync while keeping the application performant.

[Link](https://reactjs.org/docs/rendering-elements.html)
