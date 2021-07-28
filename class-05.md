# Code 201 - Read 05

In this file, a summary of **Read: 05 - HTML Images; CSS Color & Text** will be provided. The read covers multiple chapters from the book *HTML & CSS: Design and Build Websites* and a blog post.

## Table of contents

* From the Duckett HTML and CSS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 5    | Images      |
| Chapter 11   | Color       |
| Chapter 12   | Text        | 

* Blog post - [JPEG vs PNG vs GIF — which image format to use and when?](https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d)

## Chapter 5: Images [html]

### Adding images to web pages

Images are added to the HTML page using the `<img>` element. This element has no closing tag, elements with no closing tags are known as an **empty elements**.
The element mainly carries the following attributes:

#### The source attribute `src`

It is used to specify the directory of the image, which can be:

* The absolute URL of the image - if the image was taken from an online website

* The Relative URL - if the image was uploaded from the device. The relative URL should be pointing to the directory of the image in the site's files.

#### The alternative text attribute `alt`

To provide a text description of the image. This will be helpful if the image was down or for people who can't see and use screen readers.

#### The `title` attribute

Too provide additional information about the image. This title will be displayed when the user hovers over the image.

Final Example:
```
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/368px-Google_2015_logo.svg.png" alt="Google.com logo" title="Google.com logo">
```

### Height and width for images

There are two more attributes for specifying the height and width for the images: the `height` attribute and the `width` attribute. Both accepts pixel values. CSS also has image size properties that can be used.

### Figures and captions

HTML5 allows you to associate figures with their captions.

