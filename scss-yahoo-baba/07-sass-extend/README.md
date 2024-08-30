# Sass @extend Directive
***
The `@extend` directive in Sass is a powerful feature that allows you to share styles between selectors. It helps to keep your CSS DRY `(Don't Repeat Yourself)` by allowing one selector to inherit the styles of another.

## Key Points
* **Inheritance:** When you use @extend, the styles of the extended selector are included in the extending selector. This means that if you change the styles of the base class, all classes that extend it will automatically inherit those changes.
* **Selector Grouping:** The resulting CSS will group selectors that share the same styles, which can help reduce the size of your CSS file.
* **Limitations:**
  * You cannot extend multiple selectors at once.
  * Extending a selector that is not a class (like an ID or element selector) can lead to unexpected results.
  * Be cautious with @extend in large projects, as it can lead to complex CSS selectors that may be hard to debug.

##  Example with Placeholder Selectors
You can also use `@extend` with placeholder selectors (using `%`), which are **not compiled** into CSS unless they are extended:
```scss
// Define a placeholder
%button-styles {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  color: white;
}

// Extend the placeholder
.primary-button {
  @extend %button-styles;
  background-color: green;
}

.secondary-button {
  @extend %button-styles;
  background-color: red;
}
```