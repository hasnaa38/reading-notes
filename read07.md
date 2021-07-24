# read 07 
In this file a summary of *Read: 07 - Programming with JavaScript* will be provided. The file includes a summary for multiple articles, them being: 
[Control flow](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow) // [JavaScript Functions](https://www.w3schools.com/js/js_functions.asp).

## Topic 1 - Control Flow 

It is is the order in which a computer executes statements in a script.
Computers run the statements of any code from the first line in the file to the last line, unless a structures that change the control flow is executed; such as conditionals and loops. 

## Topic 2 - JavaScript Functions
A JavaScript function is a block of code used to organize a code and perform a particular task multiple times.
Functions are executed when we invokes it (i.e. call it).

### JavaScript function syntax

```
function name(parameters) {
  code block
}
```

- we begin by adding the `function` keyword. 
- we can add parameters if they were needed. The parameters allow us to pass values to the function. 
- we add the code we aim to perform when calling the function between `{}`. 



## Invoking a function
The code block inside a function will be executed when the function is being called. To call a function just write its name and pass the required parameters to it -if any-. 

## Function return 
When JavaScript reaches a return statement, the function will stop executing and the return value is returned back to the caller.
For example: 
```
function mySum(a, b) {
  return a+b; 
}
console.log(mySum(3,8))
```

Running this code will result in `11` on the console. 

_**Note**_ Variables declared within a function are local variables; therefor they can only be accessed from within the function. 