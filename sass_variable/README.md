# Sass Variables
Variables are a way to store information that you can re-use later.

With Sass, you can store information in variables, like:

* strings
* numbers
* booleans
* colors
* lists
* nulls

Sass uses the $ symbol, followed by a name, to declare variables:
### Sass Variable Syntax:
```SCSS
$variablename: value;
```
## Sass Variable Scope
Sass variables are only available at the level of nesting where they are defined.

### SCSS Syntax:
```SCSS
$myColor: red;

h1 {
  $myColor: green;
  color: $myColor;
}

p {
  color: $myColor;
}
```
> NOTE:  We can't access from outside the $myColor varibale which is inside the h1 tag. If we want to use that variable globally then we have to use this code. ($myColor: green !global;) 