# 201 Day 6
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
[Understanding the Problem Domain](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming) <br/>
**Javascript & Jquery by John Duckett** - *pg. 100-105, 183-242*

## Understanding the Problem Domain
The article can be summed up with these main points:
- If you don't know what you're building, it's hard to build.
- Coding is easy, understanding the problem is the tough part.
- Start small, understand a small portion before tackling the rest. Break it into chunks.

## Object Literals

- Objects are composed of variables and functions.
- Variables in objects are known as properties.
- Functions in objects are known as methods.
- Literal notation is the most popular way. Store the object in a variable.
- You can access object's properties or methods through dot notation or bracket syntax.

## The DOM 

Manipulating the DOM requires two steps:
1. Access the element.
2. Update the element.

### Access Elements
getElementById() - selects an element with an id attribute. Must be unique. <br/>
querySelector() - Uses CSS selector syntax and only returns the first matching element: `li.hot` <br/>
getElementsByClassName() - selects all elements with a given class attribute. <br/>
getElementsByTagName() - self-explanatory. `img` or `li`. <br/>
querySelectorAll() - Uses CSS selector syntax but selects all elements that match.

### NodeLists
A nodelist is like an array and is numbered like an array, but they're known as collections. <br/>

To select an element from a nodelist you can use either the `item()` method or array syntax `element[1]`. <br/>

When you have a nodelist, you can apply an action to every member of the list using a for loop.

```javascript
var items = getQuerySelectorAll('li.hot');
for (let i = 0; i < items.length; i++) {
  items[i].className = 'test';
}
```

### Traversing the DOM
.parentNode
.previousSibling / .nextSibling
.firstChild / .lastChild

To select a "figs" node from this code `<li id="one"><em>fresh</em> figs </li>`
you would need to use: 
```javascript
document.getElementById('one').firstChild.nextSibling.nodeValue;
```

#### Adding an element to the DOM tree
```javascript
//Create a new element and store in variable
let newSection = document.createElement('section');
let text = document.createTextNode('oh yea this is a new section');

newSection.appendChild(text);
//Then target the location where it should be added
let spot = document.getElementsByTagName('ol')[3];
spot.appendChild(newSection);
```

### Removing an element from the DOM tree
```javascript
// select the element and the containing element
let section = document.querySelectorAll('div.section');
let divContainer = section.parentNode;
divContainer.removeChild(section);
```
### Attribute Nodes
- getAttribute()
- hasAttribute()
- setAttribute()
- removeAttribute()
- className
- id
