# Code 201 - Read 07

In this file, a summary of **Read: 07 - HTML Tables; JS Constructor Functions** will be provided. The read covers multiple chapters from two books; *HTML & CSS: Design and Build Websites* and *JavaScript & jQuery: Interactive Front-End Web Development*, both written by Jon Duckett. Along with a GitHub document by CodeFellows.

## Table of contents

* GitHub - [Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

* From the Duckett HTML book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 6    | Tables      |

* From the Duckett JS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 3    | Functions, Methods, and Objects|

## Domain Modeling

### Definition

> *Domain modeling* is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An *object-oriented* model is an entity that stores data in properties and encapsulates behaviors in methods. 

*Note* Create instances using the `new` keyword followed by a call to a function.
*Note* The `this.` is used within methods to access the object's properties and methods from inside.

A well articulated domain model can verify and validate the understanding of a specific problem  among various stakeholders. To do so, follow the following tips:

1. When modeling a single entity that will have many instances, build an object with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Store the newly created object in a variable so you can access its properties and methods from outside.

## Chapter 6: Tables [html]

Tables are used to display information in a grid format; i.e. *rows* and *columns*. Each block in the grid is referred to as a *table cell*.

In HTML, tables are written out row by row.

### How to create tables

1. The `<table>...</table>` element is used to create a table.

2. The contents of the table are written out row by row. The `<tr>` tag is used to indicate the start of each row. And the closing `</tr>` tag is used to indicate the end of the row. Note: **tr** stands for table row.

3. The `<td>...</td>` element is used to add the contents of each cell in the row. Note: **td** stands for table data.

Example:

```
<table>
    <tr>
        <td>15</td>
        <td>15</td>
        <td>30</td>
    </tr>
    <tr>
        <td>45</td>
        <td>60</td>
        <td>45</td>
    </tr>
    <tr>
        <td>60</td>
        <td>90</td>
        <td>90</td>
    </tr>
</table>
```

Results should be as the following:

|     |     |     |
| --- | --- | --- |
| 15  | 15  | 30  |
| 45  | 60  | 45  |
| 60  | 90  | 90  |


* The `<th>` element is used to represent the **heading** for either a column or a row. Note: `th` stands for table heading. The `scope` attribute can be used to indicate whether it is a heading for a column: `col` or a row: `row`. Example:

```
<th scope="row">Tickets sold:</th>
<th scope="row">Total sales:</th>
```

* Even if a cell has no content, either `<td>` or `<th>` elements should be used to represent the presence of an empty cell, otherwise the table will not render correctly.

### Spanning cells

Table cells can be spanned on more than one row or column using the `rowspan` and `colspan` attributes. The attributes can be added to the `<th>` or `<td>` elements and indicates how many rows/columns that cell should run across. Example:

### Long tables

For long tables, the table content can be split into the following elements:

* The `<thead>` element is used to add the headings of the table.
* The `<tbody>` element is used to add the body of the table.
* The `<tfoot>` is used to add the footer of the table.

## Chapter 3: Functions, Methods, and Objects

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