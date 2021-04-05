# 201 Day 5
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
**HTML & CSS by John Duckett** - *pg. 94-125, 246-263, 264-299*<br/>


## HTML Images

Keep image storage organized. Include sub-folders within the site's images directory.

Where you place the `img` tag matters. `<img>` is an inline element.

Save your images at the same pixel resolution as it will appear or be used on the site.

## Color

You can specify color by: <br/>
`RGB Values / Hex Codes / Color Names / HSL`

When picking colors for a website, it's important to ensure there is enough contrast between background and foreground colors.

#### HSL
`hsl(hue[0-360degrees], saturation[percentage], lightness[percentage])`


## Text

Don't use more than three typefaces on a single page.<br/>

### Font Sizes
1. Pixels
2. Percentages
3. EM's

Browser's default font is 16 pixels. Follow the 16 point scale.

| Pixels | Percentages | EMS |
| -- | -- | -- |
| h1 - 32 pixels | h1 - 200% | h1 - 2em |
| h2 - 24 pixels | h2 - 150% | h2 - 1.5em |
| h3 - 18 pixels | h3 - 112.5% | h3 - 1.125em |
| p - 16 pixels | p - 100% | p - 1em |

To upload a custom font: 
```css
@font-face  {
  font-family: 'name';
  src: url('address of resource');
}
```

#### Text Transforms
- uppercase
- lowercase
- capitalize

```css
p {
  text-align: center, left, right, justify;
  vertical-align: text-top, baseline, text-bottom;
  text-indent: 20px;
}
in this order!!
p:first-letter
p:first-line
p:link
p:visited
p:hover
p:focus
p:active
```
