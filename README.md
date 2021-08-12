# What is REST
REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called RESTful systems, are characterized by how they are stateless and separate the concerns of client and server. We will go into what these terms mean and why they are beneficial characteristics for services on the Web.

# Guiding Principles of REST
* Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.
* Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
* Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.
* Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.
* Layered system – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
* Code on demand (optional) – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.

# Making Requests
REST request generally consists of:

* an HTTP verb, which defines what kind of operation to perform.
* a header, which allows the client to pass along information about the request.
* a path to resource and message body containing data if required.

# Resource Methods
There are 4 commonly used HTTP method in REST system:

* GET — retrieve a specific resource (by id) or a collection of resources
* POST — create a new resource
* PUT/PATCH — update a specific resource (by id)
* DELETE — remove a specific resource by id

You can learn more about these HTTP methods in the following document:
* [HTTP Methods](HTTPMethods.md)

# Choosing an HTTP Status Code and Standalization
HTTP defines these standard status codes that can be used to convey the results of a client’s request. The status codes are divided into the five categories.

* 1xx: Informational – Communicates transfer protocol-level information.
* 2xx: Success – Indicates that the client’s request was accepted successfully.
* 3xx: Redirection – Indicates that the client must take some additional action in order to complete their request.
* 4xx: Client Error – This category of error status codes points the finger at clients.
* 5xx: Server Error – The server takes responsibility for these error status codes.

You can lean more about HTTP Status code in the following document:
* [HTTP Status Codes](https://httpstatuses.com/)

# Endpoint Naming
The following is a highlight of some of the endpoint naming best practices.  For a full list of best practices view https://restfulapi.net/resource-naming/.

* Resources should be represented using nouns instead of verbs (no CRUD names). For example, don't use Get/Read/Fetch in your resource naming
* Heirarchical relationships should be separated by a forward slash (/) and use dashes (-) instead of underscores for multi-word resource names:  <div style="display: inline">https://myservice.domain.com/catalog/bikes/mountain-bikes</div>
* Use query components to filter data:  <div style="display: inline">https://myservice.domain.com/catalog/bikes/mountain-bikes?color=green&brand=coolbikes</div>


# Documentation
Altho documentation isn't something we should really cover part of REST API but it's important to utilize tools like swagger to represent your API endpoints. This should cover what your API expects and what it outputs. Most people implement Swagger but do not go the extra mile to document properly. Without going too deep into the how let's talk about what you should document. it's very important when you implement swagger documentation you cover what is required for your endpoint, what different types of response an consume can expect with status codes, don't forget to include your 50x, and 40x errors, and lastly document your required authentication type.
