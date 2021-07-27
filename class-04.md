# Code 201 - Read 04

In this file, a summary of **Read: 04 - HTML Links, CSS Layout, JS Functions** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett and an online article.

## From the Duckett HTML and CSS book

* Chapter 4: Links
* Chapter 15: Layout

## From the Duckett JS book

* Chapter 3: Functions, Methods, and Objects, pages 86-99 ONLY
* Article: *6 Reasons for Pair Programming*

### Chapter 4: Links

* Links  are HTML objects that enabling the idea of web browsin\surfingusers by allowing users to move from one web page to another when clicking them.

* Links are created using the anchor element `<a>`. Syntax:

```
<a href="URL">Link Text</a>
```

* The **href** attribute is used to add the link's destination.
* The **link text** is the clickable text that moves the user.

#### Destination options

1. Another page from another website- the value of the `href` attribute will be the full web address for that page; aka *the absolute URL*.

2. Another page within the same website (repository) - the value of the `href` attribute is the path of the intended file (with the extention); aka *the relative URL*. The relative URL specifies the destination according to the page's relation to the current page.

3. An email - add `mailto:` followed by the email address. When a user clickes this link, their email will compose a new email message addressed with the specified mailto address. Example:

```
<a href="mailto:email address">Email Us</a>
```

4. Specific part on the same page - before doing so, you should add an **id** to the aimed element. The value of the `href` attribute will be `#id` of that part. Example:

```
<a href="#aimedPara">Go to paragraph</a>
<p id="aimedPara">This is the paragraph we aim to jump to by clicking on the link</p>
```

5. Specific part on another page (whether on the same site or a different one) - beofore doing so, you should be able to have the **id** of the intended element. The value of the `href` attribute would contain the address of the page (either the absolute URL or the relative URL), followed by `#id` of the element. Example: 

```
<a href="URL/#bottom">
```

#### Opening the link in a new window

Links can be opened in a new window using the `target` attribute. The value of this attribute should be `_blank`. Example:

```
<a href="URL" target="_blank">Link Text</a> 
```

