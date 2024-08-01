# Sass Nested Rules and Properties
---
## Sass Nested Rules
* Sass lets you nest CSS selectors in the same way as HTML.

### Example: 
```SCSS
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```
Notice that in Sass, the `ul`, `li`, and `a` selectors are nested inside the `nav` selector.

## Sass Nested Properties
Many CSS properties have the same prefix, like font-family, font-size and font-weight or text-align, text-transform and text-overflow.
### Example: 
```SCSS
font: {
  family: Helvetica, sans-serif;
  size: 18px;
  weight: bold;
}
text: {
  align: center;
  transform: lowercase;
  overflow: hidden;
}
```