# Assignment 1: Class and ID Basics

## Objective
Practice using HTML class and id attributes and applying basic CSS styling to them.

## Instructions

Create an HTML file called `recipe-page.html` that contains a recipe page with the following requirements:

### HTML Requirements

1. Create a complete HTML document with proper structure (DOCTYPE, html, head, body)
2. Include a `<title>` element with "My Favorite Recipe"
3. Add the following elements with the specified classes and IDs:

   **IDs to include:**
   - Give the main `<header>` an id of "page-header"
   - Give the recipe title `<h1>` an id of "recipe-title"
   - Give the ingredients `<section>` an id of "ingredients-section"
   - Give the instructions `<section>` an id of "instructions-section"
   - Give the `<footer>` an id of "page-footer"

   **Classes to include:**
   - Give at least 3 ingredients the class "essential"
   - Give at least 2 instruction steps the class "important"
   - Create a paragraph with classes "note" and "warning" (multiple classes on one element)
   - Give the footer paragraph the class "copyright"

### CSS Requirements

Add a `<style>` section in the `<head>` and create CSS rules for:

1. Style the ID selectors:
   - `#page-header`: Give it a background color and padding
   - `#recipe-title`: Change the text color and center it
   - `#page-footer`: Add a top border and different background color

2. Style the class selectors:
   - `.essential`: Make the text bold and give it a different color
   - `.important`: Add a background color and padding
   - `.note`: Add a border around it
   - `.warning`: Make the text red

### Content Requirements

Your recipe should include:
- A recipe title
- A list of at least 6 ingredients (use `<ul>`)
- A list of at least 5 instruction steps (use `<ol>`)
- At least one note or tip paragraph
- A footer with copyright information

## Starter Code

Your should of course have a separate stylesheet files as styles.css.  I won't provide a template there.  

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My Favorite Recipe</title>
    <link rel="stylesheet" href="styles.css"
</head>
<body>
    <!-- Add your HTML content here -->
    
</body>
</html>
```

## Submission

1. Save your file as `recipe-page.html`
2. Test it in your browser to make sure all styles are applied correctly
3. Commit and push to your GitHub repository
4. Submit the link to your repository

