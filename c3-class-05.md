# Code 301 - Read 05

In this file, a summary of **Read: Class 05 -Putting it all together** will be provided.

## Thinking in React

[Article](https://reactjs.org/docs/thinking-in-react.html)

A **mock** is a simulated version of a object/service/code that mimics the behavior of the real one in controlled ways for to run test in a fast and reliable manner.

### The process of building a React app:

***Step 1*** - Break The UI Into A Component Hierarchy

- Draw boxes around every component and sub-component in the mock and give them names.
- Identify the role of each component.
- Separate the UI into components, where each component matches one piece of the data model.

***Step 2*** - Build A Static Version in React

- Building a static version means building a version that takes the data model and renders the UI but has no interactivity.
- This is done by building components that reuse other components and exchange data using props.
- For static versions, props are a way of passing data from parent to child.

***Step 3*** - Identify The Minimal (but complete) Representation Of UI State

- The state is used to make the UI interactive as it allows triggering changes to the data model.
- The minimal set of app state should be identified.
- To define a state, make sure that it represents data that changes over time and can’t be computed from anything else.

***Step 4*** - Identify Where Your State Should Live

Remember: React has a one-way data flow down the component hierarchy. To figure out which component should own what state:

1. Identify every component that renders something based on that state.
2. Find a common parent component (a component above all the components that need the state in the hierarchy).

The state should be added in this common parent component or another component higher up that hierarchy.

If it doesn't make sense for the component to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

***Step 5*** - Add Inverse Data Flow
After building an application that renders correctly as a function of props and state flowing down the hierarchy, support data flow in the other way: from a child components to a higher component in the hierarchy.

Note: components only update their own state

So to inverse the data flow, we will use events to fire a callback function whenever the state should be updated. The state will be updated using the setState() method, and the app will be updated.

### Questions

- How would you break a mock into a component hierarchy?

By drawing boxes around every component and sub-component and giving them names.

- What is the single responsibility principle and how does it apply to components?

It is a technique for deciding if a new function/object/component should be created based on the number of things it does. A component should ideally only do one thing.

- What does it mean to build a ‘static’ version of your application?

It means building a version of the application that takes the data model and renders the UI but has no interactivity.

- Once you have a static application, what do you need to add?

States to make it interactive.

- What are the three questions you can ask to determine if something is state?

1. Can it be passed in from a parent via props? If so, it probably isn’t state.
2. Does it remain unchanged over time? If so, it probably isn’t state.
3. Can we compute it based on any other state or props in the component? If so, it isn’t state.

- How can you identify where state needs to live?

1. Identify every component that renders something based on that state.
2. Find a common parent component (a component above all the components that need the state in the hierarchy).

The state should be added in this common parent component or another component higher up that hierarchy.
If it doesn't make sense for the component to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.
