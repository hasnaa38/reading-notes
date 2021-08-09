# Code 201 - Read 13

In this file, a summary of **Read: 13 - Local Storage** will be provided. The read covers an [article](http://diveinto.html5doctor.com/storage.html).

## Web Storage Introduction

Aka *Local Storage* or *DOM Storage*, a way for web pages to store data locally; within the client web browser, with no expiration date. This means the data stored in the browser will persist even after the website/browser window is closed. Unlike cookies, this data is never transmitted to the remote web server, as it is implemented natively in web browsers; so it is available even when third-party browser plugins are not.

This specification was a part of HTML5 specification, but then was split out into its own specification.

The JS `localStorage` object allows you to access local storage via the `window.localStorage` property. This property is a *read-only* property that returns a reference to the local storage object. It is only accessible to the origin that created it.

## Web Storage Data

The data in this storage is based on *named key/value* pairs: data is stored based on a named key, then that data can be retrieved with the same key.

The data can be any type supported by JavaScript: numbers, strings, Booleans, etc. The named key is a **string**, so to retrieve anything other than strings, use data type conversion functions like `parseInt()` or `parseFloat()`.

## Local Storage Methods

* The `setItem()` method is used to store data to `localStorage`. It takes two parameters: a *key* and a *value*. If the key already exists, it will silently overwrite the previous value.

* The `getItem()` method is used to retrieve  data from `localStorage`. It accepts only one parameter; the key, and returns the value as a string. For a non-existent key, it will return `null` rather than throw an exception.

square brackets can be used instead of `setItem()` and `getItem()` methods. Examples:

```
localStorage.setItem('bar', foo);
let foo = localStorage.getItem('bar');
```

OR

```
localStorage['bar'] = foo;
let foo = localStorage['bar'];
```

* The `removeItem()` method is used to remove an item by key from `localStorage`.

* The `clear()` method clears all `localStorage` data.

* The `key()` method Passes a number to retrieve the key of a `localStorage`.

## Storage Event

To keep track of the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever `setItem()`, `removeItem()`, or `clear()` is called and actually changes something. Example:

```
window.addEventListener("storage", handle_storage);
```

In this example, the *handle_storage* callback function will be called with a `StorageEvent` object.

The storage event has the following properties:

* key - it is a string that is the named key which was added, removed, or modified.
* oldValue - the previous value (now overwritten), or null if a new item was added.
* newValue - the new value, or null if an item was removed.
* url - it is a string that is the page which called a method that triggered this change.

## Local Storage Limitations

1. Each origin gets 5 MB storage space by default across all major browsers. If you exceed your storage quota, you will get the following exception: `“QUOTA_EXCEEDED_ERR”`.
2. It is not a substitute for a server based database as information is only stored on the client's browser.
3. It only stores strings, not data in its original format. Therefore, the difference in representation may add up. For example: each digit in floating point number is being stored as a character.