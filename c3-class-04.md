# Code 301 - Read 04

In this file, a summary of **Read: Class 04 - React and Forms** will be provided.

## React Docs - Forms

[Article](https://reactjs.org/docs/forms.html)

Form elements work a bit differently in React, because they naturally keep some internal state.

Forms in React still have the default behavior of refreshing the page when the user submits the form.

One way og handling the submission of the form and accessing the data entered by users is **controlled components** technique. A controlled component is an input form element whose value is controlled by:

1. the React state
2. the form event value from the React component that renders the form

The submit handling function that updates the submitted values would be:

```
handleChange(event) {
    this.setState({value: event.target.value});
}
```

Within the same component, the submitted value will be passed by React state: `this.state.value`.

To handle multiple controlled input elements add a name attribute to each element and let the handler function decides what to do based on the value of `event.target.name`.

### Questions

* What is a ‘Controlled Component’?
An input form element whose value is controlled by the React state as the only source for the value within the component and the form event value from the React component that renders the form.

* Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
We wait until they submit because they might change the input while typing it so storing all their tries will end up being impractical.

* How do we target what the user is entering if we have an event handler on an input field?
using `event.target.userInput`


## The Conditional (Ternary) Operator

[Article](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

It is a shorter way of specifying whether a certain block of code should be executed or not based of a certain condition.

Syntax: 

```
condition ? value if true : value if false
```

### Questions

* Why would we use a ternary operator? 
To specify whether a certain block of code should be executed or not based of a certain condition.

* Rewrite the following statement using a ternary statement:

```
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```

Solution:

```
(x===y) ? console.log(true) : console.log(false);
```
