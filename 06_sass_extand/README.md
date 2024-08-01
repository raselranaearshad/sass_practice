# Sass @extand and Inheritance
* The `@extend` directive lets you share a set of CSS properties from one selector to another.
* The `@extend` directive is useful if you have almost identically styled elements that only differ in some small details.
* The `@extend` directive helps keep your Sass code very DRY.
### Example: 
```SCSS
// This is example how we can create a @extend
.button-basic  {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}
// This is the example of Inheritance
.button-report  {
  @extend .button-basic;
  background-color: red;
}

.button-submit  {
  @extend .button-basic;
  background-color: green;
  color: white;
}
```
By using the `@extend directive`, you do not need to specify several classes for an element in your HTML code, like this: <button class="button-basic button-report">Report this</button>. You just need to specify .button-report to get both sets of styles.