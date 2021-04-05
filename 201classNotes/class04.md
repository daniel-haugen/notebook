# 201 Day 4
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 74-93, 358-404*<br/>
**Javascript & Jquery by John Duckett** - *pg. 86-99 + [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)*


## HTML Links

#### Relative Linking
`../` is for navigating to the parent folder.<br/>
`../../` is for navigating to the grandparent folder

`href="mailto:me@dnhaugen.com` will start a user's email client app and fill the to: field.
`target="_blank"` is a link attribute that will open the link in a new tab.

## CSS Layout

### Positioning

#### Normal Flow
Normal flow is the default positioning `position: static;`. Every block-level element begins on a new line even if there's enough width for blocks to sit side-by-side. 
#### Relative Positioning
Relative positioning is achieved by `position: relative;` and allows you to move a block-level element out of the normal flow of the document. Surrounding block-level elements will remain unaffected by any elements with relative positioning. If two containers are overlapping, you can control which appears in the foreground by using the `z-index` property.
#### Absolute Positioning
Absolute positioning a block-level element will completely remove the element from the normal flow of the document. The surrounding elements reposition as if the element with absolute positioning isn't there. As you scroll down a web page, anything absolutely positioned will scroll up with the page.
#### Fixed Positioning
Fixed position elements are removed from the normal flow of the document and positioned relative to the browser window. As you scroll down a page, the element will remain fixed to where it's positioned on the browser window.
#### Floating elements
By giving an element `position: float`, you can take it out of normal flow and allow other element's to fill in around it. Also use the `width:` property to show how wide the floated element should be. [Learn more here](https://css-tricks.com/all-about-floats/#:~:text=While%20floats%20can%20still%20be,all%20covered%20in%20this%20article)

`clear: both/left/right/none;` can be used to prevent an element from floating. 

## Functions, Methods, and Objects

An example function declaration: 
```javascript
function testFunction () {
    document.write('oh yea');
}
testFunction();
```
At the end, we call the function to invoke it and write "oh yea."

```javascript
function simpleAdd (a, b) {
    let sum = a + b;
    return sum;
}
```
### Function Declaration
- is named and creates a function that can be called.
- can be called before being declared, the javascript interpreter checks for all function declarations before going line-by-line.

### Function Expression
- they are anonymous functions
- cannot call this function before the interpreter has reached the line.

### Immediately Invoked Function Expression
code from John Duckett Javascript and JQuery
```javascript
var area = (function (){
    var width = 3;
    var height= 5;
    return width * height;
}());
```
The final () is calling the function immediately.

### Variable Scope

#### Local Variables
When a variable is created within a function, it can only be used within the function because it only has local scope / function-level scope.

#### Global Variables
Variables created outside of a function can be used anywhere in the script because it has global scope. 

#### Memory
quoted from John Duckett Javascript and JQuery:
>Global variables use more memory. The browser has to remember them for as long as the web page using them is loaded. Local variables are only remembered during the period of time that a function is being executed.

Another really important section from John Duckett:
>Naming Collisions
>>Many sites use scripts written by several people. If an HTML page uses two JavaScript files, and both have a global variable with the same name, it can cause errors.

Variables in Global Scope --> naming conflicts possible between JS files <br/>
Variables in Function Scope --> no naming conflicts <br/>

## Pair Programming
1. Driver
2. Navigator
<br/>
The driver handles the computer, navigator doesn't write code. 