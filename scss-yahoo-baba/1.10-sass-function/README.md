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
## Sass Number Functions
Sass **(Syntactically Awesome Style Sheets)** offers a variety of number functions that allow you to perform arithmetic and manipulate numbers directly within your stylesheets.
### 1. abs($number)
Returns the absolute value of a number.
```scss
.test{content: abs(-5)} // Return 5
.test{content: abs(3.5)} // Return 3.5
```
### 2.ceil($number)
Rounds a number **up** to the nearest whole number.
```scss
.test{content: ceil(4.2)} // Return 5
.test{content: ceil(-3.5)} // Return -3
```
### 3.floor($number)
Rounds a number **down** to the nearest whole number.
```scss
.test{content: floor(4.2)} // Return 4
.test{content: floor(-4.8)} // Return -5 
```
### 4. round($number)
Rounds a number to the nearest whole number.
```scss
.test{content: floor(4.2)} // Return 4
.test{content: floor(4.6)} // Return 5
```
### 5. min($number...)
Returns the **smallest** number from a list of numbers.
```scss
.test{content: min(5, 2, 8, -3)} // Return -3
```
### 6. max($number...)
Returns the **largest** number from a list of numbers.
```scss
.test{content: max(5, 2, 8, -3)} // Return 8
```
### 7. random($limit: null)
Generates a random number. If `$limit` is provided, it returns a random integer between `1` and `$limit;` otherwise, it returns a random number between `0 and 1`.
```scss
.test{content: random()} // Random number between 0 and 1
.test{content: random(10)} // Random number between 1 and 10
```
### 8. percentage($number)
Converts a number to a **percentage**.
```scss
.test{content: percentage(0.5)} // Return 50%
```
### 9. unit($number)
Returns the **unit** of a number.
```scss
.test{content: unit(10)} // Return ""
.test{content: unit(10rem)} // Return rem
```
### 10. unitless($number)
Returns whether a number has no unit.
```scss
.test{content: unitless(10)} // Return true
.test{content: unitless(10px)} // Return false
```
### 11. comparable($number1, $number2)
Returns whether two numbers can be compared. Two numbers are comparable if they have the same units or are both unitless.
```scss
.test{content: comparable(10, 5)} // Return true
.test{content: comparable(10px, 5em)} // Return false
.test{content: comparable(10px, 5px)} // Return true
```

## A Color Manipulation Function
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