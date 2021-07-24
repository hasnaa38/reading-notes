# Code 201 - Read 01
In this file, a summary of **Read: 01 - Introductory HTML and JavaScript ** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett. 

## HTML 

### Introduction 
#### Terminology
* Browser - software used to access the different websites.  
* Domain Name - a unique, human-readable internet 
addresses of a website. 
* ISP - a company that provides access to the internet. 
* IP (Internet Protocol) Address - a unique numerical identifier that is assigned to a device 
to allow communication over the internet.
* Web Server - a special computer that hosts a website. 


#### How the web works 
1. People are connected to the internet via an **ISP** (Internet Service Provider). 
2. When a person wants to visit a website, they type the **domain name** (web address) of that website to their **browser**. 
3. The computer contacts a **domain name system** (DNS) 
server; which returns the **IP address** of the **web server** that hosts the website.
4. Your **browser** contacts the **web server**. 
4. The **web server** sends the page you requested back to your **web browser**.

The **web browser** actually receives HTML, CSS, JS, and other types of files from the **web server** that hosts the site. The **web browser** interprets the received code to create the page that you see.

### Chapter 1: Structure
In all kinds of documents, structure is very important in helping readers to understand the aimed messages and to navigate around the document. Web pages are documents. **HTML** describes the structure of a web page. 

* The HTML code is made up of characters that live inside angled brackets `<>`, these are called **HTML elements**. 
* HTML elements are usually made up of two **tags**: an *opening tag* and a *closing tag*. Tags act like containers. They tell you something about the information that lies between them. 

So far, thing will look like the following:  
`<opening tag>Content</closing tag>`

An example would be: 
```
<h1>This is the Main Heading</h1>
```

* **Attributes** provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a *name* and a *value*, separated by an equals sign. 
An example would be: 
```
<p lang="en-us">Paragraph in English</p>
```
Here an attribute called `lang` is 
used to indicate the language used in this element. The value of this attribute on this page specifies it is in US English.


HTML pages are usually divided into two main elements:

1. The head element `<head> ... </head>` - which contains information about the page. 

2. The body element `<body> ... </body>` - everything inside this element is shown inside the main browser window. 



### Chapter 8: Extra Markup
DOCTYPES tell browsers which version of HTML you 
are using. During this course, **HTML5** is to be used.

#### HTML comments 
Comments are used to add information about the code and they will not be visible in the user's browser.
To add comments to the code: `<!-- Add The Comment Here -->`. 

#### id attributes 
They are used to uniquely identify that element 
from other elements on the page. Every HTML element can carry an id attribute. 
To add it to an element: 
```
<h1 id="mainHeadingID">This is the Main Heading</h1>
``` 
The id attribute is known as a **global attribute** because it can be used on any element. 

#### Class attributes 
They are used to identify several elements as being different from the other elements on the page. 
Every HTML element can also carry a class attribute. 
To add it to an element: 
```
<h1 class="mainHeadingClass">This is the Main Heading</h1>
``` 

#### The div and span elements
The `<div>` and `<span>` elements allow you to group 
block-level and inline elements together. 

#### The meta tag
The `<meta>` element lives inside the `<head>` element, it is not visible to users and contains information about that web page. 

### Chapter 17: HTML5 Layout
HTML5 is introducing a new set of elements that help define the structure of a web page. 

The `<header>`, `<main>`, and `<footer>` elements can be added to the `<body>` of the page to indicate the purpose of 
each part of the code and help to describe the structure. An example of a code would be: 
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Example</title>
</head>

<body>
  <header> ... </header>
  <main> ... </main>
  <footer> ... </footer>
</body>
</html>
```

Older browsers that do not understand the new HTML5 elements and will automatically treat them as 
inline elements. Therefore, to help older browsers, the following CSS line should be included to state the new elements that should be rendered as block-level elements.
```
header, section, footer, aside, nav, article, figure 
{
display: block;}
```

### Chapter 18: Process & Design

#### Before designing, ask yourself the following questions: 

1. Who is the website targeting?
2. Why are people visiting the website and what are they trying to achieve?
3. What information do your visitors need/give? 
4. How often will people visit the website? 


#### Site maps
allow the designer  to plan the structure of a site.
![Site Map Example](https://www.everyinteraction.com/wp-content/uploads/2017/05/sitemap-definition-example.gif)

#### Wireframes
allow the designer to organize the information that will need to go on each page.
![Wireframe Example](https://d1dlalugb0z2hd.cloudfront.net/handbooks/agile-handbook/wireframe/02-newspaper-site-wireframe-example.png)

## JavaScript

### Introduction
JavaScript is used in browsers to make websites more interactive, interesting, and user-friendly. It allows the following: 

1. Accessing the content of any element, attribute, or text from an HTML page. For example: selecting the text inside all of the `<hl>` elements on a page or finding out what was entered into a text input using its id.

2. Modifying the content by adding/removing 
elements, attributes, and text to/from the page.

3. Program rules - JS allows for specifying a set of steps for the browser to follow, in which they allow it to access or change the content of a page. 

4. React to events - JS allows for specifying that a script should run when a specific event has occurred. For example, it could be run when a button is pressed or a link is clicked.

### Chapter 1: The ABC of Programming
JavaScript is a programming language, unlinke HTML which is a markup language. Therefore, JS uses the concepts of computer programming, which will be covered in the following three sections: 

#### Section A - What is a script and how do I create one?  
* A script is a series of instructions that the computer
can follow in order to achieve a goal. 
* Each time the script runs, it might only use a subset of all the instructions. 

To approach writing a script, break down your goal into 
a series of tasks and then work out each step needed 
to complete that task (a flowchart can help).

#### Section B - How do computers fit in with the world around them? 
Computers use data to create models of things in the real world. Web browsers create models of the web page they are showing. The current web page loaded into each browser window is modelled using a document object. The document object represents an HTML page. 

##### How do browsers interpret the HTML code and apply styling to it? 

1. The browser receives the web page from the web server as a document that contains an HTML code. Each website consists of one or more documents. 

2. The browser creates a model of the page and stores it in the memory. 

3. The broswer uses a rendering engine to show the page on the screen. If there is no CSS styling sheet linked in the code, the rendering engine will apply default styles to HTML elements. However, when the browser receives CSS rules, the rendering engine processes them and applies each rule to its corresponding elements.

4. The browser uses a JavaScript interpreter to translate the JS instructions line-by-line into instructions the computer can follow.

#### Section C - How do I write a script for a web page?
Web developers mainly use about three languages to create web pages: HTML, CSS, and JavaScript. Each language forms a separate layer with a different purpose. Each layer, from left to right, builds on the previous one. 
* HTML is the content layer and it has `.html` extension. 
* CSS is the presentation layer and it has `.css` extension.
* JavaScript is the behaviour layer and it has `.js` extension.


The best practice is to keep JavaScript code in its own JavaScript file, then link it to the web page using the HTML `<script>` element and the `src` attribute -to identify where it is stored-. For example:
 ```
<script src="main.script.js"></ script>
```

