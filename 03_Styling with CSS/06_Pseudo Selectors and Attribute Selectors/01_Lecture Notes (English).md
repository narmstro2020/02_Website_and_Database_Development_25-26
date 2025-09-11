# CSS Pseudo Classes, Classes, and Attribute Selectors
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

## 📚 Table of Contents

| Topic | Description |
|-------|-------------|
| [Introduction](#introduction) | Overview of advanced CSS selectors |
| [Vocabulary](#vocabulary) | Key terms and definitions |
| [1. Pseudo Classes](#1-pseudo-classes) | Interactive and structural pseudo-classes |
| [2. Pseudo Elements](#2-pseudo-elements) | Styling specific parts of elements |
| [3. Attribute Selectors](#3-attribute-selectors) | Selecting elements based on attributes |
| [Visual Aids](#visual-aids) | Diagrams and examples |
| [Summary](#summary) | Key takeaways |
| [Resources](#resources) | Additional learning materials |

---

## Introduction
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

In our previous lessons, we learned about basic CSS selectors like element selectors, class selectors, and ID selectors. Today, we'll explore more advanced selectors that give us precise control over styling: **pseudo-classes**, **pseudo-elements**, and **attribute selectors**. These powerful tools allow us to style elements based on their state, position, or attributes without adding extra HTML markup.

### Prerequisites Review
- ✅ HTML structure and semantic tags
- ✅ Basic CSS selectors (element, class, ID)
- ✅ CSS properties and values
- ✅ CSS box model and positioning
- ✅ CSS specificity and cascade

---

## Vocabulary
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

| Term | Definition | Example |
|------|------------|---------|
| **Pseudo-class** | A keyword added to selectors that specifies a special state of the selected element | `:hover`, `:focus` |
| **Pseudo-element** | A keyword that lets you style a specific part of the selected element | `::before`, `::after` |
| **Attribute Selector** | Selects elements based on an attribute or attribute value | `[type="text"]` |
| **State** | The current condition or mode of an element | hover state, visited state |
| **Structural Pseudo-class** | Selects elements based on their position in the document tree | `:first-child`, `:nth-child()` |
| **Dynamic Pseudo-class** | Selects elements based on user interaction | `:hover`, `:active` |
| **Double Colon (::)** | Modern syntax for pseudo-elements | `::before` instead of `:before` |
| **Single Colon (:)** | Syntax for pseudo-classes | `:hover`, `:visited` |

---

## 1. Pseudo Classes
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### What are Pseudo Classes?

Pseudo-classes are keywords that start with a colon `:` and allow you to select elements based on information that isn't contained in the document tree. They target elements in specific states or positions.

### Syntax
```css
selector:pseudo-class {
    property: value;
}
```

### Categories of Pseudo Classes

#### 1.1 Dynamic Pseudo Classes (User Interaction)

These respond to user actions:

##### **:hover**
Applies when the user hovers over an element with a pointing device (mouse).

```css
/* Basic hover effect */
a:hover {
    color: red;
    text-decoration: underline;
}

/* Button hover effect */
.button:hover {
    background-color: #0056b3;
    transform: scale(1.05);
    cursor: pointer;
}
```

##### **:active**
Applies when an element is being activated (clicked/pressed).

```css
button:active {
    background-color: #004085;
    transform: scale(0.95);
}
```

##### **:focus**
Applies when an element has received focus (keyboard or mouse).

```css
input:focus {
    outline: 2px solid blue;
    background-color: #f0f8ff;
}
```

##### **:visited**
Applies to links that have been visited by the user.

```css
a:visited {
    color: purple;
}
```

##### **:link**
Applies to links that have not yet been visited.

```css
a:link {
    color: blue;
}
```

#### 1.2 Structural Pseudo Classes

These select elements based on their position in the document structure:

##### **:first-child**
Selects the first child of its parent.

```css
/* First paragraph in any container */
p:first-child {
    font-weight: bold;
    margin-top: 0;
}

/* First list item */
li:first-child {
    color: red;
}
```

##### **:last-child**
Selects the last child of its parent.

```css
li:last-child {
    border-bottom: none;
}
```

##### **:nth-child(n)**
Selects elements based on their position using a formula.

```css
/* Select every odd row */
tr:nth-child(odd) {
    background-color: #f2f2f2;
}

/* Select every even row */
tr:nth-child(even) {
    background-color: white;
}

/* Select the 3rd child */
li:nth-child(3) {
    color: green;
}

/* Select every 3rd element starting from the first */
li:nth-child(3n) {
    font-weight: bold;
}
```

##### **:nth-of-type(n)**
Selects elements of a specific type based on their position.

```css
/* Second paragraph only */
p:nth-of-type(2) {
    color: blue;
}
```

##### **:first-of-type** and **:last-of-type**
Select the first or last element of a specific type.

```css
h2:first-of-type {
    margin-top: 0;
}

p:last-of-type {
    margin-bottom: 0;
}
```

##### **:only-child**
Selects elements that are the only child of their parent.

```css
p:only-child {
    font-style: italic;
}
```

#### 1.3 Form-Related Pseudo Classes

##### **:checked**
Applies to checked checkboxes or radio buttons.

```css
input[type="checkbox"]:checked {
    accent-color: green;
}

/* Style label when checkbox is checked */
input[type="checkbox"]:checked + label {
    font-weight: bold;
    color: green;
}
```

##### **:disabled** and **:enabled**
Target form elements based on their disabled state.

```css
input:disabled {
    background-color: #e0e0e0;
    cursor: not-allowed;
}

button:enabled {
    background-color: #007bff;
    cursor: pointer;
}
```

##### **:required** and **:optional**
Target form fields based on the required attribute.

```css
input:required {
    border: 2px solid red;
}

input:optional {
    border: 1px solid #ccc;
}
```

### Complete Example: Navigation Menu with Pseudo Classes

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Navigation with Pseudo Classes</title>
    <style>
        nav {
            background-color: #333;
            padding: 0;
        }
        
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }
        
        nav li {
            margin: 0;
        }
        
        nav a {
            display: block;
            color: white;
            padding: 15px 20px;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        /* Unvisited links */
        nav a:link {
            color: white;
        }
        
        /* Visited links */
        nav a:visited {
            color: #ddd;
        }
        
        /* Hover effect */
        nav a:hover {
            background-color: #555;
        }
        
        /* Active/clicked state */
        nav a:active {
            background-color: #000;
        }
        
        /* First menu item special style */
        nav li:first-child a {
            border-left: 3px solid #ff6b6b;
        }
        
        /* Last menu item special style */
        nav li:last-child a {
            border-right: 3px solid #4ecdc4;
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</body>
</html>
```

---

## 2. Pseudo Elements
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### What are Pseudo Elements?

Pseudo-elements allow you to style specific parts of an element without adding extra HTML. They use double colons `::` in modern CSS (though single colons still work for backwards compatibility).

### Syntax
```css
selector::pseudo-element {
    property: value;
}
```

### Common Pseudo Elements

#### 2.1 ::before and ::after

These create virtual elements before or after the content of an element. They **require** the `content` property.

##### **::before**
Inserts content before the element's content.

```css
/* Add quotation marks before blockquotes */
blockquote::before {
    content: """;
    font-size: 3em;
    color: #ccc;
    position: relative;
    top: 10px;
    margin-right: 10px;
}

/* Add icons before list items */
.checklist li::before {
    content: "✓ ";
    color: green;
    font-weight: bold;
}
```

##### **::after**
Inserts content after the element's content.

```css
/* Add "NEW" badge after certain links */
.new-link::after {
    content: " NEW";
    background-color: red;
    color: white;
    padding: 2px 5px;
    border-radius: 3px;
    font-size: 0.8em;
    margin-left: 5px;
}

/* Clear floats */
.clearfix::after {
    content: "";
    display: table;
    clear: both;
}
```

#### 2.2 ::first-line and ::first-letter

##### **::first-line**
Styles the first line of text in a block element.

```css
p::first-line {
    font-weight: bold;
    color: #333;
    text-transform: uppercase;
}
```

##### **::first-letter**
Styles the first letter of text in a block element (great for drop caps).

```css
/* Create a drop cap effect */
p::first-letter {
    font-size: 3em;
    float: left;
    line-height: 1;
    margin-right: 5px;
    color: #8b0000;
    font-family: Georgia, serif;
}
```

#### 2.3 ::selection

Styles the portion of text selected by the user.

```css
::selection {
    background-color: #ffeb3b;
    color: #333;
}

/* For Firefox */
::-moz-selection {
    background-color: #ffeb3b;
    color: #333;
}
```

### Complete Example: Article with Pseudo Elements

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Article with Pseudo Elements</title>
    <style>
        article {
            max-width: 600px;
            margin: 50px auto;
            font-family: Georgia, serif;
            line-height: 1.6;
        }
        
        /* Drop cap for first paragraph */
        article p:first-of-type::first-letter {
            font-size: 4em;
            float: left;
            line-height: 0.8;
            margin: 10px 10px 0 0;
            color: #c41e3a;
            font-weight: bold;
        }
        
        /* Style first line of first paragraph */
        article p:first-of-type::first-line {
            font-variant: small-caps;
            font-weight: bold;
        }
        
        /* Add decorative quotes to blockquotes */
        blockquote {
            position: relative;
            padding: 20px 40px;
            background-color: #f5f5f5;
            border-left: 4px solid #333;
            font-style: italic;
        }
        
        blockquote::before {
            content: """;
            position: absolute;
            top: -10px;
            left: 10px;
            font-size: 5em;
            color: #ccc;
        }
        
        blockquote::after {
            content: """;
            position: absolute;
            bottom: -40px;
            right: 10px;
            font-size: 5em;
            color: #ccc;
        }
        
        /* Custom selection color */
        ::selection {
            background-color: #ffd700;
            color: #000;
        }
        
        /* Add "Read more" after truncated text */
        .truncated::after {
            content: "... Read more";
            color: #007bff;
            cursor: pointer;
            font-style: normal;
        }
    </style>
</head>
<body>
    <article>
        <h1>The Art of Web Design</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. This first paragraph demonstrates the power of pseudo-elements in creating visually appealing text layouts without additional HTML markup.</p>
        
        <blockquote>
            Design is not just what it looks like and feels like. Design is how it works.
        </blockquote>
        
        <p class="truncated">This paragraph appears to be truncated and could contain more content</p>
    </article>
</body>
</html>
```

---

## 3. Attribute Selectors
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### What are Attribute Selectors?

Attribute selectors allow you to select elements based on their attributes or attribute values. They use square brackets `[]`.

### Types of Attribute Selectors

#### 3.1 [attribute]
Selects elements with the specified attribute, regardless of value.

```css
/* Select all elements with a title attribute */
[title] {
    cursor: help;
    border-bottom: 1px dotted #333;
}

/* Select all required form fields */
[required] {
    border: 2px solid red;
}
```

#### 3.2 [attribute="value"]
Selects elements where the attribute exactly equals the value.

```css
/* Select text inputs specifically */
input[type="text"] {
    border: 1px solid #ccc;
    padding: 5px;
}

/* Select submit buttons */
input[type="submit"] {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
}

/* Select specific link targets */
a[target="_blank"] {
    background: url('external-link-icon.png') no-repeat right;
    padding-right: 20px;
}
```

#### 3.3 [attribute~="value"]
Selects elements where the attribute contains the value as a whole word.

```css
/* Select elements with "button" as one of the classes */
[class~="button"] {
    display: inline-block;
    padding: 10px 15px;
}

/* This would match: class="button primary" or class="small button" */
/* But NOT: class="button-large" */
```

#### 3.4 [attribute|="value"]
Selects elements where the attribute starts with the value or value followed by a hyphen.

```css
/* Select elements with lang attribute starting with "en" */
[lang|="en"] {
    font-family: Arial, sans-serif;
}
/* Matches: lang="en", lang="en-US", lang="en-GB" */
```

#### 3.5 [attribute^="value"]
Selects elements where the attribute starts with the value.

```css
/* Select links starting with https */
a[href^="https"] {
    padding-left: 20px;
    background: url('secure-icon.png') no-repeat left;
}

/* Select links to PDFs */
a[href^="pdf/"] {
    background: url('pdf-icon.png') no-repeat right;
    padding-right: 20px;
}
```

#### 3.6 [attribute$="value"]
Selects elements where the attribute ends with the value.

```css
/* Select links to PDF files */
a[href$=".pdf"] {
    background: url('pdf-icon.png') no-repeat right;
    padding-right: 25px;
}

/* Select images with jpg extension */
img[src$=".jpg"] {
    border: 2px solid #ddd;
}
```

#### 3.7 [attribute*="value"]
Selects elements where the attribute contains the value anywhere.

```css
/* Select links containing "example" anywhere in href */
a[href*="example"] {
    color: orange;
}

/* Select images with "thumbnail" in the filename */
img[src*="thumbnail"] {
    width: 150px;
    height: 150px;
    object-fit: cover;
}
```

### Combining Attribute Selectors

You can combine multiple attribute selectors for more specific targeting:

```css
/* Text input that is required */
input[type="text"][required] {
    border-left: 4px solid red;
}

/* External links that open in new window */
a[href^="http"][target="_blank"] {
    color: purple;
    font-weight: bold;
}

/* Submit button that is disabled */
input[type="submit"][disabled] {
    background-color: #ccc;
    cursor: not-allowed;
}
```

### Complete Example: Form with Attribute Selectors

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form with Attribute Selectors</title>
    <style>
        form {
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        /* All input elements */
        input {
            display: block;
            width: 100%;
            margin-bottom: 15px;
            padding: 8px;
            box-sizing: border-box;
        }
        
        /* Text inputs */
        input[type="text"] {
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        /* Email inputs */
        input[type="email"] {
            border: 1px solid #ddd;
            border-radius: 4px;
            background: url('email-icon.png') no-repeat 98% center;
            background-size: 20px;
        }
        
        /* Password inputs */
        input[type="password"] {
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: #fff5f5;
        }
        
        /* Required fields */
        input[required] {
            border-left: 4px solid #ff6b6b;
        }
        
        /* Placeholder styling for specific placeholders */
        input[placeholder*="Enter"] {
            font-style: italic;
        }
        
        /* Submit button */
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 12px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        
        /* Disabled submit button */
        input[type="submit"][disabled] {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        
        /* Labels for required fields */
        label[for] {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        /* Add asterisk to required field labels */
        input[required] + label::after {
            content: " *";
            color: red;
        }
    </style>
</head>
<body>
    <form>
        <label for="username">Username</label>
        <input type="text" id="username" required placeholder="Enter your username">
        
        <label for="email">Email</label>
        <input type="email" id="email" required placeholder="Enter your email">
        
        <label for="password">Password</label>
        <input type="password" id="password" required placeholder="Enter your password">
        
        <label for="website">Website (optional)</label>
        <input type="text" id="website" placeholder="https://example.com">
        
        <input type="submit" value="Sign Up">
    </form>
</body>
</html>
```

---

## Visual Aids
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### Selector Specificity Comparison

```
Inline styles:          1000 points
ID selector:            100 points
Class selector:         10 points
Pseudo-class:          10 points  ← Same as class
Attribute selector:     10 points  ← Same as class
Pseudo-element:        1 point    ← Same as element
Element selector:       1 point
```

### Pseudo-class vs Pseudo-element Quick Reference

| Pseudo-classes (:) | Pseudo-elements (::) |
|-------------------|---------------------|
| Select entire elements | Select part of elements |
| Based on state or position | Create virtual content |
| `:hover`, `:focus`, `:nth-child()` | `::before`, `::after`, `::first-line` |
| Don't create new content | Can create new content |
| Single colon syntax | Double colon syntax (modern) |

### Attribute Selector Cheat Sheet

```css
[attr]           /* Has attribute */
[attr="val"]     /* Exact match */
[attr~="val"]    /* Contains word */
[attr|="val"]    /* Starts with value or value- */
[attr^="val"]    /* Starts with */
[attr$="val"]    /* Ends with */
[attr*="val"]    /* Contains anywhere */
```

---

## Summary
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### Key Takeaways

1. **Pseudo-classes** (`:`) select elements based on their state or position
   - User interaction: `:hover`, `:focus`, `:active`
   - Structure: `:first-child`, `:nth-child()`, `:last-child`
   - Form states: `:checked`, `:disabled`, `:required`

2. **Pseudo-elements** (`::`) style specific parts of elements or create virtual content
   - `::before` and `::after` require the `content` property
   - `::first-line` and `::first-letter` for typography
   - `::selection` for user-selected text

3. **Attribute selectors** (`[]`) target elements based on their attributes
   - Exact match: `[attr="value"]`
   - Partial matches: `^=` (starts), `$=` (ends), `*=` (contains)
   - Useful for styling forms and links

### Best Practices

- Use double colons `::` for pseudo-elements (modern syntax)
- Combine selectors for more specific targeting
- Remember that pseudo-classes and attribute selectors have the same specificity as classes
- Always include `content` property for `::before` and `::after`
- Use semantic HTML attributes that you can target with CSS
- Test interactive states (hover, focus) for accessibility

### Common Use Cases

- **Navigation menus**: Hover effects, active states
- **Forms**: Validation styling, required fields
- **Typography**: Drop caps, pull quotes
- **Lists**: Zebra striping, special first/last items
- **Links**: External link indicators, file type icons
- **Decorative elements**: Icons, badges, borders

---

## Resources
[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)

### Documentation
- [MDN - Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
- [MDN - Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)
- [MDN - Attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)

### W3Schools References
- [CSS Pseudo-classes](https://www.w3schools.com/css/css_pseudo_classes.asp)
- [CSS Pseudo-elements](https://www.w3schools.com/css/css_pseudo_elements.asp)
- [CSS Attribute Selectors](https://www.w3schools.com/css/css_attribute_selectors.asp)

### Interactive Learning
- [CSS Diner - Practice Selectors](https://flukeout.github.io/)
- [MDN CSS Selectors Game](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)

### Tools
- **WebStorm**: Use code completion for pseudo-classes and pseudo-elements
- **Git**: Track your CSS experiments and iterations
- **GitHub**: Share your assignments and get feedback

---

*Remember: Practice is key! Experiment with different combinations of these selectors to create engaging and interactive web pages.*

[↑ Back to Top](#css-pseudo-classes-classes-and-attribute-selectors)
