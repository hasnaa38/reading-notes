# Code 201 - Read 02

In this file, a summary of **Read: 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett.

## From the Duckett HTML book

### Chapter 2: Text

HTML elements are used to describe the structure of the page. Therefor, a discussion on the the elements used for adding markup to the text that appears on a web page is provided in this chapter.

#### Headings

There are 6 heading levels in HTML represented by the tags `<h1> ... </h1>` to `<h6 ... </h6>`; where `<h1>` is used as the main heading, `<h2>` is used for subheadings.
Browsers display the contents of headings at different sizes, where `<h1>` is the largest and `<h6>` is the smallest.
An example would be:

```
<h1>This is the main heading</h1>
<h2>This is the subheading</h2>
```

#### Paragraphs

The `<p> ... </p>` tags are used create a paragraph, an example would be:

```
<p>Enter the paragraph here</p>
```

Paragraphs are block elements, which means that each paragraph starts at a new line and uses the full width of the page.

#### Special elements

* The `<b> ... </b>` tags are used to make the text in between them bold, unlike the text around it.

* The `<i> ... </i>` tags are used to make the text in between them italic, unlike the text around it.

* The `<sup> ... </sup>` tags are used to make superscript characters.

* The `<sub> ... </sub>` tags are used to make subscript characters.

#### White space

* Browsers only display one space if two or more spaces were written next to each other in the code. Also, it displays line breaks as a single space too. This is known as *white space collapsing*.

* The `<br />` tag is useed to jump to a new line within the same paragraph. An example would be:

```
<p>This is one paragraph<br />but this text will be added on another line</p>
```

* The `<hr />` tag is useed to create a line break between elements.

#### Other elements

* The `<strong> ... </strong>` element is used to indicate that the content is strongly important and the browser will display it as a bold text.

* The `<blockquote>` element is used for quoting long paragraphs. The `<p>` element is still used inside the `<blockquote>`
element.

* The `<q>` element is used for shorter quotes.

### Chapter 10: Introducing CSS

## From the Duckett JavaScript book

### Chapter 2: Basic JavaScript Instructions

### Chapter 4: Decisions and Loops
