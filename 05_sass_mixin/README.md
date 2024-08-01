# Sass @mixin and @include
---
## Sass Mixins
* The `@mixin` directive lets you create CSS code that is to be reused throughout the website.
* The `@include` directive is created to let you use (include) the mixin.

## Defining a Mixin
A mixin is defined with the `@mixin` directive.
```SCSS
@mixin name {
  property: value;
  property: value;
}
```
> NOTE: A tip on hyphens and underscore in Sass: Hyphens and underscores are considered to be the same. This means that @mixin important-text { } and @mixin important_text { } are considered as the same mixin!

## Using a Mixin
The @include directive is used to include a mixin.
```SCSS
selector {
  @include mixin-name;
}
```
> NOTE: A mixin can also include other mixins.
```SCSS
@mixin special-text {
  @include important-text;
  @include link;
  @include special-border;
}
```

## Passing Variables to a Mixin
Mixins accept arguments. This way you can pass variables to a mixin.
```SCSS
  /* Define mixin with two arguments */
@mixin bordered($color, $width) {
  border: $width solid $color;
}

.myArticle {
  @include bordered(blue, 1px);  // Call mixin with two values
}

.myNotes {
  @include bordered(red, 2px); // Call mixin with two values
}
```
## Using a Mixin For Vendor Prefixes
Another good use of a mixin is for vendor prefixes.
```SCSS
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}

.myBox {
  @include transform(rotate(20deg));
}
```
