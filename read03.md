# read 03 
In this file a summary of *Read 03 - Structure web pages with HTML* will be provided. The file includes a summary of multiple articles, each topic/article will have its own section and will be provided its link. 

## Topic 1 - Wireframe and Design 

### What is a wireframe
A wireframe is a diagram that outlines the features and formats of a web page. Designers use wireframes before they get to actually building the web page to define and plan the page's information hierarchy. Wireframes can be sketched by hand or using software. 

### Procedure of creating a wireframe
1. **Research and collect data** - Define what you need and research your audience; define who they are and what they want, and complement you research by doing further competitor and industry research. 
2. **Map out the user flow** - Organize the flow you expect users to follow; i.e. where they will be coming from and where you need them to end up.
3. **Start sketching** - Make sure its simple yet efficient. Asking the following questions -quoted from the article- for yourself might be helpful: 
> How can you organise the content to support your users’ goals?
Which information should be most prominent? Where should your main message go? What should the user see first when arriving at the page?
What will the user expect to see on certain areas of the page?
Which buttons or touch points does the user need to complete the desired actions?
4. **Add some details and start testing**. 
5. **Start turning it into prototypes**.  

The original article - [The Definitive Guide: How To Create Your First Wireframe](https://careerfoundry.com/en/blog/ux-design/how-to-create-your-first-wireframe/)

## Topic 2 - HTML basics
### What is HTML
**H**yper**T**ext **M**arkup **L**anguage is a markup language used to structure and add content to web pages. 

### HTML elements 
An HTML code consists of a series of elements, each element contains of the following:

1. The opening tag - it states where the element begins or starts to take effect.
2. The content of the element. 
3. The closing tag - the same as the opening tag but states where the element ends. Some elements have no closing tag. 
4. Attribute - some elements have attributes, for example to add an image you will use the `<img>` element which uses the source `src` attribute to specify the URL of the image. 

Figure .1 illustrates an example of a paragraph element.
![Figure.1](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

_**Note**_ Elements can be nested. 

### Anatomy of an HTML document
Each HTML document should has .html extension and should contain this code: 
```
<!DOCTYPE html>
<html>

  <head>
    <meta charset="utf-8">
    <title> The title of the page/ the tab name </title>
  </head>

  <body>
    The body of the page 
  </body>

</html>
```

_**Note**_ To autogenerate this code in Replit, type `!`. 

### Basic HTML elements 
- **Headings** - thet are used to specify certain parts of the content. HTML contains 6 heading levels; from `<h1>` to `<h6>`, an example: 
```
<h1>The main heading</h1>
<h2>The second heading</h2>
```

- **Paragraphs** - the `<p>` element contain paragraphs of text, an example: 
```
<p>This is a single paragraph</p>

```


- **Images** - the `<img>` element  embeds an image into the page using the help of the `src` attribute; which contains the path to our image file. For example, to add an image of a cat to your page, use the following code: 
```
<img src="https://cdn.mos.cms.futurecdn.net/VSy6kJDNq2pSXsCzb6cvYF.jpg" alt="Image of a cat <3">

```

- **Hyperlinks** - the *anchor* `<a>` element is used to link some text to a URL. This element also uses an attribute; which is the `href` attribute that contains the web address we aim to head the user to. An example: 
```
<a href="https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics">Article</a>
```

- **Lists** - There are 2 list elements in HTML: 
1. Unordered list - wrapped with the `<ul>` element.
2. Ordered listwrapped with the `<ol>` element.
Each list item is wrapped with the `<li>` element. 
Example of an unordered list: 
```
<ul>
  <li>Potato</li>
  <li>Tomato</li>
  <li>Cheese</li>
</ul>
```

The original article - [HTML basics
e](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)

## Topic 3 - Semantics 
Semantic elements refere to the meaning/effect/purpose/role of a piece of code. For example, the `<h1>` element is a semantic element that gives the content it wraps the meaning of top level heading on a web page, as a result, the browser will render this text in a large font size. 

The original article - [Semantics
](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)