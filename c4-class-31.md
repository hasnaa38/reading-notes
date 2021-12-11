# Code 401 - Read 31

## Revision

* Describe use cases `useState()` vs `useReducer()`

`useState()` is used for simple state management, conditional rendering, and flag toggling. This method is built on top of the `useReducer()` method.

The `useReducer()` is usually preferable for complex state logic that involves multiple sub-values or when the next state depends on the previous one. It also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

* Why do custom hooks need the use prefix?

Since custom hooks are normal functions, custom hooks need the use prefix to tell at a glance that the rules of Hooks apply to this function.

* What do custom hooks usually do?

They allow us to reuse stateful logic so we can have cleaner functional components, remove logic from the UI layer, and prevent code duplication.

* Using any list of custom hooks, research and name one that you think will be useful in your applications

The `useUpdate` hook. It allows triggering a component re-render manually.

[More  -10 Useful Custom React Hooks](https://javascript.plainenglish.io/10-useful-custom-react-hooks-f24f4307524b)

* Describe how a hook that fetches API data might work

It can use the `useEffect()` hook to run a function when receiving a message from the API, this function fetches the incoming data and use the `useState()` \ `useReducer()` hooks to update the state with the new data.

## Terms Documentation

* **Reducer**: a function that determines changes to an application’s state based on an action it receives to determine the change. This function takes previous state and action as arguments, and returns the next state.

[More - Understanding How Reducers are Used in Redux](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)

## Preview - Context

In a typical React application, data is passed top-down (parent to child) via props. This approach is known as prop drilling and it can be complicated when data needs to be accessible by many components at different nesting levels, such as the current authenticated user, theme, or preferred language.

Context provides a way to share data between components globally without having to explicitly pass a prop through every level of the tree. Context is designed to share data that can be considered global for a tree of React components.

![prop drilling vs context](https://www.carlrippon.com/static/0d1f722d0fe4c2bc4c3d71595dbe67dd/ca682/prop-drilling-v-context.png)

![using context example](https://uploads.toptal.io/blog/image/129071/toptal-blog-image-1549323314875-d6bc9c753a4c9ac2911e8af17732023d.png)

### Steps

1. Initializing the Context

First, we need to create the context, which we can later use to create providers and consumers.

File: **MyContext.js**

```
const MyContext = React.createContext(defaultValue);
...
export default MyContext;
```

The `createContext` property creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree. The defaultValue argument is only used when a component does not have a matching Provider above it in the tree.

2. Creating the Provider

We can import the context and use it to create our provider.

File: **MyProvider.js**

```
<MyContext.Provider value={/* some value */}>
```

Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers.

Providers can be nested to override values deeper within the tree.

All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes.

To make the provider accessible to other components, we need to wrap our app with it. So in `App.js`:

```
return (
            <MyProvider>
                <div className="App">
                   ...
                </div>
            </MyProvider>
        );
```

3. Creating the Consumer

We’ll need to import the context again and wrap our component with it which injects the context argument in the component. Then you use context since holds all the values, the same way you would use props.

```
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```

A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree.
