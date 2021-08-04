# Code 201 - Read 10

In this file, a summary of **Read: 10 - JS Debugging** will be provided. The read covers chapter 10: “Error Handling & Debugging”, from the book *JavaScript & jQuery: Interactive Front-End Web Development* by Jon Duckett.

## Chapter 10: Error Handling & Debugging [js]

### Order of execution

The order in which the interpreter is processing and executing the statements of a scripts.

The interpreter processes code line-by-line. When a statement needs data from another function, the interpreter **stacks** (piles) the function on top of the current task.

### Execution context

There is only one global execution context in any page. Whereas the code being run within a function has its own function context.

![Execution context](https://res.cloudinary.com/practicaldev/image/fetch/s--Dm0VYkB8--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/l7avn35tb8ua5fl4gnoh.png)

If a variable is declared outside a function, it can be used anywhere, this is known as global scope. But when a variable is declared within a function, it can only be used within that function, this is known as function-level scope.

Each time a script enters a new execution context, there are two phases of activity:

1. Prepare - The new scope is created. Variables, functions, and arguments are created. The value of the *this* keyword is determined.
2. Execute - Assign values to variables. Reference functions and run their code. Execute statements.

Each execution context also creates its own `variables` object. This object contains details of all of the variables, functions, and parameters for that execution context.

Each execution context can also access its parent's variables object. If a variable is not found in the current execution context variables object for the, the interpreter will look in the variables object of the parent execution context.

### Hoisting

Hoisting is JavaScript's default behavior of moving declarations to the top. The preparation of all the variables and functions and hoisting them to the top of the execution context allows you to:

1. Call functions before they have been declared.
2. Assign a value to a variable that has not yet been declared.

### Errors

If you are anticipating that something in your code may cause an error, add a set of statements to handle the error. Those are known as the **error-handling code**. 

Whenever the interpreter comes across an error, it will look for error-handling code. If the error is not handled, the script will stop processing, create an `error` object, and the user will not know why.

If an error happens in a function and the function does not have an error handling code, the interpreter goes through the stack to find one until it reaches the global context. If there is still no error handler, the script stops running and the `error` object is created. Error objects can help you find where your mistakes are.

JavaScript has 7 different types of errors (therefore, error objects):

* Error -the prototype from which all other error objects are created. 

* Syntax error - caused by incorrect use of the rules (syntax) of the language.

* Reference error - caused by a variable that is not declared or is out of scope.

* Type error - caused by trying to use an object or method that does not exist. 

* Range error - caused when calling a function using numbers outside of its accepted range.

* URI error - If these characters are not escaped in URls: `/ ? & I : ;`

* Eval error - the `eval()` function evaluates JavaScript code represented as a string. This error object indicates an error regarding this function.

***Note*** - when performing a mathematical operation using a value that is not a number, you end up with the value of **NaN**, not a type error.


### How to deal with the errors

1. Debugging - it is all about deduction; eliminating potential causes of an error.

* JavaScript *console* can help while debugging errors.

* *Breakpoints* can pause the execution of a script on any line. You can use it to check the values stored in variables at that point in time. If you set multiple breakpoints, you can step through them one-by-one to see where values change and a problem might occur.

2. Using try, catch, throw, and finally statements:

```
try {

    // Add the code that you think might throw an exception

}

catch (exception) {

    // If the try code block throws an exception, add an alternative code here

}

finally {

    // Always executed whether the try block succeeded or failed

}

```
