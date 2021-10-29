# Code 401 - Read 01

## Review, Research, and Discussion

* Array.map() method creates a new array with the same length as the original array and with the results of executing a function for every element of the original array in order.

* Array.reduce() method executes a reducer function for each element of an array and returns a single value, which is the function's accumulated result. This value can be an integer, string, array, or object.

* Using superagent() to fetch data from a URL with normal Promise .then() syntax:

```
const superagent = require('superagent');

// Using geocode.xyz api to receive data about Amman:
superagent.get('https://geocode.xyz/amman?json=1').then(reply => {
    console.log(reply.body);
}).catch(error => {
    console.error(error);
});
```

* Using superagent() to fetch data from a URL with async/await syntax:

```
const superagent = require('superagent');
let geoAmman = async () => {
    let ammanData = await superagent.get('https://geocode.xyz/amman?json=1');
    try {
        console.log(ammanData.body);
    } catch(error) {
        console.error(error);
    }
}
geoAmman();
```

* Promises:

A producing code is code that can take some time to be executed. A consuming code is code that must wait for the result from the producing code.

A Promise is a JavaScript object that links producing code and consuming code. In other words, it represents the eventual completion or failure of asynchronous operations in JavaScript.

Promises help with:
1. Improving code readability
2. Better handling of asynchronous operations
3. Better flow of control definition in asynchronous logic
4. Better Error Handling

A Promise has four states: 
* *Resolved*: Action related to the promise succeeded.
* *Rejected*: Action related to the promise failed.
* *Pending*: Promise is still pending - not resolved nor rejected yet.
* *Settled*: Promise was resolved or rejected.

The Promise constructor takes one argument, a callback function. The callback function takes two arguments, resolve and reject.
The operations are performed inside the callback function, if everything went well, call resolve. If not, call reject. This can be seen in the following code snippet and figure .1

```
new Promise( (resolve, reject) => {
    // operations
    if(condition) {
        resolve(//something);
    } else {
        reject(//something);
    }
});
```

![promises figure .1](https://javascript.info/article/promise-basics/promise-resolve-reject.svg)

An example of an authentication promise can be seen in figure .2.

![promises figure .2](https://vitalflux.com/wp-content/uploads/2016/02/promise.png)

* Are all callback functions asynchronous? No, why not?

A callback is a pattern by which a function is passed as a parameter to an higher order function and is called back to it or further down the stack.

The callback will be synchronous/asynchronous depending on how the higher order function that calls it will call it:

* It will be synchronous when the higher order function which calls it is calling it synchronously.
* It will be asynchronous if it is called within the context of the execution branch of an asynchronous operation. Further, for a function to be asynchronous it needs to perform an asynchronous operation. For example:
    1. Timer functions - setTimeout, setInterval
    2. Special functions - nextTick, setImmediate
    3. Performing input/output operations - listening to network, querying a database, reading or writing from a resource
    4. Subscribing to an event
