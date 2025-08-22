# Introduction to CSS - Lecture Notes

## Table of Contents

| Topic | Description |
|-------|-------------|
| [1. What is CSS?](#1-what-is-css) | Understanding CSS and its role in web development |
| [2. Brief History of CSS](#2-brief-history-of-css) | Evolution and versions of CSS |
| [3. CSS Selector Format](#3-css-selector-format) | Basic syntax and structure |
| [4. Inline CSS](#4-inline-css) | Styling directly in HTML elements |
| [5. Internal CSS](#5-internal-css) | Styling within the HTML document |
| [6. External CSS](#6-external-css) | Linking separate CSS files |
| [Vocabulary](#vocabulary) | Key terms and definitions |
| [Summary](#summary) | Key takeaways |
| [Resources](#resources) | Additional learning materials |

---

## 1. What is CSS?

[⬆ Back to Top](#table-of-contents)

### Definition
**CSS** stands for **Cascading Style Sheets**. It is a styling language used to describe how HTML elements should be displayed on a webpage.

### Purpose
Think of HTML as the skeleton of a webpage - it provides structure. CSS is like the clothing and makeup - it makes everything look good!

### The Relationship Between HTML and CSS

```
HTML = Structure (What content appears)
CSS = Presentation (How content looks)
```

### Visual Analogy
Imagine building a house:
- **HTML** = The frame, walls, and rooms (structure)
- **CSS** = The paint, decorations, and furniture (style)

### Why Use CSS?
1. **Separation of Concerns**: Keep structure (HTML) separate from presentation (CSS)
2. **Reusability**: One CSS rule can style multiple HTML elements
3. **Consistency**: Maintain uniform styling across your entire website
4. **Efficiency**: Change the look of hundreds of pages by editing one CSS file

---

## 2. Brief History of CSS

[⬆ Back to Top](#table-of-contents)

### Timeline

| Year | Version | Key Features |
|------|---------|--------------|
| 1996 | CSS1 | Basic styling: fonts, colors, spacing |
| 1998 | CSS2 | Positioning, media types |
| 2011 | CSS3 | Animations, gradients, shadows, responsive design |
| Present | CSS3+ | Ongoing modular updates |

### Before CSS
In the early days of the web, all styling was done directly in HTML using attributes like:
```html
<font color="red">This is red text</font>
```
This made websites hard to maintain and update!

### Why CSS Was Created
- To solve the problem of mixing content with presentation
- To give web designers more control over layout
- To reduce repetitive code

---

## 3. CSS Selector Format

[⬆ Back to Top](#table-of-contents)

### Basic CSS Syntax

Every CSS rule consists of two main parts:

```css
selector {
    property: value;
}
```

### Components Explained

1. **Selector**: What HTML element(s) to style
2. **Property**: What aspect to change (color, size, etc.)
3. **Value**: What to change it to
4. **Declaration**: A property-value pair
5. **Declaration Block**: Everything inside the curly braces `{}`

### Visual Diagram

```
    selector
       ↓
    h1 {
        color: blue;     ← declaration
        ↑       ↑
    property  value
        
        font-size: 24px; ← another declaration
    }
    ↑                 ↑
    opening          closing
    brace            brace
```

### Multiple Declarations
You can have multiple declarations in one rule:

```css
p {
    color: navy;
    font-size: 16px;
    line-height: 1.5;
}
```

### Comments in CSS
Use `/* */` to add comments:

```css
/* This is a comment in CSS */
h1 {
    color: green; /* This makes headings green */
}
```

---

## 4. Inline CSS

[⬆ Back to Top](#table-of-contents)

### Definition
Inline CSS is CSS written directly in an HTML element using the `style` attribute.

### Syntax
```html
<tag style="property: value;">Content</tag>
```

### Examples

#### Example 1: Styling a Paragraph
```html
<p style="color: red;">This text is red!</p>
```

#### Example 2: Multiple Properties
```html
<h1 style="color: blue; font-size: 36px;">Big Blue Heading</h1>
```

#### Example 3: Styling Different Elements
```html
<!DOCTYPE html>
<html>
<head>
    <title>Inline CSS Example</title>
</head>
<body>
    <h1 style="color: purple;">Welcome!</h1>
    <p style="color: green; font-size: 18px;">This is a green paragraph.</p>
    <p style="background-color: yellow;">This has a yellow background.</p>
</body>
</html>
```

### Common Properties for Inline CSS

| Property | Description | Example Values |
|----------|-------------|----------------|
| `color` | Text color | `red`, `#FF0000`, `rgb(255,0,0)` |
| `background-color` | Background color | `yellow`, `#FFFF00` |
| `font-size` | Size of text | `16px`, `1.5em`, `large` |
| `text-align` | Alignment of text | `left`, `center`, `right` |
| `font-family` | Font type | `Arial`, `"Times New Roman"` |

### Pros and Cons

**Pros:**
- Quick for testing
- Overrides other CSS (highest specificity)
- No external files needed

**Cons:**
- Not reusable
- Mixes presentation with content
- Hard to maintain
- Makes HTML messy

---

## 5. Internal CSS

[⬆ Back to Top](#table-of-contents)

### Definition
Internal CSS (also called embedded CSS) is written in the `<head>` section of an HTML document using the `<style>` tag.

### Syntax
```html
<head>
    <style>
        selector {
            property: value;
        }
    </style>
</head>
```

### Complete Example
```html
<!DOCTYPE html>
<html>
<head>
    <title>Internal CSS Example</title>
    <style>
        h1 {
            color: navy;
            text-align: center;
        }
        
        p {
            color: gray;
            font-size: 16px;
            line-height: 1.6;
        }
        
        strong {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph with <strong>important</strong> text.</p>
    <p>All paragraphs will have the same style!</p>
</body>
</html>
```

### Element Selectors
Select HTML elements by their tag name:

```css
h1 { color: blue; }
p { font-size: 14px; }
em { font-style: italic; }
strong { font-weight: bold; }
```

### Styling Multiple Elements
Apply the same style to multiple elements:

```css
h1, h2, h3 {
    font-family: Arial;
    color: darkblue;
}
```

### Pros and Cons

**Pros:**
- Styles apply to the whole page
- Keeps styles separate from HTML content
- Can reuse styles for multiple elements

**Cons:**
- Only works for one HTML page
- Not reusable across different pages
- Increases page file size

---

## 6. External CSS

[⬆ Back to Top](#table-of-contents)

### Definition
External CSS is written in a separate `.css` file and linked to HTML documents.

### Creating the Link
Use the `<link>` tag in the `<head>` section:

```html
<link rel="stylesheet" href="styles.css">
```

### File Structure Example
```
my-website/
│
├── index.html
├── about.html
├── contact.html
└── styles.css
```

### HTML File (index.html)
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Site</h1>
    </header>
    <main>
        <section>
            <h2>About Us</h2>
            <p>We create amazing websites!</p>
        </section>
    </main>
    <footer>
        <p>© 2024 My Website</p>
    </footer>
</body>
</html>
```

### CSS File (styles.css)
```css
/* Reset default margins */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Header styles */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

/* Main content styles */
main {
    padding: 20px;
}

section {
    margin-bottom: 30px;
}

h2 {
    color: #333;
    border-bottom: 2px solid #333;
    padding-bottom: 5px;
}

/* Footer styles */
footer {
    background-color: #f0f0f0;
    text-align: center;
    padding: 10px;
    color: #666;
}
```

### Linking CSS from Different Directories

#### CSS in a subfolder:
```
my-website/
│
├── index.html
└── css/
    └── styles.css
```

Link: `<link rel="stylesheet" href="css/styles.css">`

#### CSS in parent folder:
```
my-website/
│
├── styles.css
└── pages/
    └── about.html
```

Link from about.html: `<link rel="stylesheet" href="../styles.css">`

### Multiple CSS Files
You can link multiple CSS files:

```html
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/layout.css">
<link rel="stylesheet" href="css/colors.css">
```

### Pros and Cons

**Pros:**
- Complete separation of content and presentation
- Reusable across multiple HTML pages
- Smaller HTML files
- Can be cached by browsers (faster loading)
- Easy to maintain and update

**Cons:**
- Requires an extra HTTP request
- Might cause a flash of unstyled content (FOUC)

---

## Vocabulary

[⬆ Back to Top](#table-of-contents)

| Term | Definition |
|------|------------|
| **CSS** | Cascading Style Sheets - language for styling HTML |
| **Selector** | Identifies which HTML elements to style |
| **Property** | The aspect of an element you want to change |
| **Value** | What you want to change the property to |
| **Declaration** | A property-value pair (e.g., `color: blue;`) |
| **Declaration Block** | Group of declarations inside curly braces |
| **Inline CSS** | CSS written directly in HTML elements using `style` attribute |
| **Internal CSS** | CSS written in the `<style>` tag within HTML `<head>` |
| **External CSS** | CSS written in separate `.css` files |
| **Cascade** | The order in which CSS rules are applied |
| **Style Sheet** | A collection of CSS rules |
| **Link Tag** | HTML element used to connect external CSS files |
| **Specificity** | Rules determining which CSS rule applies when multiple rules target the same element |

---


## Summary

[⬆ Back to Top](#table-of-contents)

### Key Takeaways

1. **CSS makes websites beautiful** - It controls colors, fonts, spacing, and layout
2. **Three ways to add CSS**:
   - **Inline**: Quick but not reusable
   - **Internal**: Good for single pages
   - **External**: Best for multi-page websites
3. **CSS Syntax** is consistent: `selector { property: value; }`
4. **Separation of concerns** - Keep structure (HTML) separate from style (CSS)
5. **External CSS is usually best** for real websites because it's:
   - Reusable across pages
   - Easy to maintain
   - Keeps HTML clean

### CSS Priority (Cascade)
When multiple CSS rules apply to the same element:
1. **Inline CSS** (highest priority)
2. **Internal CSS**
3. **External CSS** (lowest priority)

### Best Practices
- Start with external CSS for consistency
- Use internal CSS for page-specific styles
- Use inline CSS sparingly (testing or overrides only)
- Keep your CSS organized with comments
- Use meaningful names for your CSS files

---

## Resources

[⬆ Back to Top](#table-of-contents)

### Documentation
- [MDN CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools CSS Tutorial](https://www.w3schools.com/css/)
- [CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

### CSS Properties Reference
- [W3Schools CSS Properties](https://www.w3schools.com/cssref/)
- [MDN CSS Properties Index](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)

### Tools
- **WebStorm**: Your IDE for writing HTML and CSS
- **Git**: Version control for tracking changes
- **GitHub**: Host and share your code

### Practice Resources
- [W3Schools CSS Exercises](https://www.w3schools.com/css/exercise.asp)
- [CSS Basics on MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)

### Next Steps
After mastering these basics, you'll learn about:
- Class and ID selectors
- The box model
- Flexbox and Grid layouts
- Responsive design
- CSS animations

---

*Remember: The best way to learn CSS is by practicing! Start with simple styles and gradually add more complexity as you become comfortable.*