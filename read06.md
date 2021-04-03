# NODE.JS

![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/1200px-Node.js_logo.svg.png)

## What Is Node.js?

Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

The V8 engine is the open-source JavaScript engine that runs in Google Chrome, it is responsible for compiling JavaScript directly to native machine code that your computer can execute.

So Node.js is a program we can use to execute JavaScript on our computers. We can run JS in the terminal.

## Node Version Manager

nvm stands for Node Version Manager. As the name suggests, it helps you manage and switch between different Node versions with ease. It provides a command-line interface where you can install different versions with a single command, set a default, switch between them and much more.


## JavaScript Package Manager

Node comes bundled with a package manager called npm.

It puts modules in place so that node can find them, and manages dependency conflicts intelligently. It is extremely configurable to support a wide variety of use cases. Most commonly, it is used to publish, discover, install, and develop node programs.

npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week.

## Node.js Lets Us Run JavaScript on the Server

Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.

![](https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png)

## Are There Any Downsides?

The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.

## What are Node.js Modules

Consider modules to be the same as JavaScript libraries.

A set of functions you want to include in your application.

## Include Modules

To include a module, use the `require()` function with the name of the module:

```
let http = require('http');
```
Now your application has access to the HTTP module, and is able to create a server:

```
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/html'});
  res.end('Hello World!');
}).listen(8080);
```

## Create Your Own Modules
You can create your own modules, and easily include them in your applications.

The following example creates a module that returns a date and time object:


Create a module that returns the current date and time:
```
exports.myDateTime = function () {
  return Date();
};
```
Use the exports keyword to make properties and methods available outside the module file.

## Summary

* Node.js is an open source server environment.

* Node.js is free.

* Node.js runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.)

* Node.js uses JavaScript on the server.


* Here is how Node.js handles a file request:

A) Sends the task to the computer's file system.

B) Ready to handle the next request.

C) When the file system has opened and read the file, the server returns the content to the client.

* Node.js can generate dynamic page content.

* Node.js can create, open, read, write, delete, and close files on the server.

* Node.js can collect form data.

* Node.js can add, delete, modify data in your database.

* Node.js files contain tasks that will be executed on certain events.

* A typical event is someone trying to access a port on the server.

* Node.js files must be initiated on the server before having any effect.

* Node.js files have extension ".js"
