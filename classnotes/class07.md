# 201 Day 7
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>
[Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)
**HTML & CSS by John Duckett** - *pg. 126-145*<br/>
**Javascript & Jquery by John Duckett** - *pg. 106-144*

## HTML Tables
HTML Table Structure:
```html
<table>
    <tr>
        <th></th> <!-- Blank space for first column -->
        <th scope="col">First Column Heading</th>
        <th scope="col">Second Column Heading</th>
    </tr>
      <tr>
        <th scope="row">Row 1 Heading</th>
        <td colspan="2">number</td>
        <td>number</td>
    </tr>
      <tr>
        <th scope="row">Row 2 Heading</th>
        <td rowspan="1">number</td>
        <td>number</td>
    </tr>
</table>
```
Long Table Structure
```html
<table>
    <thead>
      <tr>
        <th></th>
        <th></th>
        <th></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th></th>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
        <td></td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td></td>
        <td></td>
      </tr>
    </tfoot>
</table>
```

## Functions, Methods, Objects

- Use the assignment operator to update properties of objects.

Creating an object with a constructor function:
```javascript
function name (parameters) {
    this.parameter1 = ;
    this.parameter2 = ;
    this.parameter3 = ;
    this.parameter4 = ;
    this.method = function (){};
}
let new = name(a,b,c,d);
```
Use the `delete` keyword to delete properties or methods from an object.

### this Keyword
`this` is a keyword that refers to the window object, which comes with default properties and includes all variables of global scope. When used within a method, it references the containing properties.

- Arrays can be placed within objects, and objects can be placed within arrays

### Built in Objects
1. Browser Object Model
2. Document Object Model
3. Global Javascript Objects

### String Objects

Properties
- length
Methods
- toUpperCase
- toLowerCase
- charAt - returns the character of the index number you provide
- indexOf - provides the index number of the first occurance of your character parameter
- lastIndexOf - provides last occurance
- substring - returns the characters between the two index numbers you provide
- split 
- trim - removes whitespace around end of string
- replace - find and replace

### Number Objects
Methods
- isNaN - check if value is not a number
- toFixed - rounds to specified number of decimal places (returns string)
- toPrecision - rounds to toal number of places (returns string)
- toExponential - the number in exponential notation.

### Math Object
Properties
- Math.PI - returns pi

Methods
- Math.round - returns number to nearest integer
- Math.sqrt - returns square root
- Math.ceil - rounds up to nearest integer
- Math.floor - rounds down to nearest integer
- Math.random - generates random number between 0 and 1.

### Date Object
- Dates are stored as numbers. (milliseconds)

Methods
- getDate
- getDay
- getFullYear
- getHours
- getMilliseconds
- getMinutes
- getMonth
- getSeconds
- getTime
- getTimezoneOffset
- toDateString
- toTimeString
- toString

To create a variable with today's year:
```javascript
let today = new Date();
let year = today.getFullYear();
```
