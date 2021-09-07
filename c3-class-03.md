# Code 301 - Read 03

In this file, a summary of **Read: Class 03 - Passing Functions as Props** will be provided.

## Topic 1 - lists and keys

[Article](https://reactjs.org/docs/lists-and-keys.html)

### Lists

To create a component that accepts an array and outputs a list of elements:

```
NumberList = (props) => {
  let numbers = props.numbers;
  let  listItems = numbers.map((number) =>
  //to get a <li> element for each item:
    <li>{number}</li>
  );
  return (
    //to generate an <ul> out of the <li> items:
    <ul>{listItems}</ul>
  );
}

let numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

### Keys

A key is a special string attribute. It helps React identify which items have changed, are added, or are removed. They are given array elements to give them a stable identity.

Keys used within arrays should be unique among their siblings, but they don’t need to be globally unique.

Keys serve as a hint to React but they don’t get passed to components. If the same value needs to be passed to a component, it should be passed as a prop with a different name.

Keys are included when creating lists of elements. For the previous example, keys will be assigned to the list items inside numbers.map():

```
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

### Questions

* What does `.map()` return?
A new array composed of the results of calling a function for every input-array element.

* If I want to loop through an array and display each value in JSX, how do I do that in React?

1. Use `.map()` with a function that displays the array values as I want.
2. Create an array that holds the output of `.map()`.
3. Render the final array.

Note: JS inside JSX elements are added within curly braces `{}`.

* Each list item needs a unique *identifier; string that identifies the list item among its siblings*.

* What is the purpose of a key?
It helps React identify the items that have changed, are added, or are removed. They are given to the elements inside the array for them -the array elements- a stable identity.

## Topic 2 - The Spread Operator

[Article](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

The spread operator is an ES6 syntax used for expanding an iterable (object, array, string) into individual elements, i.e, adding items to arrays, combining arrays or objects, or spreading an array out into function arguments.

syntax: `...`

Example of using it to spread an array into arguments:

```
console.log(Math.max(...[7,12,3])); // will log 12 to the console
```

### Questions

* What is the spread operator?
It is an ES6 syntax used for expanding an iterable (object, array, string) into individual elements.

* List 4 things that the spread operator can do.

1. Using Math functions
2. Copying an array
3. Combining arrays / objects
4. Adding to state in React

* Give an example of using the spread operator to combine two arrays.

```
let array1 = [1,2,3,4,5];
let array2 = [6,7,8,9,10];
let array1_2 = [...array1,...array2];
console.log(array1_2);
```

* Give an example of using the spread operator to add a new item to an array.

```
let array1 = [1,2,3,4,5];
let item = 'hi';
let array_i = [...array1, item];
console.log(array_i);
```

* Give an example of using the spread operator to combine two objects into one.

```
let object1 = {name:'Aseel', age:23};
let object2 = {hobby: 'drawing'};
let object1_2 = {...objectOne, ...objectTwo};
console.log(object1_2);
```

## Topic 3 - How to Pass Functions Between Components

[Video](https://www.youtube.com/watch?v=c05OL7XbwXU)

### Steps:

When having a state in a higher component and a lower component that is triggering something at that state, do the following:

* In the higher element:

1. The main change-of-state function is created wherever the state is going to be changed, which is here.
2. Pass the change-of-state function to the lower component as a prop through the render method.

* In the lower component:

1. Inside the change-of-state function for this component, call that method as if it is a value prop: `this.props.function(this.props.parameter);`
2. Add this function to the event handler.

### Questions

* In the video, what is the first step that the developer does to pass functions between components? He passed the function as if it a prop from the higher component to the lower component.

* In your own words, what does the increment function do?
It increments the count for the person when the person's Add button is being clicked.

* How can you pass a method from a parent component into a child component?
Answered in steps.

* How does the child component invoke a method that was passed to it from a parent component?
It will invoke its own change-of-state method when the event occurs which has the parent's change-of-state method passed down to it as a prop. The child's change-of-state method will pass a value through the parent's change-of-state method so it will trigger the change.
