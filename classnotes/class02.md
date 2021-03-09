# 201 Day 2
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 40-61, 226-245*<br/>
**Javascript & Jquery** - *Intro, pg. 53-84, 145-162*

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
| Class Selector | `.` denoted by a period | matches all elements with the designated class. `h1.bigtext` would result in elements with a class of bigtext | 
| Universal Selector | `*` | selects all the elements on the page | 
| Universal Selector | `*` | selects all the elements on the page | 
| Universal Selector | `*` | selects all the elements on the page | 
