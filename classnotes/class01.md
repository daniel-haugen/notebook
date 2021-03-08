# 201 Day 1
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 2-11, 12-39, 176-199, 428-451, 452-475*<br/>
**Javascript & Jquery** - *Intro, pg. 11-52*

## HTML5 Layout

In the beginning, everything was a div container. Now there are more tags available to give your code more semantic meaning. They all act as div containers though.

Here's some of the tags:
1. `<header>`
2. `<footer>`
3. `<nav>`
4. `<article>`
5. `<aside>`
6. `<section>`
7. `<hgroup>`
8. `<figure>` and `<figcaption>`

If the container is not serving one of these purposes, use a div container.

You can wrap containers in `<a>` tags to make the entire container a link.

Older browsers that can't run HTML5 won't understand the new tags.

## Process and Design

1. ### Answer the Questions
    - Who is the target audience?
    - Why are they visiting your website?
    - What is your visitor trying to achieve?
    - What information does the visitor need?
    - How often will people visit your site?
2. ### Sitemap
It can be useful to create a card for each page of the website so you can visually move and group related pages to create a site heirarchy.

3. ### Wireframe
The wireframe is the layout design of the website. It designates the containers, their pixel width, and the information that will fill the box.

## ABC of Programming

A script is just a list of steps for a computer to process.
Define your goal, then define the steps required to reach the goal.

| Name | Description |
| -- | -- |
| Object | a thing. Each object can have its own properties, events, or methods. |
| Properties | The common characteristics of objects are known as properties. Each property has a name and a value. |
| Events | Events are user interactions with the web page that can be used to trigger code. |
| Methods | Methods are used to update the values of object properties. |  

The document object model is the computer's view of the webpage, beginning with the document object.

Each element in HTML is considered a node, which is a type of object, somewhere on the tree below the document object.

Javascript is run where it is found in the HTML document. If javascript is placed before an html element it changes in the browser, then it won't load properly. 

HTML holds the content, CSS provides the styling information, and Javascript creates interactions and event-driven changes to the document object model. 