![Figure and figcaption in html5](https://i.stack.imgur.com/kiKn4.png)

* The `<figure>` element is used to add the images associated with captions. Multiple images can be added here as long as they share the same caption. 

* The `<figcaption>` element is used to add the caption to images.

Example:

```
<figure>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/368px-Google_2015_logo.svg.png" alt="Google.com logo">
<br />
 <figcaption>Fig .1: Google.com logo</figcaption>
</figure>
```

### Image formats

There are many image formats that developers can use. Websites mainly use *jpeg*, *png*, and *gif* images. Using the wrong format might result in the image looking not as sharp as it should be and can make the web page load slower.

* **JPEG** - best used for images with where variation in colour and intensity is smooth, for example: natural scenes.

* **PNG** -  best used for the images with few colors or large areas of the same color. It is also used for images that need transparency or for images with text & objects with sharp contrast edges like logos.

* **Animated GIFs** - they show several frames of an image in sequence (they are moving).

* Scalable Vector Graph **SVG** - it is a new format used to display *vector images*.

> Vector images are created by placing points on a grid, and drawing lines between those points. A color can then be added to "fill in" the lines that have been created.

> The advantage of creating line drawings in vector format is that you can increase the dimensions of the image without affecting the quality of it.

## Chapter 11: Color [css]

The `color` property is used for specifying the color of text inside an element. The most used ways to assign color values in CSS are:

1. **Color names** - There are 147 predefined color names.

2. **RGB values** - to express colors in terms of how much red, green and blue are used to make the color up. Formula: `rgb(red, green, blue)`. Each one of these parameters will have a numeric value between 0 and 255. Example: red is rgb(255, 0, 0).

***Note*** RGBA (in CSS3) has an extra value that indicates opacity. This value can be a number between 0.0 (means 0% opacity) and 1.0 (means 100% opacity).

3. **HEX codes** - six-digit codes that express the amount of red, green and blue in a color, preceded has `#` sign. Formula: `#RRGGBB`. Each color is represented with a hexadecimal value between 00 and ff. Example: red is #ff0000.

### Background color

Since HTML elements are treated as if they are in boxes, the `background-color` property is used to set background color for that box.
Any of the mentioned color value assigning methods can be used.

### HSL and HSLA colors

CSS3 has introduced the **hsl** color property for specifying colors. Format: `hsl(hue, saturation, lightness)`: 

* *hue* - it is the angle degree that represents the color on the color wheel. Values range between 0 and 360. 0 is red, 120 is green, and 240 is blue.

* *saturation* - it is the amount of gray in a color. Values are expressed as a percentage. 0% 
is a shade of gray, and 100% is the full color.

* *lightness* - it is the amount of white or black in a color. Values are represented as a percentage. 0% is black, and 100%  is white.

***Note*** HSLA has an extra value that indicates opacity. This value can be a number between 0.0 (means 0% opacity) and 1.0 (means 100% opacity).

## Chapter 12: Text

The properties to control the appearance of text can be split into two groups:

### properties that affect the font and its appearance

#### Font family

The `font-family` property is used to specify the typeface for element text. The value is the name of the typeface. It is important to point out that browsers will only display the typeface if it was already installed on the user's computer. 

It is preferred to use fonts from the following font families: *Serif*, *Sans-serif* and *Monospace*.

- Example: 

```
h1 {font-family: "Courier New", Courier, monospace;}
p {font-family: Arial, Verdana, sans-serif;}
```

***Note*** `@font-face` can be used if you want to use a font that might not be installed on the user's computer. This can be done by specifying a path to a copy of the font using `src`, which will be downloaded if it is not on the user's machine. Example:

```
@font-face {
font-family: 'ChunkFiveRegular'; src: url('fonts/chunkfive.eot');}

h1 {
font-family: ChunkFiveRegular, Georgia, serif;}
```

#### Font size

The `font-size` property is used to specify the font size. Text size units are:

* **Pixels**

* **Percentages**

> The default size of text in browsers is 16px. So a size of 75% would be the equivalent of  12px, and 200% would be 32px.

* An **em** is equivalent to the width of a letter m.

#### Font weight

The `font-weight` property is used to create **bold** text. It has two commonly used values: normal and bold.

#### Font style

The `font-style` property is used to create *italic* text. It has three commonly used values: normal, italic, and  oblique. 


### Properties that affect the text itself


#### Text case

The `text-transform` property is used to change the case of text. The values are: uppercase, lowercase, and capitalize; to capitalize the first letter of each word.

#### Underline and strike

The `text-decoration` property is used to specify the following values:

| value      | effect |
| -----------  | ----------- |
| none          | to remove any decoration already applied to the text |
| underline     | to add a line under the text        |
| overline      | to adds a line on top of the text   | 
| line-through  | to adds a line through words        | 
| blink         | to animate the text so it flashes on and off        | 

#### Leading

Leading is the vertical space (gap) between lines of text.

The `line-height` property sets the height of an entire line of text. Increasing the value of line-height makes the vertical gap between lines of text larger.

#### Letter and word spacing

The `letter-spacing` and `word-spacing` properties are used to control the gap between letters/words. The value should be in ems, and it will be added on top of the default value specified by the font.

#### Alignment

The `text-align` property is used to control the alignment of text. The values can be: *left*, *right*, *center*, and *justify*; which means that all the lines should take up the full width except the last line. 

* The `vertical-align` property is used to align inline elements such as images elements.

#### Indenting text

The `text-indent` property is used to indent the first line of text within an element. The amount you want the line indented by can be specified numerically using pixels or ems. I can also take negative values; so it pushes text off the browser window. 

#### First letter or line

Different values for the first letter or first line of text inside an element can be specified using `:first-letter` and `:first-line`. Those are not properties, they are *pseudo-elements*.
Pseudo-elements are specified at the end of the selector, then declare CSS as usual. Example:

```
p.intro:first-letter {
    font-size: 200%;}
p.intro:first-line {
    font-weight: bold;}
```

### Styling links

Browsers tend to show links in blue with an underline by default.

There are two pseudo-classes that can be used for styling links:

* *:link* - to set styles for links that have not yet been visited. 

* *:visited* - to set styles for links that have been clicked on.

Those classes are used to control colors of the links and whether they are to appear underlined or not.

#### Responding to users

There are three pseudo-classes that can be used change the appearance of elements when users interacting with the:

* *:hover* - it is applied when a user hovers over an element with a pointing device such as a mouse. It can be used to change the appearance of links and buttons when a user places their cursor over them.

* *:active* - it is applied when an element is being activated by a user.

* *:focus* - it is applied when an element has focus.

> Focus occurs when a browser discovers that you are ready to interact with an element on the page. For example, when your cursor is in a form input ready to accept typing, that element is said to have focus.

