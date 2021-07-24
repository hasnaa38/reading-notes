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

An example would be: `<h1>This is the Main Heading</h1>`

* **Attributes** provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a *name* and a *value*, separated by an equals sign. 
An example would be: `<p lang="en-us">Paragraph in English</p>`. Here an attribute called `lang` is 
used to indicate the language used in this element. The value of this attribute on this page specifies it is in US English.


HTML pages are usually devided into two main elements:

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
To add it to an element: `<h1 id="mainHeadingID">This is the Main Heading</h1>`. 
The id attribute is known as a **global attribute** because it can be used on any element. 

#### Class attributes 
They are used to identify several elements as being different from the other elements on the page. 
Every HTML element can also carry a class attribute. 
To add it to an element: `<h1 class="mainHeadingClass">This is the Main Heading</h1>`. 

#### The div and span elements
The `<div>` and `<span>` elements allow you to group 
block-level and inline elements together. 

#### The meta tag
The `<meta>` element live inside the `<head>` element, it is not visible to users and contains information about that web page. 

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
inline elements. Therefore, to 
help older browsers, the follwing CSS line should be included to state the new elements that should be rendered as block-level elements.
```
header, section, footer, aside, nav, article, figure 
{
display: block;}
```

### Chapter 18: Process & Design

#### Before designing, ask yourself the following questions: 

1. Who is the website targeting?
2. Why are people visiting the website and what are they trying to achieve?
3. What information your visitors need/give? 
4. How often people will visit the website? 


#### Site maps
allow the designer  to plan the structure of a site.
![Site Map Example](https://www.everyinteraction.com/wp-content/uploads/2017/05/sitemap-definition-example.gif)

#### Wireframes
allow the designer to organize the information that will need to go on each page.
![Wireframe Example](https://d1dlalugb0z2hd.cloudfront.net/handbooks/agile-handbook/wireframe/02-newspaper-site-wireframe-example.png)

## JavaScript

### Introduction

### Chapter 1: The ABC of Programming