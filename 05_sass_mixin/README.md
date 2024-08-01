# Sass @import and Partials

Sass keeps the CSS code DRY (Don't Repeat Yourself). One way to write DRY code is to keep related code in separate files.

## Sass Importing Files
The `@import` directive allows you to include the content of one file in another.

The CSS `@import` directive has a major drawback due to performance issues; it creates an extra **HTTP** request each time you call it. However, the Sass `@import` directive includes the file in the CSS; so no extra HTTP call is required at runtime!
```SCSS
@import "filename";
```

## Sass Partials
Sass transpiles all the .scss files directly. However, when you want to import a file, you do not need the file to be transpiled directly.

Sass has a mechanism for this: If you start the filename with an **underscore**, Sass will not transpile it. Files named this way are called partials in Sass.
### Example: 
```SCSS 
_colors.scss // (This file will not be transpiled directly to "colors.css")
```