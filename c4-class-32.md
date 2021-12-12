# Code 401 - Read 32

## Revision

* When you have multiple contexts, what component type should you use (class/function) and why?

function component. Because we can use the `useContext()` hook to consume those multiple hooks in the same component.

* What are some good use cases for using the Context API for global state?

site configuration settings (theme, preferred language, etc), or logged-in user data.

* How can you best test context?

Test if the child components are consuming its values or not.

## Terms Documentation

* **context**: a method that provides a way to share data between components globally without having to explicitly pass a prop through every level of the tree. It is designed to share data that can be considered global for a tree of React components.
* **useContext()**: a React hook used to allow the component from consuming a Context.
* **static context**: a way for class-based components to get access to Context without using the `Context.Consumer` component. To use this way, a static property called contextType should be declared and sat to equal to the full context. It has to be static, which means that this property can be accessed from outside without the need to instantiate an object based on this class first. This allows React to automatically connect this class component to context and it gives you a new property - `this.context` property, which we can use. [Resource](https://dev.to/olenadrugalya/what-is-contexttype-1b75)

## Preview - Context API - Behaviors

Context localizes the state of the app so it becomes a single centralized component. That same centralized component can be responsible for rendering them. It also allows accessing the management of that state (adding, removing) globally.

The context provider is responsible for both displaying the local state of the context object, and for exposing an API for globally managing them.

The context consumer is a component that accesses the Context. There are three ways to get the context values:

1. wrapping the component with the Context's consumer and use as props:

```
<MyContext.Consumer>
{value => 
  <SomeComponent value={value}/>
}
</MyContext.Consumer>
```

2. using static contextType:

```
static contextType = MyContext;
```

3. using the `useContext` hook (Functional components only)

```
const myContextValue = useContext(MyContext);
```

There’s a lot of buzz around how you can replace a lot of what Redux does with  and . The combination of the `useContext` and `useReducer` hooks means it’s possible to have a global state and use Redux-like reducers, actions, and dispatchers to mutate that global state.
