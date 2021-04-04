# REST API

## What is Rest

REST is acronym for Representational State Transfer. It is architectural style for distributed hypermedia systems and was first presented by Roy Fielding in 2000 in his famous dissertation.

## Guiding Principles of REST
* Client-server — By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.


* Stateless — Each request from a client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. The session state is therefore kept entirely on the client.


* Cacheable — Cache constraints require that the data within a response to a request be implicitly or explicitly labelled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.


* Uniform interface — By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behaviour of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.


* Layered system — The layered system style allows an architecture to be composed of hierarchical layers by constraining component behaviour such that each component cannot “see” beyond the immediate layer with which they are interacting.


* Code on demand (optional) — REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.



REST API is one of the Design Philosophy.

1) Way of thinking about how to treat “resource”

2) When you access URL by specifying parameters, you can get XML or JSON.

3) It doesn’t manage the state of sessions.

4) You can get always the same result regardless of state or session. The resource is information like an article or video.


A RESTful web application exposes information about itself in the form of information about its resources. It also enables the client to take actions on those resources, such as create new resources (i.e. create a new user) or change existing resources (i.e. edit a post).

In order for your APIs to be RESTful, you have to follow a set of constraints when you write them. The REST set of constraints will make your APIs easier to use and also easier to discover, meaning a developer who is just starting to use your APIs will have an easier time learning how to do so.

REST stands for REpresentational State Transfer.

It means when a RESTful API is called, the server will transfer to the client a representation of the state of the requested resource.

For example, when a developer calls Instagram API to fetch a specific user (the resource), the API will return the state of that user, including their name, the number of posts that user posted on Instagram so far, how many followers they have, and more. The representation of the state can be in a JSON format, and probably for most APIs this is indeed the case. It can also be in XML or HTML format.

What the server does when you, the client, call one of its APIs depends on 2 things that you need to provide to the server:

An identifier for the resource you are interested in. This is the URL for the resource, also known as the endpoint. In fact, URL stands for Uniform Resource Locator.

The operation you want the server to perform on that resource, in the form of an HTTP method, or verb. The common HTTP methods are GET, POST, PUT, and DELETE.

## The difference between RESTful API and NOT RESTful API

If you think about creating the system that can operate to create, read, update and delete user information. You would need 4 URL for each request like below unless you use RESTful API.

```
// Assuming that you have a domain you want to request
https://example.com
// If you want…
// create, you need URL like this
https://example.com/createbook
// read
https://example.com/readbook
// update
https://example.com/updatebook
// delete
https://example.com/deletebook
```

If you use RESTful API, you don’t need to think about each process by using request methods. They are GET, POST, PUT and DELETE

```
// In this case, you need a URL to operate the information about the book
// and you can request methods.
https://example.com/book/
```

* GET:
Read a specific resource (by an identifier) or a collection of resources.

* PUT:
Update a specific resource (by an identifier) or a collection of resources. It can also be used to create a specific resource if the resource identifier is known before-hand.

* DELETE:
Remove/delete a specific resource by an identifier.

* POST:
Create a new resource. Also a catch-all verb for operations that don’t fit into the other categories.