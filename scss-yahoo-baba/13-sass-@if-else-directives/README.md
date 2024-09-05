# Sass @if & @else Directives
The `@if` and `@else` directives in Sass are used to control conditional logic within your stylesheets. These directives allow you to write code that behaves differently based on specific conditions.

### Basic Syntax of @if
The `@if` directive works similarly to conditionals in programming languages. It checks if a given condition is true, and if so, it executes the corresponding block of code.
```scss
@if condition {
  // code to be executed if condition is true
}
```
### Example of @if
```scss
$primary-color: blue;
  @if $primary-color == blue {
    body {
      background-color: blue;
    }
  }
/* In this example, if the $primary-color is blue, the background color of the body will be set to blue. */
```
### Adding @else if and @else
You can extend the `@if` directive by adding `@else` if and `@else` blocks.
```scss
@if condition1 {
    // Code to run if condition1 is true
} @else if condition2 {
    // Code to run if condition2 is true
} @else {
    // Code to run if none of the conditions are true
}
```
### Example of @else if and @else
```scss	
$theme : dark;

@if $theme == light {
    body {
        background-color: white;
        color: black;
    }
 } @else if $theme == dark {
   body {
     background-color: black;
     color: white;
   }
 } @else {
   body {
     background-color: lightgray;
     color: black;
   }
 }
```
In this example:

* If `$theme` is `light`, the body will have a white background with black text.
* If `$theme` is `dark`, the body will have a black background with white text.
* If neither condition is `true`, it will default to a gray background with black text.