# Sass Partials
***
### What are Sass Partials?
Sass partials are small Sass files that contain a portion of your CSS. They are typically used to break down your styles into manageable pieces, making it easier to maintain and organize your code. Partials are defined in separate files and are imported into a main stylesheet.

### Naming Convention

Partials are usually named with a leading underscore `_`. The underscore indicates that the file is a partial and should not be compiled into a standalone CSS file.

### Importing Partials
To use a partial in your main Sass file, you can use the @import directive. For example:
```scss
@import 'buttons';
@import 'variables';
```
When you compile your main Sass file (e.g., styles.scss), all the imported partials will be included in the final CSS output.

### Benefits of Using Partials
* **Modularity:** Partials allow you to break your styles into smaller, reusable components, making your codebase more organized.

* **Maintainability:** Smaller files are easier to manage and update. You can focus on specific components without navigating through a large stylesheet.

* **Reusability:** You can reuse partials across different projects or stylesheets, promoting consistency and reducing duplication.

* **Collaboration:** In a team environment, multiple developers can work on different partials simultaneously without causing merge conflicts in a single large file.