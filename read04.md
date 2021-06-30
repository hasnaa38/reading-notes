# read 04 
In this file a summary of *Read 04 - Dynamic web pages with JavaScript* will be provided. The file includes a summary of multiple articles, them being: 
[JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) // [Input Output in plain JavaScript](https://code-maven.com/input-output-in-plain-javascript) // [JavaScript Variables](https://www.w3schools.com/js/js_variables.asp)

## JavaScript
JavaScript -or in short, JS- is a lightweight, interpreted and compiled programming language, used to add functionality to web applications using a set of instructions. 

JS can be used while programming the front-end (client-side) or the back-end (server-side). Some examples of things that can be done using JS in the front-end:

1. Prompt inputs from users and store them as variables. 
2. Apply operations on variables. 
3. Running code in response to certain events occurring on a web page.

## Adding JS to HTML 
JavaScript can be applied to HTMLs page using the `<script>` element. There are two styles of doing so: 

1. **Internally** - the script can be added directly inside the HTML page wrapped by the `<script>` element, it should look like this: 
```
<script> JS goes here </script>
```

2. **Externally** - the script can be written in a different file (with .js extension) then linked to the HTML page also using the `<script>` element and the `src` attribute. Linking a js file called script.js should look like this: 
```
<script src="script.js"></script>
```
_**Note**_ it is preferred to link external js scripts at the end of the `<body>` element of the code. 

## JS variables 
A variable is a container for a value. 
To create/declare a variable, use the `var` keyword, followed by the name you want to call the variable. For example, to declare a variable called myName, use the following code: 
```
var myName 
```

To assign a value for the varable, use the assignment operator `=`. For example: 
```
var myName = "Hasnaa" 
```
_**Note**_ You can't assign a value to an undeclared variable. 

The value of a variable can be changed/update along the code, the variable will always keep the most recent value that has been declared to it. 

To check the value of a variable on the console, use `console.log(variable-name)`. 

## DataTypes
The data type defines the values a variable can take and the operations that can be performed on it. The main data types we use: 
- **Number**, js treats all number types as one, i.e. you don't have to specify if a number is an integer or a floating point, both of these are just numbers. 
To declare a variable called myAge with a number value use the following code: 
```
var myAge = 23
```

- **String** - a string is a pieces of text. To declare a variable with a string value, the value should be wrapped in single or double quote marks; otherwise, JavaScript tries to interpret it as another variable name. For example: 
```
var myName = "Hasnaa" 
```

- **Boolean** - a boolean is simply *true* or *false*. 

To check the type of data on the console, use the `typeof` operator: 
```
console.log(typeof myName) 
```

## operators 
There are many operators used for JS, i.e. 
- **Arithmetic operators**

| Operator      | Meaning |
| ----------- | ----------- |
| + | Addition or concatenation (with strings)|
| - | Subtraction |
| * | Multiplication |
| / | Division |

- **Comparison operators** - the type of the result is a boolean 

| Operator      | Meaning |
| ----------- | ----------- |
| == | Equal to in value |
| != | Not equal to in value |
| === | Equale to in value and type |
| !== | Not equale to in value and type |
| > | Greater than |
| < | Less than |


## Other operators
* `alert("text")` - shows text to the user in a pop-up box.

* `var result = prompt("text")` - shows a pop-up box that takes data from the user, then saves it in the variable result. 
* `document.write("text")` - shows text to the user in the HTML page. 
