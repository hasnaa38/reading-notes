# Code 301 - Read 01

In this file, a summary of **Read: Class 01 - Introduction to React and Components** will be provided.

## Topic 1 - Component Based Architecture

[Article](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

### What is a component?

A component is a modular, portable, replaceable, and reusable software unit that encapsulates the functionality and behavior of software elements.

### What are the characteristics of a component?

1. **Reusable** − can be be reused in different situations in different applications.
2. **Replaceable** − they can be substituted with other similar components.
3. **Not context** specific − they can operate in different environments and contexts.
4. **Extensible** − they can be extended from existing components to provide new behavior.
5. **Encapsulated** − they have interfaces that allow the caller to use its functionality without exposing any internal details.
6. **Independent** − they are designed to have minimal dependencies on other components.

### What are the advantages of using component based architecture?

1. **Reusable** - components can be re-used across several applications or systems if needed.
2. **Independent** − each component is developed separately to encapsulate a certain functionality/behavior. Therefore, different components can be developed in parallel.
3. **Easy to develop, deploy, and modify** − since components are independent of each other, they can be developed, deployed, or modified without affecting other components or the system as a whole.
4. **Reliable** − the reliability of each individual component increases the reliability of the overall system.
5. **System maintenance and evolution** − it is easy to change and update the implementation without affecting the rest of the system.
6. **Reduces the cost** − using third-party components may reduce the cost of development and maintenance.

## Topic 2 - Props

[Article](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0#:~:text=%E2%80%9CProps%E2%80%9D%20is%20a%20special%20keyword,way%20from%20parent%20to%20child)

Props are used to pass data from one component to another. Therefore, they allow communication (data exchange) between system components.

### What is props short for?

`Props` is a React keyword that stands for *properties*.

### How are props used in React?

To see how we will use props, we will use the following example:

* The parent component:

```
class ParentComponent extends Component {  
  render() {
    return (
      <div>
        <h1>I'm the parent component.</h1>
        <h3><ChildComponent/></h3>
        <h3><ChildComponent/></h3>
        <h3><ChildComponent/></h3>
      </div>
    );
  }
}
```

* The child component:

```
const ChildComponent = () => {  
  return <p></p>; 
};
```

Steps:

1. Define attributes and assign values to them:
In this example, a `text` attribute was declared to the child component and then assigned different string values:

```
class ParentComponent extends Component {  
  render() {
    return (
      <div>
        <h1>I'm the parent component.</h1>
        <h3><ChildComponent text=“I’m the 1st child”/></h3>
        <h3><ChildComponent text=“I’m the 2nd child”/></h3>
        <h3><ChildComponent text=“I’m the 3rd child”/></h3>
      </div>
    );
  }
}
```

2. Pass data with props and render it:

* Props are passed to the child component like function arguments.
* Props returns back an object. To access the props object element we need (the text property) we will use the dot(.) notation.
* Finally, each child component will render its own prop data.

```
const ChildComponent = (props) => {  
  return <p>props.text</p>; 
};
```

Result:
![result](https://miro.medium.com/max/700/1*Kd52H-jKv6N1Cwgnaz4tOA.png)

### What is the flow of props?

Props have a *uni-directional flow*, in which data is passed one way from the parent component to the child components.
Furthermore, props data is *read-only*; data coming from the parent component can't be changed by the child components.

## Things I want to know more about

State.