# Sass @extend Directive
### 1. Arithmetic Operators
Sass supports basic arithmetic operations:

* Addition (`+`): Adds two numbers.
```scss
$width: 100px;
$extra: 20px;
.box {
  width: $width + $extra; // 120px
}
```
* Subtraction (`-`): Subtracts one number from another.
```scss
$width: 100px;
$reduction: 30px;
.box {
  width: $width - $reduction; // 70px
}
```
* Multiplication (`*`): Multiplies two numbers.
```scss
$base: 10px;
$multiplier: 3;
.box {
  width: $width * 2; // 200px
}
```
* Division (`/`): Divides one number by another.
```scss
$width: 100px;
$divisor: 4;
.box {
  width: calc($width / $divisor); // 25px
}
```

### 2. Comparison Operators
These operators are used to compare values:

* Equal (`==`): Checks if two values are equal.
* Not Equal (`!=`): Checks if two values are not equal.
* Greater Than (`>`): Checks if the left value is greater than the right.
* Less Than (`<`): Checks if the left value is less than the right.
* Greater Than or Equal To (`>=`): Checks if the left value is greater than or equal to the right.
* Less Than or Equal To (`<=`): Checks if the left value is less than or equal to the right.

### 3. Boolean Operators
Sass also supports boolean logic:

* And (`and`): Returns true if both conditions are true.
* Or (`or`): Returns true if at least one condition is true.
* Not (`not`): Reverses the truth value of a condition.

### 4. Sring Operators
You can concatenate strings using the `+` operator:
```scss
$full-name: "John";
$last-name: "Doe";
.full-name {
  content: $full-name + " " + $last-name;
}
```

### 5. Color Operators
Sass allows you to manipulate colors:

* **Lighten:** Lightens a color by a specified amount.
* **Darken:** Darkens a color by a specified amount.
* **Saturate:** Increases the saturation of a color.
* **Desaturate:** Decreases the saturation of a color.
* **Adjust:** Adjusts the hue of a color.

```scss
$color: #3498db;
.light {
  background-color: lighten($color, 20%); // Lightened color
}
.dark {
  background-color: darken($color, 20%); // Darkened color
}

```