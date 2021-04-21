# 301 Day 8
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- [SuperAgent](https://visionmedia.github.io/superagent/)
- [RegExr](https://regexr.com/)
- [RegEx Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)


## API Design

A well designed web API should:
1. Allow any client to call the API
2. Grow without disrupting client applications currently using it

### REST

A REST web service could be written in any backend programming language but can be communicated with through HTTP protocol.

Standard HTTP Verbs:
1. GET - retrieves a representation of a resource at URI. The body of the response contains details of the requested resource.
2. POST - creates a new resource at the specificed URI. POST can also be used to trigger operations that don't create resources.
3. PUT - either creates or replaces the resource at the URI.
4. PATCH - performs partial update of a resource.
5. DELETE - removes the resource at the URI.

|Resource |	POST	| GET	| PUT	| DELETE |
|-|-|-|-|-|
|/customers |	Create a new customer	| Retrieve all customers	| Bulk update of customers	| Remove all customers |
|/customers/1	| Error	| Retrieve the details for customer 1	| Update the details of customer 1 if it exists	| Remove customer 1 |
|/customers/1/orders	| Create a new order for customer 1	| Retrieve all orders for customer 1	| Bulk update of orders for customer 1	| Remove all orders for customer 1 |

- A POST request creates a resource
- A PUT request creates or updates a resource
- A PATCH request performs a partial update to an existing resource.

>PUT requests must be idempotent. If a client submits the same PUT request multiple times, the results should always be the same (the same resource will be modified with the same values). POST and PATCH requests are not guaranteed to be idempotent. [source: MS Web API Design]

Example of a POST request that includes JSON data:
```javascript
POST https://adventure-works.com/orders HTTP/1.1
Content-Type: application/json; charset=utf-8
Content-Length: 57

{"Id":1,"Name":"Gizmo","Category":"Widgets","Price":1.99}
```




