# Code 301 - Read 02

In this file, a summary of **Read: Class 02 - State and Props** will be provided.

## Topic 1 - React components lifecycle

Every React component has a lifecycle.
There are 3 phases/stages of the component lifecycle:

1. **Mounting** - called each time a component is being created and inserted into the DOM (when the component is rendered for the first time).

* Mounting lifecycle events (in order):

    1. Constructor
    2. static getDerivedStateFromProps
    3. render
    4. componentDidMount
    5. UNSAFE_componentWillMount

2. **Updating** - called when:

    1. An update of a prop used in the component occurs.
    2. An update of a state variable occurs.
    3. Force updating the component.

* Updating lifecycle events (in order):

    1. static getDerivedStateFromProps
    2. shouldComponentUpdate
    3. render
    4. getSnapshotBeforeUpdate
    5. componentDidUpdate
    6. UNSAFE_componentWillUpdate
    7. UNSAFE_componentWillReceiveProps

3. **Unmounting** - called when a component is being removed from the DOM.

* componentWillUnmount is the only lifecycle event during this phase.

### Questions:

* Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’? The render

* What is the very first thing to happen in the lifecycle of React? The constructor of the React component.

* Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates:
    1. Constructor
    2. render
    3. React Updates
    4. componentDidMount
    5. componentWillUnmount

* What does componentDidMount do? Indicates that the component has been mounted.

## Topic 2 - React State Vs Props

Both are JavaScript objects that hold data.

### Props

JavaScript objects that hold data then pass it from one component to another.
With props we pass values we want to use inside our components, props can be used in situations like:

1. Setting up initial values for the component, for example: a counter initial value.
2. To pass information for the component to render, for example: students names and ages for table cells.

Handled/updated outside the component.
They get passed to the component similar to function parameters

Useful for displaying dynamic content of the component.

### State

A JavaScript objects that holds data being managed inside the component to influences the output of render.

Handled/updated inside the component.
It is similar to variables declared within a function.

example: setting a state to the initial value and updating this value.

Changing the state will re-render that component.

Useful for updating the app based on something the user has done. The component will be updated each time the state changes.

### Questions

* What types of things can you pass in the props?
Data / state from another component.

* What is the big difference between props and state?
Props are handled and updated outside the component, they make the component dynamic but the prop itself is a static value for the component.
States are handled and updated inside the component.

* When do we re-render our application?
Each time we get new props (updating them in their parent component), and each time we update the state in the component.

* What are some examples of things that we could store in state?

1. Counting how many time a button has been clicked (to record the likes or change the inventory stock).
2. To update the content based on the change of the state (to change the text per second).
