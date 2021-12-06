# Code 401 - Read 29

## Revision

* How can we ensure that an effect hook runs only once?

By passing an empty array ( [] ) as a second argument. This way React will run the code inside it only once on mount/unmount, and React will know that the effect doesn't depend on any values from props or state, so it never needs to re-run

* Can `useState()` update more than one state variable at the same time?

Yes, `useState()` can be used multiple times to declare multiple state variable pairs

A single instance can't but creating multiple state variables can.

* Is `useState()` synchronous?

No, its asynchronous

## Terms Documentation

* **State Hook**: a built-in React Hook used inside the a function component to add the React state feature.

* **Component Lifecycle**: it is the phase a component is going through. The component’s lifecycle is broadly classified into four parts: initialization, mounting, updating, and unmounting: React components are created by being mounted onto the DOM, they change or grow through updates, and finally, they can be removed or unmounted from the DOM.

## Preview - Advanced State with Reducers

The `useReducer()` is an alternative to `useState()`. It helps with separating concerns (rendering and state management) by extracting the state management out of the component.

The `useReducer()` hook accept 2 arguments: the **reducer function** and the **initial state**. The hook then returns an array of 2 items: the **current state** and the **dispatch function**:

```
const [state, dispatch] = useReducer(reducer, initialState);
```

* The **action object** is an object that describes how to update the state. Typically, it has a property type; a string describing what kind of state update the reducer must do. It can also carry a payload that can be used by the reducer.
* The **dispatch function** is a special function that dispatches the action object. Whenever you want to update the state, you simply call the dispatch function with the appropriate action object: `dispatch(actionObject)`.
* The **initial state** is the value the state is initialized with.
* The **reducer** is a pure function that accepts 2 parameters: the current state and the action object. Depending on the action object, the reducer function must update the state in an immutable manner, and return the new state.

### Workflow

![useReducer() workflow](https://dmitripavlutin.com/5c33affee33e7c40e73028fb48a8367b/diagram.svg)

1. As a result of some event, The dispatch function is called with the action object.
2. React redirects the action object and the current state value to the reducer function.
3. The reducer function uses the action object and performs a state update, returning the new state.
4. React checks whether the new state differs from the previous one. If the state has been updated, the component will be re-rendered and the new state value will be returned by `useReducer()`.


[useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer), [Ultimate Guide to useReducer](https://blog.logrocket.com/guide-to-react-usereducer-hook/), [An Easy Guide to React useReducer() Hook](https://dmitripavlutin.com/react-usereducer/)
