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

## Sass String Functions
Sass **(Syntactically Awesome Style Sheets)** provides several string functions that can help you manipulate and format strings in your stylesheets. 
### 1. quote($string)
Adds **quotes** around a string.
```scss
.test{content: quote(hello world)} // Return "hello world"
```
### 2. unquote($string)
**Removes quotes** from a string.
```scss
.test{content: unquote("Hello World")} // Return Hello World
```
### 3. str-length($string)
Returns the **number of characters** in a string.
```scss
.test{content: str-length("Hello World")} // Return index number 11
```
### 4. str-insert($string, $insert, $index)
**Inserts a substring** into a string at a specified index.
```scss
.test{content: str-insert("Hello World", " Beautiful", 7)} // Return Hello Beautiful World
```
### 5. str-index($string, $substring)
Returns the **index** of the first occurrence of a substring within a string. Returns null if the substring is not found.
```scss
.test{content: str-index("Hello World", "World")} // Return 7
```
### 6. str-slice($string, $start-at, [$end-at])
**Extracts** a substring from a string, starting at a specified index. Optionally, you can specify an end index.
```scss
.test{content: str-slice("hello world", 1, 5)}; // "hello"
```
### 7. to-upper-case($string)
Converts all characters in a string to **uppercase**.
```scss
.test{content: to-upper-case("hello world")} // Return HELLO WORLD  
```
### 8. to-lower-case($string)
Converts all characters in a string to **lowercase**.
```scss
.test{content: to-upper-case("Hello World")} // Return hello world
```
### 9. unique-id()
Generates a **unique** CSS identifier.
```scss
.test{content: unique-id()} // Return an unique id
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