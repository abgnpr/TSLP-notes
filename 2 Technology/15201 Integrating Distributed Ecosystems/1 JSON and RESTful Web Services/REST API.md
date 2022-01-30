# REST API

> Representational State transfer refers to a group of software architecture design constraints that bring about efficient, reliable, and scalable systems.

It's an architecture and design methodology.



What is an API?

> A set of features and rules that exist inside a software program enabling interaction between the software and other items, such as other software or hardware.



What is the difference between a web app and a web application?

web app: all files comprising the UI are download to the client at once. And when there's any change in data, the UI is capable to update itself accordingly at the client the, It does not need to fetch new files from the server to show the updated UI.



URI

> "A compact sequence of characters that identifies an abstract or physical resource" that "provides a simple and extensible means for identifying a resource".

URL

> Subset of URI that identifies a resource and explains how to access that resource by rpoviding an explicit method like https:// or ftp://

What is the relationship between URIs, URLs, and URNs?

A URN can be a URL and both are always URIs.



![Screenshot (22)](.images/Screenshot (22).png)

Six Constraints

- 

How REST relates to HTTP

A REST API that works over the HTTP(s) protocol is called a REST**ful** API. In other words, a RESTful API is a service that runs on the web over HTTP to facilitate access to web resources.

Who can interact with a REST API?

Anyone, unless the REST API includes an authentication layer or similar access restrictions.

REST is a stateless protocol. What does this mean?

No client context or information (aka “state”) can be stored on the server between requests.

What is a REST API?

an application programming interface that follows the six constraints of REST

What is a "resource"?

any information that can be named can be a resource

What is the minimum requirement to send a successful REST request?

The request must contain a method (verb) and a URI.

What is the POST method used to do?

- Post a new resource with a unique ID on the REST server.

  Correct

- Post a request to the REST server.

- Check for mail on the REST server.

- Post a comment or a form submission.