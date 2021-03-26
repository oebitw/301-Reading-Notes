# Read: 01 - SMACSS and Responsive Web Design

![](https://miro.medium.com/max/3468/1*qF8LfAwUhl57g9T0BVvVdg.jpeg)

## Responsive Web Design:

Responsive web design is the practice of building a website suitable to work on every device and every screen size

### Responsive vs. Adaptive vs. Mobile: 

**Responsive** generally means to react quickly and positively to any change. With responsive design websites continually and fluidly change based on different factors, such as viewport width.

**adaptive** means to be easily modified for a new purpose or situation, such as change. Adaptive websites are built to a group of preset factors.

Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media.

### Flexible Layouts:

It is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units, like percentages or em units.
Flexible layouts do not advocate the use of fixed measurement units, such as pixels or inches.

There is an easy formula to help identify the proportions of a flexible layout using relative values.

`target ÷ context = result`

This an example on using the formula:

```
<div class="container">
  <section>...</section>
  <aside>...</aside>
</div>

```
We have a `div` contains two children elements a `section` and an `aside` .

```
.container {
  width: 538px;
}
 
section,
aside {
  margin: 1.858736059%; /*  10px ÷ 538px = .018587361 */
}
section {
  float: left;
  width: 63.197026%;    /* 340px ÷ 538px = .63197026 */   
}
aside {
  float: right;
  width: 29.3680297%;  /* 158px ÷ 538px = .293680297 */
}
```
At times the width of a browser viewport may be so small that even scaling the layout proportionally will create columns that are too small to effectively display content. 
In this case we will use **Media Queries**.

## Media Queries

Media queries provide the ability to specify different styles for individual browser and device circumstances, like the width of the viewport or device orientation.


There are a couple different ways to use media queries, using the @media rule inside of an existing style sheet, importing a new style sheet using the @import rule, or by linking to a separate style sheet from within the HTML document.
 

 Each media query may include a media type followed by one or more expressions.

We can use Logical operators in media queries to build powerful expressions. There are three different logical operators available for use within media queries, including and, not, and only.


The example below selects all media types between 800 and 1024 pixels wide.

```
@media all and (min-width: 800px) and (max-width: 1024px) {...}

```

We can add break points to the Media Queries where certain parts of the design will behave differently on each side of the breakpoint.

In the following example i will introduce the Typical Device Breakpoints:

```
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}
 
/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}
 
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}
 
/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}
 
/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
```
 
The best practice is to Always Design for Mobile First.
this means designing for mobile before designing for desktop or any other device (This will make the page display faster on smaller devices).

Instead of changing styles when the width gets smaller than 768px, we should change the design when the width gets larger than 768px. 

## Float

The float property is used for positioning and formatting content e.g. let an image float left to the text in a container.

The float property can have one of the following values:

* left : The element floats to the left of its container.

* right : The element floats to the right of its container.

* none : The element does not float (will be displayed just where it occurs in the text). This is default.

* inherit : The element inherits the float value of its parent.

![](https://miro.medium.com/max/840/1*CFwJ6lMQMOi4Oy7L8Mn17g.png)

We also have a property related to the float called **clear**.

The clear property specifies what elements can float beside the cleared element and on which side.

The clear property can have one of the following values:

* none - Allows floating elements on both sides. This is default.


* left - No floating elements allowed on the left side.

* right- No floating elements allowed on the right side.

* both - No floating elements allowed on either the left or the right side.

* inherit - The element inherits the clear value of its parent.

The most common way to use the clear property is after you have used a float property on an element.

![](https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/02/directionalclearing_kzfb8t.png?resize=540%2C226&ssl=1)


## SMACKS

SMACKS stands for Scalable and Modular
Architecture for CSS.

SMACKS is is more style guide than rigid framework.

With SMACKS we can organize our css in five different categories:

1) Base.css

It contains any general styling on top of what is provided by a reset.css 

2) Layout.css

It contains general positioning on the page for the ( header, footer, nav, aside, Classes and IDs can be included here as well )

3) Module.css

It contains smaller components on the page (Specific elements such as list items, individual images, specific paragraphs, etc..)

4) State.css 

It contains any styling that changes upon user interaction or state change

5) Theme.css

It contains small changes on top of all other normal styling, like applying temporary changes, such as a sales season theme.