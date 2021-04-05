# 201 Day 3
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 62-73, 300-329*<br/>
**Javascript & Jquery by John Duckett** - *pg. 70-73, 162-182*


## HTML Lists

There are three types of lists.

1. Unordered List
2. Ordered List
3. Definition List

To create a definition list (aka a glossary):

- Wrap the entire list with a `<dl>` tag.
- Wrap the term with a `<dt>` tag.
- Wrap the definition with a `<dd>` tag.

## CSS Boxes

Width, Height

min-height
min-width both define the minimum height that it can shrink to.

#### Using em
If you use `em`, the size of the box is based upon the size of the text within it.

### Overflowing Content
`overflow: hidden` will cause any text outside of the box to be chopped off.
`overflow: scroll` will add a scroll bar

### BMP

| Name | Definition | 
| -- | -- |
| Border | The edge of the box. |
| Margin | Margin sits outside the border |
| Padding | Padding is the space between the border and content inside. |

### Border Width
You have three options with `border-width:`:
1. pixels
2. `thick`, `thin` 
3. `1px 4px 12px 4px`

In the third example, it's defining the top width, then right width, bottom width, and finally the left width.

#### Border Styles
- solid
- dotted 
- dashed
- double
- groove
- ridge
- inset 
- outset
- hidden/none

You can also individualy style each side with `border-top-style:`.

### Border

`border: size, style, color`

#### Padding increases the size of the border from the content
#### Margin controls the gap between boxes

### Centering Content
`margin-left: auto; margin-right: auto;` will center the content vertically.

## Arrays

You can use the `.length` property to access the number of items within the array.

## Switch Statements

```javascript
switch (level) {
    case 'One':
    title = 'Level 1';
    break;

    case 'two':
    title = 'Level 2';

    case 'three';
    title = 'Level 3';

    default:
    title = 'Test';
    break;
}
```

| If else | Switch |
| -- | -- |
| "There is no need to provide an else option." | "You have a default option that is run if none of the cases match. |
| "With a series of if statements, they are all checed even if a match has been found (so it performs more slowly than switch). | :If a match is found, that code is run; then the break statement stops the rest of the switch statement |

## Loops

Simple Counter that counts to ten
```javascript
for (var i = 0; i <10; i++) {
    document.write(i);
}
```
#### for ( initialize, condition, update)

`break` is a keyword that terminates a loop and the interpreter moves to the next block of code.
