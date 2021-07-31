# Code 201 - Read 06

In this file, a summary of **Read: 06 - JS Object Literals; The DOM** will be provided. The read covers multiple chapters from the book *JavaScript & jQuery: Interactive Front-End Web Development* by Jon Duckett and an article.

## Table of contents

* Article - [Understanding The Problem Domain Is The Hardest Part Of Programming](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming)

* From the Duckett JS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 3    | Object Literals       |
| Chapter 5    | Document Object Model |

## Article:The Problem Domain

### What does "problem domain" mean?

> A problem domain is the area of expertise or application that needs to be examined to solve a problem. A problem domain is simply looking at only the topics of an individual's interest, and excluding everything else.

In other words, it is the information required to define the problem and constrain the solution when writing code. The problem domain includes:

1. The goals that should be achieved.
2. The context within which the problem exists.
3. The rules that define essential functions or other aspects of the code.

A well defined problem domain makes the process of writing code easy, and results in good software. As quoted from the article:
> I was essentially given the entire problem domain in the form of a spec that was clear and unambiguous. I was easily able to learn that problem domain and because of it, I was able to write the code very easily as well.

### Writing code and jigsaw puzzles

The steps of solving a jigsaw puzzle are:

1. Figure out what the major components of the picture are.
2. Sort the pieces by color or component.
3. Put together all the border pieces.
4. Put together each component of the picture from the piles you created.

All these steps will be useless if the picture was unclear and the components can't be identified.

Writing code is mush like putting together a jigsaw puzzle; e put together code with the purpose of building components that we have taken out of the *bigger picture* or the problem domain. So if the *bigger picture* was unclear or blurry; we will not be able to write a well functioning code.

### How to understand the problem domain?

1. Make the problem domain easier - by focusing on fully understanding a particular part of the problem and excluding everything else.
2. Get better at understanding the problem domain - by talking to customers or business people who know about the problem domain and understanding a problem inside and out before trying to solve it with code.

> The more and more I write code, the more I learn that understanding the problem is the most critical piece to the equation. It is very difficult to solve a problem before you know the question.

## Chapter 3: Object Literals [JS]

### What are objects?

Objects are one of JavaScript's data types used for grouping multiple variables and functions. An object consists of:

* Variables become known as **properties**. Properties tell us about the object.
* Function become known as **methods**. Methods represent tasks that are associated with the object.

Objects consist of a set of kay/value pairs, where each property and method have:

* *A name* - The name is called a **key**. An object cannot have two keys with the same name because keys are used to access their corresponding values. 
* *A value* - it can be a number, string, boolean, array, or another object. The value of a method is always a function.

### Creating objects

There are several ways to create objects. The method is being discussed through this read is known as the *literal notation*. Syntax:

```
var objectName = { 
    propertyKey1: value1,
    propertyKey2: value2,
    functionKey: function () { 
        return this.propertyKey1 + ' ' + this.propertyKey2;
        } 
};
```

* Each key is separated from its value using a colon `:`.

* Each property and method are separated by a comma `,`. 

* Each object is defined by a name and its contents is within curly brackets.

* In an object method, the **this** keyword refers to the owner of the method. In other words, `this.propertyKey1` means `propertyKey1` from `objectName` object.

Example:

```
var person = {
  firstName: 'Jon',
  lastName: 'Duckett',
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
```

### Accessing objects

The **dot notation** `.` is used for accessing object properties and methods. This is done using the object name, followed by a dot `.`, then the required property/method name within the object. Syntax: 

```
objectName.propertyKey;
objectNAme.functionName();
```

To console log the full name using the object from the previous example, do the following:

```
console.log(person.fullName())
```

* Another way for accessing properties within objects (but not methods) is to used square brackets `[]`. Syntax:

```
person['firstName'];
```

## Chapter 5: Document Object Model (DOM) [JS]

The Document Object Model (DOM) is a set of rules that specifies: 

* **How browsers should create a model of an HTML page** - when the browser loads a web page, it creates a *model* of the page in memory. The DOM specifies the way in which the browser should structure this model using a *DOM tree*.

The DOM is called an object model because the model (the DOM tree) is made of *objects*. Each object represents a different part of the page loaded in the browser window. 

* **How JS can access and update the contents of a web page while it is in the browser window** - the DOM also defines *methods* and *properties* to access and update each object in this model to update what the user sees in the browser. Scripts access and update the DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in the browser.

***NOTE*** Some people call the DOM an *Application Programming Interface (API)*. APls let programs and scripts interact with each other. The DOM states what the script can ask the browser about the current page, and how to tell the browser to update what is being shown to the user.

***NOTE*** Browsers offer tools for viewing the DOM tree.

### Nodes

Every element, attribute, and piece of text in the HTML page is represented by its own DOM node. DOM trees have four types of nodes (can be seen in Figure .1):

1. **Document/root nodes** - the starting point for all visits to the DOM tree. To access any element, attribute, or text node, you navigate to it via the document node.

2. **Element nodes** - the HTML elements that describe the structure of an HTML page. For example, the `<h1>` - `<h6>` elements describe what parts are headings, and the `<p>` tags indicate where paragraphs of text start and finish.

* The relationships between the document and all of the element nodes are described using the following terms: parents, children, siblings, ancestors, and descendants.

* Every node is a descendant of the document node.

3. **Attribute nodes** - the attributes carried by the opening tag of the elements.

* Attribute nodes are not children of the element that carries them; they are part of that element.

4. **Text nodes** - the text within the elements.

* Text nodes cannot have children. If an element contains text and another child element, the child 
element is a child of the containing element.

![The DOM tree nodes](https://1.bp.blogspot.com/-c1VhRCxc4ds/X5938GT76GI/AAAAAAAACFU/yzX7a1aIinIR_i4sy7dSIW9z8Q5mgX72QCLcBGAsYHQ/s732/dom1.png)

Visiting this link will give additional information about DOM trees and the nodes relationships: [HTML DOM](http://www-acad.sheridanc.on.ca/~jollymor/syst10049/dom.html)


* Each node is an object with methods and properties. 

### DOM queries

The methods that find elements in the DOM tree. The query of an element can be stored in a variable and used more than once. The variable will actually store the location of the element in the DOM tree.

DOM queries may return one element, or they may return a Nodelist; which is a set of nodes.

### Element nodes

#### Finding/selecting element nodes

Element nodes can be selected by:

* Their *ID attribute* - `getElementByld('ID')`

* Their *class attribute* - `getElementsByClassName('class')`

* Their *tag name* - `getElementsByTagName('tagName)`

* Using *CSS selector* - `querySelector('css selector')`

#### Getting/updating element content

There are two approaches to add/remove content from the DOM tree:

* Using properties such as `textContent` and `innerHTML`. This can update entire fragments. 

The `innerHTML` property can be used to:

1. Get HTML from an element,this property will get the content of an element and return it as one long string, including any markup that the element contains.

2. Set new content for an element, it will take a string that can contain markup and process that string, then add it to the DOM tree.
Be careful when using this property to add content because one missing closing tag could throw out the design of the entire page.

* Using DOM manipulation techniques. It targets individual nodes in the tree. This approach involves three steps:

1. Create the element - the `createElement()` is used to create a new element node. This element node is stored in a variable.

2. Give it content - the `createTextNode()` is used to create a new text node, also stored in a variable. To add this text node to the element node use the `appendChild()` method. This step can be skipped if you want to add an empty element to the DOM tree.

3. Add it to the DOM - the `appendChild()` method is used to add the element to the DOM tree.