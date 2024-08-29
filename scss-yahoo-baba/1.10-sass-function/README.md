# Sass Function
Functions in Sass can take arguments, perform operations, and return a value.
### Basic Syntax
* `@function`: Keyword to define a function.
* `function-name`: The name of the function.
* `$arg1, $arg2, ...`: Arguments passed to the function.
`@return`: The value that the function returns.
```scss
@function function-name ($arg1, $arg2, $arg3) {
  // Function Logic Here !
  @return some-value;
}
```

### A Color Manipulation Function
You can use Sass functions to manipulate colors. For example, you could create a function that darkens a color by a certain percentage:
```scss
@function darken-color ($color, $amount) {
  @return darken($color, $value);
}
// Usage
.button {
  background-color: darken-color(#3498db, 10%);
  // This will output a darker shade of blue
}
```