# Sass @mixin & @include
***

In Sass (Syntactically Awesome Style Sheets), `@mixin` and `@include` are powerful directives that allow you to create reusable styles. 

This helps keep your stylesheets DRY `(Don't Repeat Yourself)` and makes your code more maintainable.

## Benefits of Using Mixins
* **Reusability:** You can define styles once and reuse them across multiple selectors.
* **Maintainability:** If you need to change a style, you only have to do it in one place.
* **Flexibility:** You can pass parameters to mixins to customize styles as needed.

### @mixin & @include systex:
@mixin Syntex:
```scss
@mixin mixin-name ($agrument1, $argument2){
  // write your code here 
}
```
@include Syntex:
```scss
.button-primary {
  // Argument value will be px, color etc.
  @include mixin-name (argument-value1, argument-value2);
}
```
## @mixin
The `@mixin` directive is used to define a block of styles that can be reused throughout your stylesheet. You can also pass `arguments` to a mixin to make it more flexible.

### Example:
```scss
// Create a @mixin
@mixin button($color, $padding: 10px) {
  background-color: $color;
  color: white;
  padding: $padding;
  border: none;
  border-radius: 5px;
  cursor: pointer;

  &:hover {
    opacity: 0.8;
  }
}
```

In this example, we define a `mixin` called **button** that takes two parameters: `$color` and `$padding`. The `$padding` parameter has a default value of 10px.

## @include
The `@include` directive is used to include the styles defined in a mixin within a selector.

### Example:
```scss
.button-primary{
  @include button (blue);
}
.button-secondary{
  @include button (green, 15px);
}
.button-danger{
  @include button (red, 20px);
}
```
In this example, we create three classes, `.button-primary`, `.button-secondary` and `.button-danger`. The `.button-primary` class uses the button mixin with the color `blue`, while the .`button-secondary` class uses the mixin with the color green and a custom padding of 15px.