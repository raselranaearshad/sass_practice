## Sass `@media` Directive
The `@media` directive in Sass is similar to the standard CSS `@media` rule, which is used for applying styles based on certain conditions like screen size, orientation, etc.
```scss
.container {
  width: 100%;
  
  @media (min-width: 768px) {
    width: 750px;
  }

  @media (min-width: 992px) {
    width: 970px;
  }

  @media (min-width: 1200px) {
    width: 1170px;
  }
}

```

### Explanation:

* The `.container` class will have different widths depending on the screen size.
* Sass compiles this into separate media queries, resulting in a clean and organized CSS file.

## Sass `@at-root` Directive
The `@at-root` directive is used to break out of the current nesting level and output the CSS at the root level. 

This is useful when you want to control where a piece of CSS is placed in the final output, regardless of the nested structure in your Sass file.

```scss
.parent {
  color: blue;
  
  .child {
    color: red;
    
    @at-root .another-child {
      color: green;
    }
  }
}

```
### Explanation:
* In this example, `.another-child` is nested within `.child`, but the `@at-root` directive moves it outside of `.parent` in the compiled CSS.
* The compiled CSS would look like this:
```css
.parent {
  color: blue;
}

.parent .child {
  color: red;
}

.another-child {
  color: green;
}
```