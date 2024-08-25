# Sass Variable
***
Think of variables as a way to store information that you want to reuse throughout your stylesheet. You can store things like colors, font stacks, or any CSS value you think you’ll want to reuse. Sass uses the $ symbol to make something a variable.
### Example:
```scss
$font-family: Helvetica, sans-serif;
$primary-color: red;

body{
  font-family: $font-family;
  color: $primary-color;  
}
```

When the Sass is processed, it takes the variables we define for the `$font-family` and `$primary-color` and outputs normal CSS with our variable values placed in the CSS.