# Code 401 - Read 39

## Revision

* What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

using the `useEffect()` hook.

* When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

the reducer function.

## Terms Documentation

* **middleware**: anything you put in the middle of one layer of the software and another to do a specific thing.
* **thunk**: the Redux's official version of async function middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments.

## Preview - Redux Toolkit

It is Redux's official, opinionated, batteries-included toolset for efficient Redux development.

*opinionated* - the Redux core library is unopinionated; it lets you decide how you want to handle everything. This gives you flexibility, but that flexibility isn't always needed.

Redux Toolkit includes several utility functions that simplify the most common Redux use cases, including store setup, defining reducers, immutable update logic, and even creating entire "slices" of state at once without writing any action creators or action types by hand. It also includes the most widely used Redux addons, like Redux Thunk for async logic and Reselect for writing selector functions, so that you can use them right away.
