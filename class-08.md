# Code 201 - Read 08

In this file, a summary of **Read: 08 - More CSS Layout** will be provided. The read covers **chapter 15 - Layout** from *HTML & CSS: Design and Build Websites* book, written by Jon Duckett.

## Controlling the position of elements

CSS treats each HTML element as if it is in its own box. This box will either be:

* A *block-level* box: starts on a new line and uses the full width of the page or container. Examples: `<p>`, `<div>`, `<nav>`, `<ol>` and `<ul>`, `<table>` and `<section>`.

* An *inline* box: flows between surrounding text. Examples: `<span>` and `<a>`.

The space that each box takes can be controlled by setting a width and height for the box.

Boxes can be separated using borders, margins, padding, and background colors.

### Grouping multiple elements

If one block-level element sits inside another block-level element, then the outer box is known as the *containing* or *parent element*. For example, `<div>` is often used as containing element to group together sections of a page.

### CSS positioning schemes

CSS offers positioning schemes to control the layout of a page, them being: normal flow, relative, absolute, fixed, sticky, and float. This can be done using the `position` property and one of the values:

* Normal flow `position: static;` - all elements are in order as they appear in the document. It the default way for browsers to display pages.

* Relative positioning `position: relative;` - the element is positioned relative to its normal position. This means when adding other styles, the element will adjust its positioned from where it would have been in normal flow.

* Absolute positioning `position: absolute;` - the element is positioned absolutely to its first positioned parent.

* Fixed positioning `position:fixed` - the element is positioned related to the browser window. Therefore, when a user scrolls through the page, it stays in the exact same place.

* Sticky positioning `position:sticky` -  the element is positioned based on the user's scroll position.

### Floating elements

The `float` property places elements as far from left `float: left;` or right `float: right;` of the page as defined. It is also used to create multi-column layouts.

When using the float property, the width property should be also used to to indicate how wide the floated element should be.

### Multi-column layouts

To achieve multi-column layouts, use the following:

1. The `<div>` element to represent each column.

2. The `width` property to set the width of the columns.

3. The `float` property to positions the columns next to each other.

4. The `margin` property to create a gap between the columns.

Example:

**The HTML code**

```
<div class="column1of3">
    <h1>Left column</h1>
    <p>...</p>
</div>
<div class="column2of3">
    <h1>Center column</h1>
    <p>...</p>
</div>
<div class="column3of3">
    <h1>Right column</h1>
    <p>...</p>
</div>
```

**The CSS code**

```
.column1of3, .column2of3, .column3of3 {
width: 300px;
float: left;
margin: 10px;}
```

**Results**

![3-column layout](https://miro.medium.com/max/1400/1*vI1swETTM0HNBuoPfm0hmw.png)

## Screens

> Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).

### Designing for different sized screens

* **Screen size** - different devices have different sized screens, therefore, different amounts of information may appear on each screen.

* **Screen resolution** - it refers to the number of pixels (dots) a screen shows per inch.

* Because screen sizes and display resolutions vary so much; designers tend keep pages within 960-1000 pixels wide, and they try to describe the main purpose of the site within the top 600 pixels.

### Screen layouts

* **Fixed width layouts** - they don't change the size as the user increases or decreases the size of the browser window. To do so, use pixels to specify the width of each box while styling the page.

* **Liquid (stretchy) layouts** - they stretch and contract the size as the user increases or decreases the size of the browser window. To do so, use percentages to specify the width of each box while styling the page.
