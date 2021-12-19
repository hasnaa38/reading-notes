# Code 401 - Read 39

## Revision

* Why choose Redux instead of the Context API for global state?

Redux is suitable for larger applications where there are high-frequency state updates

* What is the purpose of a reducer?

its a pure function that takes an action and the previous state of the application and returns the new state

* What does an action contain?

an object with type and payload. The type indicates the type of action performed, and the payload carries information to the store.

* Why do we need to copy the state in a reducer?

reducers copy state and make changes to that copy to avoid mutating the original state

## Terms Documentation

* **immutable state**: a state that its value cannot be changed, so every update creates new value, leaving the old one untouched
* **time travel in redux**: ability to move back and forth among the previous states of an application
* **action creator**: a function that creates an action object
* **reducer**: a function that takes in an action and state to mutate the original state and return the new state of our application
* **dispatch**: a method used to dispatch actions and trigger state changes to the store

## Preview - Redux - Combined Reducers

combineReducer is a Redux helper function that turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by `combineReducers()` namespaces the states of each reducer under their keys as passed to `combineReducers()`.

