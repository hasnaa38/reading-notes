# Code 201 - Read 04

In this file, a summary of **Read: 04 - HTML Links, CSS Layout, JS Functions** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett and an online article.

## Table of contents

* From the Duckett HTML and CSS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 4    | Links       |
| Chapter 15   | Layout      | 

* From the Duckett JS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 3    | Functions, Methods, and Objects, pages 86-99 |

* Article: [*6 Reasons for Pair Programming*](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

## Chapter 4: Links [HTML]

* Links are HTML objects that enable the idea of web browsing\surfing; by moving users from one web page to another.

* Links are created using the anchor element `<a>`. Syntax:

```
<a href="URL">Link Text</a>
```

* The **href** attribute is used to add the link's destination.
* The **link text** is the clickable text that moves the user.

### Destination options

1. Another page from another website- the value of the `href` attribute will be the full web address for that page; aka *the absolute URL*.

2. Another page within the same website (repository) - the value of the `href` attribute is the path of the intended file; aka *the relative URL*. The relative URL specifies the destination according to the page's relation to the current page.

3. An email - add `mailto:` followed by the email address. When a user clicks this link, their email will compose a new email message addressed with the specified mailto address. Example:

```
<a href="mailto:email address">Email Us</a>
```

4. Specific part on the same page - before doing so, you should add an **id** to the aimed element. The value of the `href` attribute will be `#id` of that part. Example:

```
<a href="#aimedPara">Go to paragraph</a>
<p id="aimedPara">This is the paragraph we aim to jump to by clicking on the link</p>
```

5. Specific part on another page (whether on the same site or a different one) - before doing so, you should be able to have the **id** of the intended element. The value of the `href` attribute would contain the address of the page (either the absolute URL or the relative URL), followed by `#id` of the element. Example: 

```
<a href="URL/#bottom">
```

### Opening the link in a new window

Links can be opened in a new window using the `target` attribute. The value of this attribute should be `_blank`. Example:

```
<a href="URL" target="_blank">Link Text</a> 
```

## Chapter 15: Layout [CSS]

CSS treats each HTML element as if it lives in its own box, which will either be a *block-level box* or an *inline box*.

* A *block-level box* element fills up the entire width of the screen by default and forces starting on a new line. Examples are: headers `<h1> - <h6>`, paragraphs `<p>`, lists `<ul>, <li>`, and divisions `<div>`.

* An *inline boxe* element is displayed in a line, flowing between surrounding text. Examples: images `<img>`,  `<span>`,  and `<label>`.

* The space each element takes can be controlled by setting the width and height of its box. Different boxes can be separated by changing the value of borders, margins, padding, and background colors.

### Controlling the position of elements

CSS allows controlling the layout of a page by positioning elements in various ways. Those ways are known as the **positioning schemes**; i.e.

* Normal flow `position: static;` - it is the default behaviour; in which elements are always positioned according to the normal flow of the page.

* Relative positioning `position: relative;` - it changes the position of one element from its default (normal) position, without affecting its surrounding elements.

* Absolute positioning `position: absolute;` - it positions the element relative to its nearest containing element, unlike fixed positioning where the positioning is relative to the browser window. This doesn't affect the position of the surrounding elements.

The **box offset properties** are used to indicate where a box should be positioned; how far it should be positioned from the top, bottom, left, or right.

* Fixed Positioning `position: fixed;` - it is positioned relative to the browser window, which means it always stays in the same place even if the page is scrolled. This does not affect the position of the surrounding elements.

* Floating elements - The `float` property is used for taking an element out of normal flow and positioning it to the far left or right of its containing box. This property can be used to place elements side-by-side by changing the width and height of them.

### Designing for different sized screens

* **Screen size** - different devices have different sized screens, therefore, different amounts of information may appear on each screen.

* **Screen resolution** - it refers to the number of pixels (dots) a screen shows per inch.

* Because screen sizes and display resolutions vary so much; designers tend keep pages within 960-1000 pixels wide, and they try to describe the main purpose of the site within the top 600 pixels.

### Screen layouts

* **Fixed width layouts** - they don't change the size as the user increases or decreases the size of the browser window. To do so, use pixels to specify the width of each box while styling the page.

* **Liquid (stretchy) layouts** - they stretch and contract the size as the user increases or decreases the size of the browser window. To do so, use percentages to specify the width of each box while styling the page.



## Chapter 3: Functions, Methods, and Objects [JS]

Functions, methods, and objects are used to organize complicated code.

### Functions and methods

**Functions** allow grouping a set of statements together to perform a specific task. They can be reused each time the task needs to be repeated, rather than repeating the same set of statements again and again. So, functions can be seen as a way for storing the steps of performing a task. 

#### Declaring functions

The process of creating a function is known as *function declaration*. To do so, use the following syntax:

```
function functionName(parameters) {
  statements;
}
```

* The `function` keyword is used to declare the function.
* Each function should be given a meaningful name, aka identifier.
* parentheses ().
* The **parameters** are used when information is needed to be passed to the function's statements.
* use `return value` if the function was supposed to return anything.

Example of a simple function:

```
function logNumbers () {
    for (let i=0; i<5; i++) {
    console.log(i);
    }
}
```


## Article: [*6 Reasons for Pair Programming*](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

### What is pair programming, how it works?

Pair programming is when two developers sharing a single workstation interactively work on a code together. There are different styles for pair programming, commonly they involve two roles: the *Driver* and the *Navigator*.

* The Driver is the one handling the mechanics/physical side of the work, i.e; typing the code, managing the text editor, switching files, etc.

* The Navigator is the one responsible for guiding the Driver, i.e; thinking about the big picture, controlling the flow of the work, how an algorithm might be converted into code, while scanning for typos or bugs, etc. They are not supposed to write any code.

### Why pair programming?

learning coding is like learning a new language; it aquires the following skills:

* Listening - students listen to others guidance.
* Speaking - students explain out loud what the code should do.
* Reading - students write code themselves.
* Writing - students read code that others have written.

Pair programming touches on all four skills.

### Pair programming advantages

1. *Greater efficiency* - it might take a bit longer when two people focus on the same code block, however, studies show that it produces higher-quality code that doesn’t require later effort in troubleshooting and debugging. So, in the long-run, it would be more efficient than two people working on separate features.

2. Engaged collaboration* - When two programmers focus on the same code, it  becomes harder to procrastinate or get off track. Also, When two programmers work together, they can often find a solution together without the need to ask for additional help.

3. *Learning from fellow students* - each person has their unique approach to a specific problem. Pair programming exposes the different students to new approaches and maybe different experience levels.
 
4. Helps improving *social, and communication skills*. It also helps programmers in strengthening their ability to work with and learn from others. It also helps them to get familiar with how pairing works. Those skills help programmers to attract *job opportunities*.