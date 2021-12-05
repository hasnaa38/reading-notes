# Code 401 - Read 28

## Revision

* Why do we not need more .html pages in a multi-page React app?

Because React creates single-page applications that interacts with the web browser by rewriting the content of index.html dynamically, instead of the default method of the browser loading entire new pages.

>> When building your react-app, you can see that there is only one App.js from where your entire web-app is loaded in fragments and components. This behavior of rendering components and pages on a single page and changing the DOM( is a single page behavior and hence the name), instead of loading a new page with new content, this makes it feel like a single application.

However, React Router can be used to display multiple views in a single page application.

* If we wanted a component to show up on every page, where would we put it and why?

Inside the `<BrowserRouter />`, outside a `<Route />`. The `<BrowserRouter />` component is the core of the React Router application, it is used to keep the UI in sync with the URL. The `<Route />` component is a route matching component, it is used to render the proper component that matches the current URL.

* What does routing do with the components that were rendered when a new route is requested.

It will unmount the previous component.

* What does `props.children` contain?

`props.children` is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component. So it contains the content of a component. In the following example, the string `'Hello world!'` is the `props.children` for `<MyComponent>`

```
<MyComponent>Hello world!</MyComponent>
```

[more](https://hackernoon.com/introduction-to-props-children-in-react-661e1b6e45c3)

* How do `useState()` and `this.setState()` differ?

`useState()` is a Hook that updates the state in functional components, `setState()` updates state in class components.

## Terms Documentation

* **State Hook**: a built-in React Hook used inside the a function component to add the React state feature.

* **Mounting**: the process of outputting the virtual representation of a component into the final UI representation.

* **Un-Mounting**: the process of removing a component from the DOM

## Preview - The Effect Hook

The Effect Hook lets you perform side effects in function component. It is used to run some additional code after React has mounted the component/updated the DOM. It is similar to `componentDidMount()` and `componentDidUpdate()` in class components.

There are two common kinds of side effects in React components:

1. **Effects that don’t require cleanup**, network requests, manual DOM mutations, and logging for example. These effect don't require cleanup because we can run them and immediately forget about them.

```
useEffect(() => {
    document.title = `You clicked ${count} times`;
});
```

In this example, `useEffect()` will tell React that the component needs to do something after render. React will remember the function passed inside it (the effect), and call it later after performing the DOM updates.

By default, `useEffect()` runs both after the first render (when mounting) and after every update. React guarantees the DOM has been updated by the time it runs the effects.

2. **Effects that require cleanup**, every effect may return a function that cleans up after it. This lets us keep the logic for adding and removing a part of the same effect. Example on this case is setting up a subscription to some external data source, a clean up is important to avoid memory leaks.

```
useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    // Specify how to clean up after this effect:
    return function cleanup() {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });
```

React performs the cleanup when the component unmounts. However, effects run for every render and not just once. This is why React also cleans up effects from the previous render before running the effects next time.

### Separating concerns

Several `useEffect()` effects can be used to separate unrelated logic into different effects. React will apply every effect used by the component, in the order they were specified.

[link](https://reactjs.org/docs/hooks-effect.html)