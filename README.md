### Sprint guide
* @RestController: Marks a class as a REST controller where methods return JSON or XML data
* @RequestMapping: Maps HTTP requests to handler methods of REST controllers.
* @GetMapping: A shortcut for @RequestMapping with method = GET.
* @PostMapping: A shortcut for @RequestMapping with method = POST.
* @RequestParam: Binds query parameters to method parameters.
--------------
* @SpringBootApplication is a convenience annotation that adds all of the following:
* @Configuration: Tags the class as a source of bean definitions for the application context.
* @EnableAutoConfiguration: Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings. For example, if spring-webmvc is on the classpath, this annotation flags the application as a web application and activates key behaviors.
* @ComponentScan: Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.

-----------------

### RapidApi.com

## What is HTTP
HTTP is an application layer protocol, which means that it provides a standardized way for applications to communicate with each other over the internet. HTTP defines a set of request methods, response codes, headers, and message formats that are used to exchange data between clients and servers.
![image](https://github.com/user-attachments/assets/8d600174-321d-4386-8cb8-6e0497132e8f)

## Request methods
# GET
Think of GET as asking the server for a resource, like a webpage or an image. When you type a URL into your browser and hit Enter, your browser sends a GET request to the server asking for the contents of that webpage.

## POST
POST is like submitting a form to the server with some data. For example, when you submit a login form on a website, your browser sends a POST request to the server with your username and password.

## PUT
PUT is like updating a resource on the server. For example, if you edit your profile information on a website, your browser might send a PUT request to the server with the updated information.

## DELETE
DELETE is like asking the server to delete a resource. For example, if you want to delete a post on a social media website, your browser might send a DELETE request to the server.

## PATCH
PATCH is like updating a resource on the server, but only changing part of it. For example, if you only want to change the caption on an image on a website, your browser might send a PATCH request to the server.

--------------------------

### Response Codes
* 2xx: Success codes, like 200 OK, which means the request was successful and the server is sending back the requested data.
* 3xx: Redirection codes, like 301 Moved Permanently, which means the requested resource has moved to a new location and the client needs to update its URL.
* 4xx: Client error codes, like 404 Not Found, which means the requested resource couldn't be found on the server.
* 5xx: Server error codes, like 500 Internal Server Error, which means there was an error on the server that prevented it from fulfilling the request.

---------------------------

### HTTP methods
## GET
This method is used to retrieve a resource from the server. When a client sends a GET request, the server responds with the requested resource. This method is idempotent, which means that sending the same request multiple times should have the same effect as sending it once.

## POST
This method is used to submit data to the server for processing. When a client sends a POST request, the server processes the data and sends back a response. This method is not idempotent, which means that sending the same request multiple times may have different effects.

## PUT
This method is used to update an existing resource on the server. When a client sends a PUT request, the server replaces the existing resource with the new data provided by the client. This method is idempotent, which means that sending the same request multiple times should have the same effect as sending it once.

## DELETE
This method is used to delete a resource from the server. When a client sends a DELETE request, the server removes the specified resource from its storage. This method is idempotent, which means that sending the same request multiple times should have the same effect as sending it once.

## OPTIONS
This method is used to retrieve information about the communication options available for a resource. When a client sends an OPTIONS request, the server responds with a list of the available methods, headers, and other communication options for the specified resource.

## HEAD
This method is similar to the GET method, but it only retrieves the headers for a resource and not the body. When a client sends a HEAD request, the server responds with the headers for the specified resource but does not send the actual content.

## CONNECT
This method is used to establish a network connection to a resource. When a client sends a CONNECT request, the server responds with a tunnel that can be used to establish a secure connection to the specified resource.

## TRACE
This method is used to retrieve a diagnostic trace of the communication between a client and a server. When a client sends a TRACE request, the server responds with a message that contains a copy of the request and response headers.

-------------------------

### REST APIs follow six design principles which are as follows:

## Client-server Separation
Think of a waiter taking an order from a customer in a restaurant. The waiter is like the server and the customer is like the client. In the same way, the server provides services to the client, but they are separate and don't depend on each other.

## Stateless
Imagine you go to a shop to buy something, and the shopkeeper doesn't remember you from your previous visit. Similarly, the server doesn't remember anything about the previous requests made by the client. Each request contains all the information needed to process it, like ordering a pizza without the pizza maker remembering your previous orders.

## Cacheable
Sometimes when you go to a shop, the shopkeeper may remember the item you bought and suggest something similar. Similarly, the server can store the response to a request and use it to respond to future requests more quickly. This is called caching.

## Layered System
Just like a building has multiple floors, a RESTful API can have multiple layers, with each layer providing a different function. The client can interact with the top layer without knowing anything about the layers below it.

## Uniform Interface
Imagine a menu in a restaurant that has pictures and descriptions of each dish. In the same way, a RESTful API should have a consistent interface that all clients can understand. This includes using standard HTTP methods like GET, POST, PUT, and DELETE, and using URLs to identify resources.

## Code on Demand (optional)
Some RESTful APIs may provide executable code to the client, like a JavaScript function. This can be useful for adding additional functionality to the client without requiring it to be built into the initial application.


-----------------------

### Spring Rest Book

# REST - REpresentational State Transfer

* Client-Server—Concerns should be separated between clients and servers.
* Stateless—The communication between client and server should be stateless.
* Layered System—Multiple hierarchical layers such as gateways, firewalls, and proxies can exist between client and server.
* Cache—Responses from the server must be declared as cacheable or noncacheable.
* Uniform Interface— All interactions between client, server, and intermediary components are based on the uniformity of their interfaces.
* Code on demand—Clients can extend their functionality by downloading and executing code on demand.

# RESTful resources are abstract entities.

# REST components interact with a resource by ransferring its representations back and forth. they never directly interact with the resource.

## Richardson’s Maturity Model

# Level Zero
This is the most rudimentary maturity level for a service. Services in this level use HTTP as the transport mechanism and perform remote procedure calls on a single URI. Typically, POST or GET HTTP methods are employed for service calls. SOAP- and XML-RPC-based Web services fall under this level.

# Level One
The next level adheres to the REST principles more closely and introduces multiple URIs, one per resource. Complex functionality of a large service endpoint is broken down into multiple resources. However, services in this layer use one HTTP verb, typically POST, to perform all of the operations.

# Level Two
Services in this level leverage HTTP protocol and make the right use of HTTP verbs and status codes available in the protocol. Web services implementing CRUD operations are good examples of Level 2 services.

# Level Three
This is the most mature level for a service and is built around the notion of Hypermedia as the Engine of Application State, or HATEOAS. Services in this level allow discoverability by providing responses that contain links to other related resources and controls that tell the client what to do next.

----------------
# The Model View Controller, or MVC, is an architectural pattern for building decoupled Web applications.
