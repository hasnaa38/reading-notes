# Code 401 - Read 38

## Revision

* How granular should your reducers be?

They should handle a singular change and be predictable.

* Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

A pro, if multiple states in multiple components need to change at the same time, so each reducer can provide a different logic to the same dispatcher.

* Name a strategy for preventing the above

Making a reducer for each component that will be affected by the dispatcher.

## Terms Documentation

* **store**:  a plain JavaScript object that allows components to share state.
* **combined reducers**: a Redux helper function that turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

## Preview - Redux - Asynchronous Actions

### Async Logic and Data Fetching

Most real applications need to work with data from a server, by making HTTP API calls to fetch and save items.

By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

A **side effect** is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like: logging a value to the console, saving a file, or making an HTTP request. Redux reducers must never contain side effects. **Redux middleware** were designed to enable writing logic that has side effects.

Redux middleware can enable us to write some kind of async logic that interacts with the Redux store.

### Async data flow

1. handling a user event in the application
2. calling `dispatch()`, and pass in something
3. the dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes

![image1](https://miro.medium.com/max/760/0*Q4lgrUkqEFvvoUzZ)

### Redux Thunk Middleware

Thunk middleware is Redux's official version of async function middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.

![image2](https://d33wubrfki0l68.cloudfront.net/08d01ed85246d3ece01963408572f3f6dfb49d41/4bc12/assets/images/reduxasyncdataflowdiagram-d97ff38a0f4da0f327163170ccc13e80.gif)

[more](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)