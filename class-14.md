# Code 201 - Read 14

In this file, a summary of **Read: 14a - CSS Transforms, Transitions, and Animations** and **Read: 14b - What Google Learned About Teams** will be provided.

## Read: 14a - CSS Transforms, Transitions, and Animations

### Topic 1 - CSS Transforms

The `transform` property is used to apply 2D or 3D transformation to an element, i.e. you can rotate, scale, move or skew elements. Syntax:

```
selector {
    transform: value;
}
```

#### 2D Transforms 

[Lesson 7 - Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

They work on the **x** (horizontal) and **y** axes (vertical) axes.

* **2D Rotate** `transform: rotate(degree)` - used to rotate an element from 0 to 360 degrees. A positive degree value will rotate the element *clockwise*, a negative value will rotate the element *counterclockwise*.

* **2D Scale** `transform: scale(value)` - used to change the appeared size of an element. The default scale value is 1, values<1 make the element appear *smaller*, while values>1 make the element appear *larger*. Scaling the height and width of an element with different values simultaneously can be done using `transform: scaleX(value)` and `transform: scaleY(value)`

* **2D Translate** `transform: translate(valueX, valueY);` - used to change the position of an element by pushing and pulling it in different directions without interrupting the normal flow of the document. It works a bit like *relative positioning*. Translate can also change the position of the element on the horizontal axis using `translateX` and on the vertical axis using `translateY`.

* **2D Skew** `transform: skew(valueX, valueY)` - used to distort elements on the horizontal axis, vertical axis, or both.

[2D Transforms](https://miro.medium.com/max/1400/1*_NVMTnvHTM9teQxrVRlDeg.png)

#### 3D Transforms

They work on the **x** (horizontal) and **y** axes (vertical) axes, as well as the **z** axis to define the *depth*.

* **3D Rotate** - the same as *2D rotate* but it can also rotate an element around any axes. To do so, set three new transform values, including `rotateX`, `rotateY`, and `rotateZ`.

* **3D Scale** - the same as *3D scale* but it can also scale the element on the z axis using `scaleZ`.

* **3D Translate** - the same as *3D scale* but elements may also be translated on the z axis using `translateZ`. A negative value here will push an element further away on the z axis, resulting in a *smaller* element. A positive value will pull an element closer on the z axis, resulting in a *larger* element.

* There is no 3d skew transformation.

### Topic 2 - Transitions & Animations

[Lesson 8 - Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

For a transition to take place, an element must have a change in *state*, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.

not all properties may be transitioned, only properties that have an identifiable halfway point. A list of popular transitional properties: background-color, background-position, border-color, border-width, border-spacing, bottom, clip, color, crop, font-size, font-weight, height, left, letter-spacing, line-height, margin, max-height, max-width, min-height, min-width, opacity, outline-color, outline-offset, outline-width, padding, right, text-indent, text-shadow, top, vertical-align, visibility, width, word-spacing, z-index.

To build a transition, the properties are to be used:

1. `transition-property` - it determines exactly what properties will be altered in conjunction with the other transitional properties. By default, it will alter all of the properties within an element’s different states upon the change.

2. `transition-duration` - it sets the duration in which a transition takes place.

3. `transition-timing-function` - it sets the speed in which a transition will move. Some popular values for it are: linear, ease-in, ease-out, and ease-in-out.

4. `transition-delay` - it sets a time value that determines how long a transition should be stalled before executing.

To see examples: [8 simple css3 transitions](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

## Read: 14b - What Google Learned About Teams

[What Google Learned From Its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

Teams are now the fundamental unit of organization. If a company wants to outstrip its competitors, it needs to influence not only how people work but also how they work together.

Studies show that team-based work has the following advantages:

* Teams tend to innovate faster
* Teams see mistakes more quickly
* Teams find better solutions to problems
* People working in teams tend to achieve better results
* People working in teams report higher job satisfaction

As a result, Google became focused on building the perfect team. So in 2012, the company embarked what they called *Project Aristotle*; to study hundreds of Google’s teams and figure out why some stumbled while others soared.

The researchers noticed two behaviors that all the good teams generally shared:

1. Conversational turn-taking - members spoke in roughly the same proportion
2. Average social sensitivity - members were skilled at intuiting how others felt based on their tone of voice, expressions and other nonverbal cues.

Within psychology, researchers refer these two traits as aspects of *psychological safety*.

Within psychology, researchers sometimes colloquially refer these two traits as aspects of *psychological safety*.

> Psychological safety is a sense of confidence that the team will not embarrass, reject or punish someone for speaking up, It describes a team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves. Edmondson, 1999.

Project Aristotle research pointed psychological safety, more than anything else, was critical to making a team work, even though that there were other behaviors that seemed vital to success, like making sure teams had clear goals and creating a culture of dependability.

Establishing psychological safety is somewhat messy and difficult to implement. The behaviors that create psychological safety are part of the same unwritten rules we often turn to, as individuals, when we need to establish a bond. And those human bonds matter as much at work as anywhere else.

> What Project Aristotle has taught people within Google is that no one wants to put on a work face when they get to the office. No one wants to leave part of their personality and inner life at home. But to be fully present at work, to feel ‘‘psychologically safe,’’ we must know that we can be free enough, sometimes, to share the things that scare us without fear of recriminations. We must be able to talk about what is messy or sad, to have hard conversations with colleagues who are driving us crazy. We can’t be focused just on efficiency. Rather, when we start the morning by collaborating with a team of engineers and then send emails to our marketing colleagues and then jump on a conference call, we want to know that those people really hear us. We want to know that work is more than just labor.

So, when most work­places shied away from emotional conversations, Google’s research have led them to conclude that in the best teams, members listen to one another and show sensitivity to feelings and needs. In other words, Google in its race to build the perfect team, has demonstrated the usefulness of imperfection and realized that to build good teams, they aim to create psychological safety faster, better and in more productive ways.
