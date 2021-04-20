# 301 Day 7
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [REST APIs Explained](https://gist.github.com/brookr/5977550)

## Rest API

- Roy Fielding created the internet

From the reading:
>ME: So anyway, HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page. Web pages usually have images, right? Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.

>Brother: Sounds like GET is a pretty important verb.

>ME: It is. Especially when you're using a web browser because browsers pretty much just GET stuff. They don't do a lot of other types of interaction with resources. This is a problem because it has led many people to assume that HTTP is just for GETing. But HTTP is actually a general purpose protocol for applying verbs to nouns.

>Brother: Cool. But I still don't see how this changes anything. What kinds of nouns and verbs do you want?

>ME: Well the nouns are there but not in the right format.

>Think about when you're browsing around amazon.com looking for things to buy me for Christmas (whispers: VITAMIX!!!) . Imagine each of the products as being nouns. Now, if they were available in a representation that a machine could understand, you could do a lot of neat things.