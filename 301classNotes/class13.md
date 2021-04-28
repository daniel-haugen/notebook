# 301 Day 13
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [Status Codes for CRUD App](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)
- [Video: Build REST API](https://www.youtube.com/watch?v=fgTGADljAeg)



## SQL Vs NoSQL

In your own words, describe what each group of status code represents:
100’s = 100 level status codes are status updates that say 'everything so far is okay'
200’s = 200 level status codes are success related. Loading resources, contacting API's successfully, etc.
300’s = 300 level status codes are for redirections for outdated / deprecated URLs.
400’s = 400 level status codes are for all types of client errors.
500’s = 500 level status codes are for all types of server errors.
1. What is a status code 202?
A status code 202 states that a request is validated but not necessarily processed succesfully.
2. What is a status code 308?
A status code 308 is specific to reading resources. If the URL is no longer the current URL, a 308 will redirect that request to the updated URL.
3. What code would you use if an update didn’t return data to a client?
I would use a `204 No Content` status code.
4. What code would you use if a resource used to exist but no longer does?
410 status code
5. What is the ‘Forbidden’ status code?
403 is the forbidden status code


## Questions
1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
If we didn't, then the server code would have our database URL and anyone could access it.


2. What is middleware?
Code that runs when the server gets a request but before it's passed to your route. 

3. What does app.use(express.json()) do?
this allows your server to accept straight JSON as input.

4. What does the /:id mean in a route?
This means that whatever parameters are passed into the server can be accessible through `req.params.id`

5. What is the difference beween PUT and PATCH?
PUT will make changes to every field within an entry whereas PATCH can update singular fields within an entry and leaving the rest of the entry in tact.

6. How do you make a defalut value in a schema?
To make a default schema you use`new mongoose.Schema`

7. What does a 500 error status code mean?

A 500 error is a server-error.

8. What is the difference between a status 200 and a status 201?
200 is a success code, 201 means it was successful and a new resource has been created because of it.