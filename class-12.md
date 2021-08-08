Code 201 - Read 12

In this file, a summary of **Read: 12 - Docs for the HTML `<canvas>` Element & Chart.js** will be provided. The read covers multiple articles.

## Canvas element

[Basic usage of canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

The html `<canvas>` element is a graphics container used for drawing graphics on the page via JavaScript. The container is initially 300px wide and 150px high , but it can be assigned different values using the `width` and `height` attributes. Example:

```
<canvas id="demo" width="150" height="150"></canvas>

```

### Canvas grid/coordinate space

* 1 unit in the grid corresponds to 1 pixel on the canvas.

* The *origin* of the grid is positioned in the top left corner at coordinate (0,0).

* All elements are placed relative to the *origin*. So, in the figure, the blue square is positioned from the top left corner by **x** pixels from the **left** , and **y** pixels from the **top** - coordinate (x,y).

![blue square](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes/canvas_default_grid.png)

### The rendering context

The canvas is initially blank. To draw on it, do the following steps:

1. Access the ccanvas element through the script:

```
var canvas = document.getElementById('tutorial');
```

2. To obtain the rendering context its drawing functions, use the `getContext()` method. `getContext()` takes one parameter; the type of context. For 2D graphics, enter '2d':

```
var ctx = canvas.getContext('2d');
```

### Drawing shapes

[Drawing shapes with canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

To draw a rectangle, use the following functions:

1. `fillRect(x, y, width, height)` - draws a filled rectangle.
2. `strokeRect(x, y, width, height)` - draws a rectangular outline.
3. `clearRect(x, y, width, height)` - clears the specified rectangular area, making it fully transparent.

The *x* and *y* parameters provide the space coordinations, the *width* and *height* parameters provide the rectangle's size.

Example:

```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}
```

Result:
![rectangle](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes/canvas_rect.png)

### Drawing text

[Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

The canvas rendering context provides two methods to render text:

1. `fillText(text, x, y [, maxWidth])` - fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
2. `strokeText(text, x, y [, maxWidth])`  - strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

### Styling

[Applying styles and colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

#### Coloring

There are two properties for applying colors to a shape:

1. `fillStyle = color` - sets the style used when filling shapes.
2. `strokeStyle = color` - sets the style for shape's outlines.

`color` is a string representing a CSS color.

#### Styling text

There are multiple properties for applying text syles:

1. `font = value` - the current text style being used when drawing text. The default font is 10px sans-serif.
2. `textAlign = value` - text alignment setting. Possible values: start, end, left, right or center. The default value is start.
3. `textBaseline = value` - baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
4. `direction = value` - directionality. Possible values: ltr, rtl, inherit. The default value is inherit.


## Chart.js API

Article [link](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

*Charts* are used for displaying data visually.
e
*Chart.js* is a JavaScript plugin that uses the `<canvas>` element for drawing graphs onto a page. It makes using various kinds of charts -i.e. bar ,line, pie, etc- incredibly easy.

### Setting up

1. Download [Chart.js](https://github.com/chartjs/Chart.js) and unzip it.
2. Copy `Chart.min.js` into your repository.
3. Import the script to your html page: `<script src='Chart.min.js'></script>`

### Draw a line chart

1. Create a `<canvas>` element in the html file, so Chart.js can draw the chart in it:

```
<canvas id="buyers" width="600" height="400"></canvas>
```

2. Prepare the data in the script:

```
var buyerData = {
    labels : ["January","February","March","April","May","June"],
    datasets : [
                {
                fillColor : "rgba(172,194,132,0.4)",
                strokeColor : "#ACC26D",
                pointColor : "#fff",
                pointStrokeColor : "#9DB86D",
                data : [203,156,99,251,305,247]
                }
            ]
}
```

3. Get the line chart canvas:

```
var buyers = document.getElementById('buyers').getContext('2d');
```

4. Draw line chart:

```
new Chart(buyers).Line(buyerData);
```

### Draw a pie chart

1. Create a `<canvas>` element in the html file, so Chart.js can draw the chart in it:

```
<canvas id="countries" width="600" height="400"></canvas>
```

2. Prepare the data in the script, The data for the pie chart is a value and a color for each section:

```
var pieData = [
    { value: 20, color:"#878BB6"},
    {value : 40, color : "#4ACAB4"},
    {value : 10, color : "#FF8153"},
    {value : 30, color : "#FFEA88"}
    ];
```

3. Add pie chart options, These optionsremove the stroke from the segments, and then they animate the scale of the pie so that it zooms out from nothing.

```
var pieOptions = { 
    segmentShowStroke : false, 
    animateScale : true 
}
```

4. Get pie chart canvas:

```
var countries= document.getElementById("countries").getContext("2d");
```

5. draw pie chart:

```
new Chart(countries).Pie(pieData, pieOptions);
```

### Draw a bar chart

1. Create a `<canvas>` element in the html file, so Chart.js can draw the chart in it:

```
<canvas id="income" width="600" height="400"></canvas>
```

2. Add the bar char data:

```
var barData = {
    labels : ["January","February","March","April","May","June"],
    datasets : [
                {fillColor : "#48A497", strokeColor : "#48A4D1", data : [456,479,324,569,702,600]},
                {fillColor : "rgba(73,188,170,0.4)", strokeColor : "rgba(72,174,209,0.4)", data : [364,504,605,400,345,320]}
    ]
}
```

3. Get bar chart canvas:

```
var income = document.getElementById("income").getContext("2d");
```

4. Draw the bar chart:

```
new Chart(income).Bar(barData);
```

### Demo

The demo for the already given examples is shown [here](https://www.webdesignerdepot.com/cdn-origin/uploads7/easily-create-stunning-animated-charts-with-chart-js/chartjs-demo.html)

