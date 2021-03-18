# 201 Day 9
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 144-175, 330-357*<br/>
**Javascript & Jquery by John Duckett** - *pg. 243-292*

## Forms
Types of form inputs:
- Text input
- Password input
- Text area

Making choices in forms:
- Radio buttons
- Checkboxes
- Drop-down boxes

Submitting forms:
- Submit buttons
- Image buttons
- File upload

```html
<form action="http:..." method="get"> <!-- OR <fieldset> -->
  <input type="text" name="username"/>
  <input type="password" name="password"/>
   <input type="radio" name="blueorred" value="blue"/>Blue
   <input type="radio" name="blueorred" value="red"/>Red
  <textarea name="comments"> </textarea>
  <input type="submit" name="submit">
  </form>
```

## Lists, Tables, Forms
If there is an empty cell in a table:
`empty-cells: show;` or `empty-cells: hide;`

To put gaps between cells use the `border-spacing` and `border-collapse` properties.

Cursor styles:
- auto
- crosshair
- default
- pointer
- move
- text
- wait
- help
- url("cursor.gif")

## Javascript Events

There are a ton of different events that can occur within the browser that we can capture to trigger our own javascript code. This is done by binding an event listener to the DOM node element and then stating in our app what code we'd like to run in response.

1. HTML Event Handlers (bad practice)
2. Traditional DOM Handlers
3. DOM Level 2 Event Handlers - Event Listeners (best practice)

```javascript
element.addEventListener('event', functionName, [Boolean]) //(boolean typically set to false)
```

Whenever an event occurs, an event object is created which contains information about the fired event.

### User Interface Events
- load
- unload
- error
- resize
- scroll

### Mouse Events
- click
- dblclick
-mousedown
- mouseup
- mouseover
- mouseout
- mousemove

### Keyboard Events
- input
- keydown 
- keypress
- keyup

### Form Events
- submit
- change
- input

### Mutation Events & Observers
- DOMNodeInserted
- DOMNodeRemoved
- DOMSubtreeModified
- DOMNodeInsertedIntoDocument
- DOMNodeRemovedFromDocument

### HTML5 Events
- DOMContentLoaded
- hashchange
- beforeunload