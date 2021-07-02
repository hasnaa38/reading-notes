# read 06 
In this file a summary of *Read: 06 - Design web pages with CSS* will be provided. The file includes a summary for multiple articles, them being: 
[What is CSS?](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS) // [How To Add CSS](https://www.w3schools.com/css/css_howto.asp) // [CSS color Property](https://www.w3schools.com/cssref/pr_text_color.asp). 

## what is CSS? 
CSS (Cascading Style Sheets) is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

CSS is a rule-based language; rules are defined to specify groups of styles that should be applied to particular elements/groups of elements on a web page.

#### There are 3 ways to insert CSS: 

1. **Inline CSS** -  used to apply a unique style for a single element. To do so, add the style attribute to the relevant element. The style attribute can contain any CSS property. Example: 
```
<p style="color:red;">This is a paragraph.</p>
```


2. **Internal CSS** - used if one single HTML page has a unique style. To do so, defined a `<style>` element inside the head section and add your rules there. Example: 
```

<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

3. **External CSS** - can be used to style multiple web pages! Basically its a `.css` file that contains styling rules that can be applied to any document that linkes it. To do so, define a `<link>` element inside the head section and link it. Example: 
```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```


#### Cascading Order
If there is more than one style specified for an HTML element, the value from the highest priority style will override the others. 
priority list -from the highest to the lowest-: 

1. Inline style (inside an HTML element)

2. Internal and External style sheets (in the head section)

3. Browser default
