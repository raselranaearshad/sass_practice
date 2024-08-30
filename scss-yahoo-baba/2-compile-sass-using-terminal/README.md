# Installing SASS Using Terminal
Run this command to install sass using npm:
```npm
npm install -g sass
```
or 
```npm
npm install sass --save-dev
```

When you install Sass on the command line, you’ll be able to run the sass executable to compile.
```npm 
sass foldername/inputfile.scss foldername/outputfile.scss
```
You can also watch individual files or directories with the `--watch` flag. The watch flag tells Sass to watch your source files for changes, and re-compile CSS each time you save your Sass.

If you wanted to watch (instead of manually build) your input.scss file, you’d just add the watch flag to your command, like so:
```npm
sass --watch input.scss output.css
```

### Fun fact:
Sass has two syntaxes! The SCSS syntax (.scss) is used most commonly. It’s a superset of CSS, which means all valid CSS is also valid SCSS. 

The indented syntax (.sass) is more unusual: it uses indentation rather than curly braces to nest statements, and newlines instead of semicolons to separate them.

`.scss` syntex example: 
```scss
$primary-font: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $primary-font;
  color: $primary-color;
}
```
`.sass` syntex example: 
```sass
$primary-font: Helvetica, sans-serif
$primary-color: #333
  body
    font: 100% $primary-font
    color: $primary-color
```