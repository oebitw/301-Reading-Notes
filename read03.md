# Flexbox and Templating

![](https://labs.tadigital.com/wp-content/uploads/2020/06/featured-image.jpg)


## Flexbox
Before the Flexbox Layout module, there were four layout modes:

* Block, for sections in a webpage.
* Inline, for text.
* Table, for two-dimensional table data
Positioned, for explicit position of an element.
* The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.

### Flexbox Elements

To start using the Flexbox model, you need to first define a flex container.

![](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)
HTML:
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

CSS:
```
.flex-container {
  display: flex;
}
```


The flex container becomes flexible by setting the `display` property to `flex`

The flex container properties are:

* flex-direction

![](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)

```
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

* flex-wrap

![](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)

```
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

* flex-flow
```
.container {
  flex-flow: column wrap;
}
```

* justify-content

![](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)

```
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around
    | space-evenly | start | end | left | right ... + safe | unsafe;
}
```
* align-items
![](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

```
.container {
  align-items: stretch | flex-start | flex-end | center | baseline | first
    baseline | last baseline | start | end | self-start | self-end + ... safe |
    unsafe;
}
```
* align-content
![](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

```
.container {
  align-content: flex-start | flex-end | center | space-between | space-around |
    space-evenly | stretch | start | end | baseline | first baseline | last
    baseline + ... safe | unsafe;
}
```


## Templating
![](https://www.tsmean.com/assets/img/the-ultimate-mustache-tutorial/mustache-logo.png)


Mustache is a logic-less template syntax.

It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are replaced with a value, some nothing, and others a series of values.

```
Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn
```

In the above, we see two braces around {{ name }}. This is Mustache syntax to show that it is a placeholder.

In general, we would write templates according to the Mustache specification, and it can then be compiled by a templating engine to be rendered to create an output.

![](https://miro.medium.com/max/700/1*LbqYj87xlazySm6wE0Q2lA.png)
