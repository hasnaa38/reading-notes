# Code 301 - Read 10

In this file, a summary of **Read: Class 10 - FUNCTIONAL PROGRAMMING** will be provided.

## JavaScript Call Stack

[The JavaScript Call Stack - What It Is and Why It's Necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

The **JavaScript engine** is a single-threaded interpreter comprising of a heap and a single call stack. It is found in a hosting environment like the browser. The browser provides web APIs like the DOM, AJAX, and Timers.

A **call stack** is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call). Since the js engin has a single call stack, calls are done one at a time, from top to bottom. It means the call stack is `synchronous`.

* What is a ‘call’?

A function invocation.

* How many ‘calls’ can happen at once?

Only one.

* What does LIFO mean?

Last In, First Out - it is a data structure principle in which the last function that gets pushed into the stack is the first to be popped out, when the function returns.

* Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

![call stack example](https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Call-Stack.png)

What happens here is:

1. main() wat executed so an empty stack frame is created. This is the entry point of the program.
2. main() calls average() so average() is pushed into the stack.
3. average() calls add() so add() is pushed into the stack.
4. when add() finishes executing, it gets popped off the stack.
5. The execution order moves back to average().
6. When average() finishes executing, it gets popped off the stack.
7. The execution order moves back to main().
8. When main() finishes executing, it gets popped off the stack, clearing the memory.

* What causes a Stack Overflow?

A stack overflow occurs when there is a recursive function - function that calls itself without an exit point. The browser has a maximum stack call that it can accommodate before throwing a stack error: *maximum call size exceeded*.

In **asynchronous** JS functions, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

## JavaScript error messages

[JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

* What is a ‘refrence error’?

It is an error that occurs when you try to use a variable that is not declared yet.

* What is a ‘syntax error’?

It is an error that occurs when you have something that cannot be parsed in terms of syntax.

* What is a ‘range error’?

It is an error that occurs when you give it an invalid length to an array.

* What is a ‘tyep error’?

It is an error that occurs when the types (number, string, etc) you are trying to use/access are incompatible

* What is a breakpoint?

A point in which JS will stop executing and let you examine JavaScript values when it reaches.

* What does the word ‘debugger’ do in your code?

It stops the execution of JavaScript, and calls the debugging function if it was available.
