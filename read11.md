# EJS

![](https://www.w3jar.com/wp-content/uploads/2019/05/express-js-template-engine.png)

## Introduction

EJS simply stands for Embedded JavaScript templates, and we can use it both server-side or client-side. In this article, we’ll focus on the server-side.

**Basic Syntax**:
* `<% 'Scriptlet'` tag, for control-flow, no output.

* `<%= Outputs` the value into the template (HTML escaped).

* `<%- Outputs` the unescaped value into the template.


## Partials

In this section we’ll learn how to use <%- include(‘’)-%> tag.

First of all let's move to the steps to install and prepare EJS to work with:

* Install EJS

```
npm i ejs
```
* Server.js will look like :

```
const express = require('express')
let path = require('path');
const app = express();
const port = 3000;

// view engine setup
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');

//setup public folder
app.use(express.static('./public'));
app.get('/',function (req, res) {
res.render('pages/home')
});
app.listen(port, () => console.log(`MasterEJS app Started on port ${port}!`));
```

* Set up the view engine and the views directory

```
// view engine setup
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');
```
* set up our public folder for static files

```
//setup public folder
app.use(express.static('./public'));
```

* add the ‘/’ route to render the views/pages/home.ejs page

```
app.get('/',function (req, res) {
res.render('pages/home')
});
```

## Render Links

In this section, we’ll discuss how to render links dynamically.

```
app.get('/links',function (req, res) {
//array with items to send
let items = [
{name:'node.js',url:'https://nodejs.org/en/'},
{name:'ejs',url:'https://ejs.co'},
{name:'expressjs',url:'https://expressjs.com'},
{name:'vuejs',url:'https://vuejs.org'},
{name:'nextjs',url:'https://nextjs.org'}];
res.render('pages/links',{
links:items
})
});
```



This time at res.render function after the name of the file we want to render we pass a JSON object.

```
res.render('pages/links',{
links:items
});
```
This JSON object will pass to the view pages/links.ejs. At this point, we use foreach function to iterate the links array and use “<%=” tag to output the properties url and name.

```
<% links.forEach(function(entry) {%>
<a href="<%= entry.url%>" class="list-group-item text-dark"><%=entry.name%></a>
<%});%>
```


## Conclusion

EJS lets us spin up quick applications when we don’t need anything too complex. By using partials and having the ability to easily pass variables to our views, we can build some great applications quickly.