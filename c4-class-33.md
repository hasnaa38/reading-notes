# Code 401 - Read 33

## Revision

* Why is the Context API useful?

Because it makes the process of sharing and managing global states easier than using prop drilling.

* Can a component outside of a provider get its context?

If the component wasn't wrapped with the provider it can't. But any component wrapped with the provider can use it if it was marked as a consumer, used the static contextType or using the useContext hook.

* What are some common use cases for using the Context API?

site configuration settings (theme, preferred language, etc), or auth and logged-in user data.

* Describe “Context Hell”

it is the mess you get from nesting multiple Context.Providers and passing them as children of each other

## Terms Documentation

* **global state**: state data that is shared and can be accessed by all the components within a React application
* **global context**: a way to share and manage global state to all components within a React application without using prop drilling
* **provider**: a React component that allows consuming components to subscribe to context changes
* **consumer**: any React component that is subscribed the the context provider to access and manage the provider's global state

## Preview - Login and Auth

### Role Based Access Control

It is the approach of restricting system access to authorized users based on their role in an organization.
With the proper implementation of RBAC, the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.

### RBAC variations:

1. *Access control lists (ACL)* - defining access rights by a given user or user group, to a specific object, such as a document. Example: allowing users from one department to make changes to a document, while only allowing users from other departments to read the document.
2. *Attribute-based access control (ABAC)* - sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.

### RBAC implementation

1. Inventory the systems: list what resources you have for which you need to control access.
2. Analyze the workforce and create roles: group your workforce members into roles with common access needs. Keep them as simple and stratified as possible.
3. Assign people to roles: now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.
4. Never make one-off changes: only apply changes when necessary.
5. Audit: periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role.

### React-Cookies Component

Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them.

The **react-cookie** package is used to load and save cookies with React.

For the following example code, the username and password will be taken from the user and stored as a cookie in the user’s computer.

#### Setting cookies

1. in the root app component of the application `index.js` -> import the `CookiesProvider` component from the react-cookie package and wrap the component with it:

```
import { CookiesProvider } from "react-cookie";
ReactDOM.render(
   <CookiesProvider>
      <App />
   </CookiesProvider>,
   document.getElementById('root')
);
```

2. in the component were you want to set the cookies, import and use the `useCookies` hook provided by the package and use it to set the cookie:

```
const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
```

* **Cookies**: an object with all of the user’s cookies.
* **setCookie**: a function to set the cookies.
* **removeCookie**: a function to remove the cookies.

#### Retrieving cookies

After the cookies have been set, they can be accessed by writing `cookies.{cookie key name}`
