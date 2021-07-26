# Code 201 - Read 03

In this file, a summary of **Read: 03 - HTML Lists, CSS Boxes, JS Control Flow** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett.

## From the Duckett HTML book

### Chapter 3: Lists

There are three types of HTML lists:

1. Ordered lists - each list item begins with a number, this list of types of lists is an ordered list! This type of lists is created using the `<ol>` element.
2. Unordered lists - each list item begins with a bullet point (*). This type of lists is created using the `<ul>` element.

The `<li>` element is used to add list items. An example of an ordered list with 3 list items is:

```
<p>There are three types of HTML lists:</p>
<ol>
    <li>Ordered lists</li>
    <li>Unordered lists</li>
    <li>Definition lists</li>
</ol>
```

3. Definition lists - a set of terms along with their definitions. This type of lists is created using the `<dl>` element. The term is contained in the `<dt>` element and the deintion in the `<dd>` element. Example: 

```
<dl>
    <dt>Happiness</dt>
    <dd>it is a positive emotional state characterized by feelings such as contentment, joy, and life satisfaction.</dd>
    <dt>Sadness</dt>
    <dd>it is an emotional pain associated with, or characterized by, feelings of disadvantage, loss, despair, grief, helplessness, disappointment and sorrow. </dd>
</dl>
```

***Note*** Lists can be nested (we can create a sub-list inside a list item).


### Chapter 13: Boxes

#### Controlling boxes dimensions

CSS treats each HTML element as if it lives in its own box. This chapter discusses the following concepts:

* The `height` and `width` properties: to control the box dimensions. There are three ways to specify the size of a box: *pixels*, *percentages* (based on the size of the browser window), or *ems* (based on the size of text within it).

* The `min-height` and `max-height` properties: to limit the height of the box.

* The `min-width` and `max-width` properties: to limit the width of the box.

* The `overflow` property: to control what happens if the content within a box is larger than the box itself.

#### Border, margin and padding

* *Padding* The space between the border of a box and its contents.

* *Border* it separates the edge of one box from another.

* *margin* it is outside the edge of the border.

![Border, margin and padding](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKgpOQdy1FFpF8YxlYwzJCEbiBERdsFg3gUg&usqp=CAU)

* Padding and margin are used to add space between various boxes on a page.

#### Centering boxes and content

* The `left-margin` and `right-margin` properties can be used to center boxes on a page.

* The `text-align` property can be used to center the text inside a bax.

#### Hiding boxes

The `visibility` property allows hiding boxes from users. However, it hides the box but leaves a space where the element would have been.

#### Switch between in-line and block elements

* Inline elements display in a line. They do not force the text after them to start on a new line.

* Block elements take up all the width by default. They force the text after them to start on a new line.

* The `display` property is used to turn *inline* elements to *block-level* elements or vice versa, and can also be used for elements from the page.

## From the Duckett JS book

### Chapter 2: Basic JavaScript Instructions - Arrays

Arrays are special variables that store a list of values. Example: 

```
var names; 
names= ['Sarah','Samar', 'Aseel']; 
```

*Sarah* has the **index** 0, so executing `console.log(names[0])` results with *Sarah*.

### Chapter 4: Decisions and Loops - Loops

Loops offer a quick and easy way to repeat an action multiple times.

#### How do they work -in general-:

1. The control checks a condition. If it returns true; the code block will be executed.
2. It keeps rechecking -repeating step 1- until the condition returns false. When this happens, the loop terminates.

Therefore, a poorly written loop code will result in something called **infinite loop**.

#### For loop

Syntax: 

```
for ([initial expression]; [condition]; [increment expression]) {
  statements; 
}
```

**Execution**:

1. The initializing expression initializes one or more loop counters. An example of an initialization expression would be `let i = 0`.
2. The condition expression is evaluated. If the value of condition is true, the loop statements execute. If the value of condition is false, the for loop terminates.
3. The statement executes.
4. The update expression (increment expression) is executed.
5. The control returns to Step 2.

#### While loop

A while loop executes its statements as long as a condition evaluates to true. If the condition becomes false, the statements within the loop will stop executing and the control passes to the statement following the loop. Syntax:

```
while (condition) {
  statements;
}
```

#### Do While loop

The difference between this loop and the **while** loop is that this loop allows executing the statements once before checking the condition. Syntax:

```
do {
   statement;
}
while (condition);
```