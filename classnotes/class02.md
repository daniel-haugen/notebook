# 201 Day 2
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 40-61, 226-245*<br/>
**Javascript & Jquery by John Duckett** - *Intro, pg. 53-84, 145-162*

## HTML Text

Here's a bunch of html tags related to text:

| Element | Description |
| -- | -- |
| `<h1>, <h2>, <h3>` | headings |
| `<p>` | paragraph text |
| `<b> <i>` | bold and italic |
| `<sup> <sub>` | superscript and subscript |
| `<br> <hr>` | line breaks and horizontal rules |
| `<strong> <em>` | strong and emphasis |
| `<blockquote> <q>` | blockquote is used for paragraph-long quotes, the `<q>` tag is for short quotes within a `<p>` tag. |
| `<abbr>` | abbr is used to specify the full term. |
| `<cite> <dfn>` | When referencing source, use the cite element. `<dfn>` is used to provide the definition to a word. |
| `<address>` | used to wrap information regarding the author of the webpage. |
| `<ins> <del> <s>` | `<del>` is a strikethrough, `<ins>` is underlined. `<s>` is strikethrough. |

#### Semantic Markup
Semantic markup is html markup that doesn't affect the structure of the page, but can still provide information for search engines and web|assist devices. For example, `<address>`.

## Introducing CSS

### Use External CSS
To use external CSS, you must connect it to the html page with a `<link>` tag in the `<head>`.

`<link href= "stylesheetLocation" type= "text/css" rel= "stylesheet">`

### Use Internal CSS

`<style>` tags are used to place CSS rules inline with the HTML. It can either be placed in `<head>` or `<body>`.

### Types of CSS Selectors

| CSS Selector | Example | Definition | 
| --- | --- | --- | 
| Universal Selector | `*` | selects all the elements on the page | 
| Type Selector | `h1` or `main` | matches with all instances of this type | 
| Class Selector | `.` | matches all elements with the designated class. `h1.bigtext` would result in any h1 elements with a class of `bigtext` | 
| ID Selector | `#` | matches all elements with the designated id. `h1#bigtext` would result in any h1 elements with an id of `bigtext` | 
| Child Selector | `>` | selects an element that is a **direct** (has to be direct) child of another. `main>p` would select `<p>` tags that are direct children of the `<main>` tag. | 
| Descendant Selector | `[space}` | selects an element that sits inside another element regradless if other elements are nested.| 
| Adjacent Sibling Selector | `+` | Targets the only the first instance of an element after an indicated element. `main+figure` would select the first instance of `<figure>` after `<main>`.
| General Sibling Selector | `~` | Matches elements that are siblings of each other. 


### Cascade Rules

#### Last Rule
If two selectors are duplicate, the latter takes control.

#### Specificity
Rules with increased specificity/granularity will take control. 

#### !important 
By adding `!important` to the end of a CSS property, you'll indicate that it takes priority over everything else.


## Basic Javascript

#### Data Types

| Type | Example | 
| -- | -- |
| Numeric | 0.75, 5, 10 |
| String | "this is a string" | 
| Boolean | Either 'true' or 'false' | 

### Rules for Naming Variables
1. Must begin with a letter, $ or an underscore.
2. Do not use dash or period.
3. Cannot use keywords or reserved words.
4. Variables are case sensitive.
5. Use descriptive names
6. Always use camelCase

"Values in an array are accessed as if they are in a numbered list."

| Arithmetic Operators | Example | Result |
| -- | -- | -- |
| Addition | + | Adds value together |
| Subtraction | - | Subtracts value from another |
| Division | / | Divides values |
| Multiplication | * | Multiplies two values |
| Increment | ++ | Increases value by 1 |
| Decrement | -- | Decreases value by 1 |
| Modulus | % | Delivers remainder |

| Comparison Operators | Example |
| -- | -- |
| == | Equal to | 
| != | Not equal to | 
| === | Strict equal to (data type enforcement) | 
| !== | Strict not equal to (data type enforcement) | 
| > | Greater than | 
| < | Less than | 
| >= | Greater than or equal to |
| <= | Less than or equal to |

| Logical Operators | Example |
| -- | -- |
| && | Logical and |
| `||` | Logical or |
| ! | Logical not | 


### If and If else Statements   
**if** statements evaluate a condition to determine whether or not to run a block of code. <br/>
**if else** statements evaluate a condition and determine whether 1 block of code gets run or another.
