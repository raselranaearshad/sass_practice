# Sass Tutorial
---
## What is Sass ?
* **SASS** stands for **S**yntactically **A**wesome **S**tyle **S**heet.
* Sass is an extension to CSS
* Sass is a CSS pre-processor
* Sass is completely compatible with all versions of CSS
* Sass reduces repetition of CSS and therefore saves time
> Sass was designed by **Hampton Catlin** and developed by **Natalie Weizenbaum** in 2006
## Why Use Sass?
Stylesheets are getting larger, more complex, and harder to maintain. This is where a CSS pre-processor can help.

Sass lets you use features that do not exist in CSS, like variables, nested rules, mixins, imports, inheritance, built-in functions, and other stuff.

### Example: 
```SCSS
/* define variables for the primary colors */
$primary_1: #a2b9bc;
$primary_2: #b2ad7f;
$primary_3: #878f99;

/* use the variables */
.main_header{
  background-color: $primary_1;
}
.menu_left{
  background-color: $primary_2;
}
.menu_right{
  background-color: $primary_3;
}
```

## How Does Sass Work?
A browser does not understand Sass code. Therefore, you will need a Sass pre-processor to convert Sass code into standard CSS.

This process is called transpiling. So, you need to give a transpiler (some kind of program) some Sass code and then get some CSS code back.

> NOTE: Transpiling is a term for taking a source code written in one language and transform/translate it into another language.