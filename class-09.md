# Code 201 - Read 09

In this file, a summary of **Read: 09 - Forms and Events** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett and an online article.

## Table of contents

* From the Duckett HTML and CSS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 7    | Forms       |
| Chapter 14   | Lists, Tables & Forms | 

* From the Duckett JS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 6    | Events |

## Chapter 7: Forms [html]

Forms allow collecting information from website users. We see forms when signing up for a website, when signing up for 
newsletters or mailing lists and when searching using Google or other search engines.

Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server. A form may have several form controls to gather information. The server needs to know which piece of inputted data corresponds with which form element. Therefore, information is sent in name/value pairs.

### How forms work?

1. A user fills in the form and presses the submit button to submit the information to the server.
2. Information from the form are sent to the server in name/value pairs.
3. The server processes the information using any programming language and may store it in a database.
4. The server creates a new page to send back to the browser based on the received information.

### Form structure

Form controls live inside a `<form>` element. This element is a container for different types of input elements.

It uses the `action` attribute, the value is the URL for the page on the server that will process the form when its submitted.

It uses the `method` attribute. Forms can be sent using one of two methods: 

* *get* - the form values are added to the end of the URL.
* *post* - the form values are sent in HTTP headers. This method is used when the form:

1. allows users to upload a file
2. is very long
3. contains sensitive data (e.g. passwords)
4. adds information to, or deletes information from, a database

Example:

```
<form action="http://www.example.com/subscribe.php" method="get">
<p>This is where the form controls will appear.</p>
</form>
```

Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

#### The input element

The `<input>` element is used to create various form controls. The value of the `type` attribute determines what kind of input they will be creating.

* `type="text"` - creates a single-line text input field.
* `type="password"` - creates a single-line text input field but the characters are blocked out.
* `type="radio"` - allows users can pick one of the option buttons.
* `type="checkbox"` - allows users to select and unselect one or more options boxes.
* `type="file"` - creates a box and a browse button. When the user clicks on the browse button, a window opens and they select a file from their computer to be uploaded to the website.
* `type="submit"` - used to send a form to the server.

#### Other elements

* The `<textarea>` element is used to create a mutli-line text input.
* The `<select>` element is used to create a drop down list box. It contains two or more `<option>` elements.

## Chapter 14: Lists, Tables & Forms [css]

### Styling lists

Here, we are styling the `<ol>`, `<ul>`, and `<li>` elements.

* The `list-style-type` property is used to control the shape or style of bullet points (aka: markers).

* The `list-style-image` property is used to specify an image to act as a marker. The value is the word url followed by the path to the image inside (""). Example:

```
ul {
list-style-image: url("images/star.png");
}
```

* The `list-style-position` property is used to specify the position of the list-item markers.

* The `list-style` property is used as a shorthand for list styles (does all the previous).

### Styling tables

* The `empty-cells` property is used to specify whether empty cell borders should be shown or not.

* The `border-spacing` property is used to control the distance between adjacent cells.

* The `border-collapse` property is used to collapse borders ar into a single border where possible.

### Styling forms

* To style *text inputs*: font-size, color, background-color, background-image, border, border-radius, :hover and :focus pseudo-classes.

* To style *submit buttons*: color, text-shadow, border-bottom, background-color, :hover pseudo-class.

* To style *fieldsets and legends*: width, color, background-color, border, border-radius, padding.

* The `:focus` pseudo-class is used to change the background color of the text input when it is being used.

* The `cursor` property is used to control the type of mouse cursor that should be displayed to users.


