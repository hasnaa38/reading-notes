# Code 401 - Read 27

## Revision

* How does React differ from vanilla JS/HTML/CSS?

React takes advantage of HTML's popularity and strength, by letting developers use a very similar syntax to HTML to build interfaces and add dynamic features to it using JS. React uses JSX; which is a JS extension to easily append and update elements to the DOM. UI appends/updates in vanilla JS have to happen by finding the DOM node to update and manually appending or removing elements. React automatically updates the UI based on setting and changing state within the component.

React requires breaking the UI into components, but vanilla JS apps can be structured in any way that fits.

Data for vanilla JS apps is stored in the DOM itself and has to be found from the DOM before it can be used. Whereas React apps store data in regular JavaScript variables.

* What is the primary difference between a function component and a class component?

Functional components are plain JS functions that accept props as an argument and return React elements (no render method). Class components are extended from the React class component and they use the render method to return React elements.

Functional components has no constructors, unlike class components.

Functional components are easier to read, debug, and test. They offer performance benefits, decreased coupling, and greater reusability and stability.

## Terms Documentation

* **Functional Components**: plain JS functions that accept props as an argument and return React elements.

* **Children / Child Components**: components invoked in another component (called the parent). In the following example, `ProfileImage` and `ProfileDetails` are children of `Profile`.

```
<Profile>
  <ProfileImage src="/asset/profile-img.png" />
  <ProfileDetails name="name" surname="surname" />
</Profile>
```

## Preview - Hooks

### React Hooks

Hooks are regular JavaScript functions that let you “hook into” (use) React features like state, lifecycle, and context. Hooks let us organize the logic inside a component into reusable isolated units.

React provides built-in hooks like `useState` and `useEffect` which can be used for:

1. creating custom hooks to reuse stateful behavior between different components
2. introducing the ability to use React state while writing functional components; which were known as stateless components before adding this feature. Hooks don’t work inside classes, but they can be used instead of writing classes.

#### Rules of Hooks

Hooks are JavaScript functions, but they impose two additional rules:

1. Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
2. Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions or React class components.

[link](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889),
[link](https://reactjs.org/docs/hooks-overview.html), 
[link](https://reactjs.org/docs/hooks-reference.html)

### The State Hook

Previously, function components that needed a state had to be converted to a class components. Thus, function components were known as stateless components. Now, the `useState` hook can be used inside the existing function component to add React state.

#### Declaring a State Variable

In a function component, we have no `this`, so we can’t assign or read `this.state`. Instead, we call the `useState()` Hook directly inside our component after importing it from react and we pass the initial state to it. Unlike with classes, the state doesn’t have to be an object. `useState()` returns a pair of values: the current state and a function that updates it.

```
import React, { useState } from 'react';

function Example() {
  // the count state variable
  const [count, setCount] = useState(0);
```

This JavaScript syntax is called **array destructuring**. `useState()` returns a pair; an array with two item. So we’re making two new variables *count* and *setCount*, where count is set to the first value returned by useState, and setCount is the second.

#### Reading State

In a function component, we can use the state variable directly to read the state:

```
<p>You clicked {count} times</p>
```

#### Updating State

In a function component, we already have defined a function to update the state:

```
<button onClick={() => setCount(count + 1)}>
    Click me
</button>
```

#### Using Multiple State Variables

```
function ExampleWithManyStates() {
  // Declare multiple state variables!
  const [age, setAge] = useState(42);
  const [fruit, setFruit] = useState('banana');
  const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
```

[link](https://reactjs.org/docs/hooks-state.html)
