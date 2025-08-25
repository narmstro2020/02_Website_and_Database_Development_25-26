# CSS Colors, Units, and Fonts - Lecture Notes

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

## Table of Contents

| Topic | Description |
|-------|-------------|
| [Introduction](#introduction) | Overview of CSS colors, units, and fonts |
| [CSS Colors](#css-colors) | RGB, RGBA, HSL, HSLA, Hexadecimal, and Named Colors |
| [CSS Units](#css-units) | Absolute and Relative Units |
| [CSS Fonts](#css-fonts) | Font Properties and Web Typography |
| [Vocabulary](#vocabulary) | Key terms and definitions |
| [Assignments](#assignments) | Practice exercises |
| [Summary](#summary) | Key takeaways |
| [Resources](#resources) | Additional learning materials |

---

## Introduction

In this lesson, we'll explore three fundamental aspects of CSS styling that will transform your web pages from plain text to visually appealing designs. You'll learn how to add colors, control sizing with different units, and style text with various font properties.

### Prerequisites
- HTML document structure (DOCTYPE, html, head, body)
- Basic HTML tags (h1-h6, p, em, strong)
- Semantic HTML (header, footer, main, section, article)
- Lists (ul, ol, li)
- Links and images
- Basic CSS syntax and selectors from previous lessons

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## CSS Colors

CSS provides multiple ways to specify colors. Each method has its advantages and use cases.

### 1. Named Colors

CSS supports 140 standard color names that you can use directly.

```css
/* Using named colors */
p {
    color: red;
    background-color: lightblue;
}

h1 {
    color: darkgreen;
    background-color: gold;
}
```

**Common Named Colors:**
- Primary: red, blue, green, yellow
- Neutrals: black, white, gray, silver
- Extended: coral, salmon, turquoise, violet

### 2. Hexadecimal Colors

Hexadecimal (hex) colors use a # followed by 6 characters (0-9 and A-F).

```css
/* Hexadecimal color format: #RRGGBB */
p {
    color: #FF0000;      /* Pure red */
    background-color: #00FF00;  /* Pure green */
}

h1 {
    color: #0000FF;      /* Pure blue */
    background-color: #FFFFFF;  /* White */
}

/* Shorthand hex (when pairs match) */
h2 {
    color: #F00;        /* Same as #FF0000 */
    background-color: #0F0;     /* Same as #00FF00 */
}
```

**Understanding Hex Colors:**
- First two characters: Red value (00-FF)
- Middle two characters: Green value (00-FF)
- Last two characters: Blue value (00-FF)
- 00 = no color, FF = maximum color

### 3. RGB Colors

RGB uses decimal values from 0-255 for Red, Green, and Blue.

```css
/* RGB color format: rgb(red, green, blue) */
p {
    color: rgb(255, 0, 0);      /* Pure red */
    background-color: rgb(0, 255, 0);   /* Pure green */
}

h1 {
    color: rgb(0, 0, 255);      /* Pure blue */
    background-color: rgb(128, 128, 128); /* Gray */
}

/* Mixing colors */
h2 {
    color: rgb(255, 165, 0);    /* Orange */
    background-color: rgb(128, 0, 128);  /* Purple */
}
```

### 4. RGBA Colors

RGBA adds an alpha channel for transparency (0 = fully transparent, 1 = fully opaque).

```css
/* RGBA format: rgba(red, green, blue, alpha) */
p {
    background-color: rgba(255, 0, 0, 0.5);   /* 50% transparent red */
}

section {
    background-color: rgba(0, 0, 255, 0.3);   /* 30% opaque blue */
}

/* Layering with transparency */
header {
    background-color: rgba(0, 0, 0, 0.8);     /* 80% opaque black */
    color: rgba(255, 255, 255, 1);            /* Fully opaque white */
}
```

### 5. HSL Colors

HSL stands for Hue, Saturation, and Lightness - a more intuitive color model.

```css
/* HSL format: hsl(hue, saturation%, lightness%) */
p {
    color: hsl(0, 100%, 50%);      /* Red */
    background-color: hsl(120, 100%, 50%);  /* Green */
}

h1 {
    color: hsl(240, 100%, 50%);    /* Blue */
}

/* Creating color variations */
section {
    background-color: hsl(200, 50%, 70%);   /* Light blue */
}
```

**Understanding HSL:**
- Hue: 0-360 degrees on color wheel (0=red, 120=green, 240=blue)
- Saturation: 0% = gray, 100% = full color
- Lightness: 0% = black, 50% = normal, 100% = white

### 6. HSLA Colors

HSLA adds transparency to HSL colors.

```css
/* HSLA format: hsla(hue, saturation%, lightness%, alpha) */
article {
    background-color: hsla(60, 100%, 50%, 0.5);  /* 50% transparent yellow */
}

footer {
    background-color: hsla(0, 0%, 0%, 0.9);      /* 90% opaque black */
}
```

### Visual Color Guide

```css
/* Complete color example */
body {
    background-color: #f0f0f0;  /* Light gray background */
}

header {
    background-color: rgb(51, 51, 51);  /* Dark gray */
    color: white;
}

main {
    background-color: rgba(255, 255, 255, 0.95);  /* Slightly transparent white */
}

footer {
    background-color: hsl(210, 50%, 30%);  /* Dark blue */
    color: hsla(0, 0%, 100%, 0.9);  /* Slightly transparent white */
}
```

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## CSS Units

CSS units determine the size of elements. They fall into two categories: absolute and relative.

### Absolute Units

Absolute units have a fixed size regardless of other settings.

#### Pixels (px)
Most common absolute unit for screen display.

```css
p {
    font-size: 16px;
    margin: 20px;
    padding: 10px;
}

h1 {
    font-size: 32px;
    margin-bottom: 24px;
}

img {
    width: 300px;
    height: 200px;
}
```

#### Other Absolute Units
Less commonly used but available:

```css
/* Rarely used absolute units */
p {
    margin: 0.5in;    /* inches */
    padding: 1cm;     /* centimeters */
    border: 2mm;      /* millimeters */
    width: 12pt;      /* points (1pt = 1/72 inch) */
    height: 1pc;      /* picas (1pc = 12pt) */
}
```

### Relative Units

Relative units scale based on other values, making designs more flexible.

#### Percentages (%)
Relative to the parent element's size.

```css
/* Percentage units */
section {
    width: 80%;           /* 80% of parent's width */
    margin: 0 auto;       /* Center the section */
}

article {
    width: 50%;           /* Half of parent's width */
    padding: 5%;          /* 5% of parent's width */
}

img {
    width: 100%;          /* Full width of container */
    height: auto;         /* Maintain aspect ratio */
}
```

#### Em Units (em)
Relative to the font-size of the element (or parent's font-size for other properties).

```css
/* Em units */
p {
    font-size: 1em;       /* Same as parent's font-size */
    margin: 1.5em;        /* 1.5 times the font-size */
    padding: 0.5em;       /* Half the font-size */
}

h1 {
    font-size: 2em;       /* Twice the parent's font-size */
    margin-bottom: 0.5em; /* Half of h1's font-size */
}

/* Cascading em values */
body {
    font-size: 16px;
}

article {
    font-size: 1.2em;     /* 19.2px (16px × 1.2) */
}

article p {
    font-size: 1.1em;     /* 21.12px (19.2px × 1.1) */
}
```

#### Rem Units (rem)
Relative to the root element's font-size (usually html).

```css
/* Rem units - more predictable than em */
html {
    font-size: 16px;      /* Base size */
}

p {
    font-size: 1rem;      /* 16px */
    margin: 1.5rem;       /* 24px */
}

h1 {
    font-size: 2.5rem;    /* 40px */
    margin-bottom: 1rem;  /* 16px */
}

h2 {
    font-size: 2rem;      /* 32px */
}
```

#### Viewport Units
Relative to the browser viewport size.

```css
/* Viewport units */
header {
    width: 100vw;         /* 100% of viewport width */
    height: 10vh;         /* 10% of viewport height */
}

h1 {
    font-size: 5vw;       /* 5% of viewport width */
}

section {
    min-height: 100vh;    /* Minimum full viewport height */
    padding: 5vw;         /* Responsive padding */
}

/* vmin and vmax */
article {
    width: 80vmin;        /* 80% of smaller viewport dimension */
    font-size: 2vmax;     /* 2% of larger viewport dimension */
}
```

### Choosing the Right Unit

```css
/* Best practices for different use cases */

/* Fixed sizes - use px */
img {
    border: 2px solid black;
}

/* Typography - use rem for consistency */
body {
    font-size: 1rem;
}

h1 {
    font-size: 2.5rem;
}

/* Layouts - use % or viewport units */
main {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Spacing - use em or rem */
p {
    margin-bottom: 1em;
    padding: 1rem;
}
```

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## CSS Fonts

Typography is crucial for web design. CSS provides extensive control over text appearance.

### Font Family

Specifies which font to use. Always provide fallback fonts.

```css
/* Font family with fallbacks */
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1 {
    font-family: Georgia, 'Times New Roman', serif;
}

p {
    font-family: 'Courier New', Courier, monospace;
}

/* Using quotes for font names with spaces */
article {
    font-family: 'Segoe UI', Tahoma, sans-serif;
}
```

#### Generic Font Families
Always end with a generic family as the ultimate fallback:
- **serif**: Times New Roman, Georgia (decorative strokes)
- **sans-serif**: Arial, Helvetica (no decorative strokes)
- **monospace**: Courier New, Consolas (equal character width)
- **cursive**: Comic Sans MS (handwriting style)
- **fantasy**: Impact (decorative)

### Font Size

Controls text size using any CSS unit.

```css
/* Different font size units */
p {
    font-size: 16px;      /* Absolute size */
}

h1 {
    font-size: 2.5rem;    /* Relative to root */
}

h2 {
    font-size: 2em;       /* Relative to parent */
}

/* Keyword sizes */
small {
    font-size: small;     /* Predefined size */
}

h3 {
    font-size: larger;    /* Relative keyword */
}
```

### Font Weight

Controls the thickness of characters.

```css
/* Font weight values */
p {
    font-weight: normal;  /* Same as 400 */
}

strong {
    font-weight: bold;    /* Same as 700 */
}

h1 {
    font-weight: 900;     /* Extra bold */
}

h2 {
    font-weight: 300;     /* Light */
}

/* Numeric values: 100-900 */
h3 {
    font-weight: 600;     /* Semi-bold */
}
```

### Font Style

Controls italic or oblique text.

```css
/* Font style options */
p {
    font-style: normal;
}

em {
    font-style: italic;
}

footer {
    font-style: oblique;  /* Slanted text */
}
```

### Text Decoration

Adds lines to text.

```css
/* Text decoration */
a {
    text-decoration: underline;
}

h1 {
    text-decoration: none;
}

/* Multiple decorations */
h2 {
    text-decoration: underline overline;
}

/* Decoration styles */
p {
    text-decoration: underline wavy red;
}
```

### Text Transform

Changes text capitalization.

```css
/* Text transform */
h1 {
    text-transform: uppercase;   /* ALL CAPS */
}

h2 {
    text-transform: lowercase;   /* all lowercase */
}

h3 {
    text-transform: capitalize;  /* First Letter Of Each Word */
}

p {
    text-transform: none;        /* Normal text */
}
```

### Line Height

Controls spacing between lines of text.

```css
/* Line height */
p {
    line-height: 1.5;     /* 1.5 times font size */
}

body {
    line-height: 1.6;     /* Good for readability */
}

h1 {
    line-height: 1.2;     /* Tighter for headings */
}

/* Using units */
article {
    line-height: 24px;    /* Fixed height */
}
```

### Letter Spacing and Word Spacing

Controls space between letters and words.

```css
/* Letter spacing */
h1 {
    letter-spacing: 2px;
}

p {
    letter-spacing: 0.5px;
}

/* Word spacing */
p {
    word-spacing: 5px;
}

h2 {
    word-spacing: -2px;  /* Negative brings words closer */
}
```

### Text Alignment

Controls horizontal alignment of text.

```css
/* Text alignment */
h1 {
    text-align: center;
}

p {
    text-align: left;     /* Default for LTR languages */
}

footer {
    text-align: right;
}

article {
    text-align: justify;  /* Stretches lines to full width */
}
```

### Complete Font Example

```css
/* Comprehensive font styling */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 16px;
    line-height: 1.6;
    color: #333333;
}

h1 {
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 2.5rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    text-align: center;
    color: #2c3e50;
    line-height: 1.2;
}

h2 {
    font-family: inherit;  /* Inherits from parent */
    font-size: 2rem;
    font-weight: 600;
    color: #34495e;
    margin-bottom: 1rem;
}

p {
    font-size: 1rem;
    line-height: 1.8;
    text-align: justify;
    margin-bottom: 1em;
}

em {
    font-style: italic;
    color: #e74c3c;
}

strong {
    font-weight: bold;
    color: #c0392b;
}

a {
    color: #3498db;
    text-decoration: none;
    font-weight: 500;
}

/* Hover effect for links */
a:hover {
    text-decoration: underline;
    color: #2980b9;
}
```

### Web Fonts

While not using external services, you can use system fonts creatively:

```css
/* System font stacks for different operating systems */
body {
    /* Modern system fonts */
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
                 Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 
                 'Helvetica Neue', sans-serif;
}

/* Monospace system fonts */
pre {
    font-family: 'SF Mono', Monaco, 'Cascadia Code', 
                 'Roboto Mono', Consolas, 'Courier New', 
                 monospace;
}
```

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## Vocabulary

### Color Terms
- **RGB**: Red, Green, Blue color model using values 0-255
- **RGBA**: RGB with Alpha (transparency) channel
- **HSL**: Hue, Saturation, Lightness color model
- **HSLA**: HSL with Alpha channel
- **Hexadecimal**: Base-16 number system using 0-9 and A-F
- **Alpha Channel**: Controls transparency (0 = transparent, 1 = opaque)
- **Hue**: The color itself on a 360-degree color wheel
- **Saturation**: Intensity of the color (0% = gray, 100% = vivid)
- **Lightness**: How light or dark the color is

### Unit Terms
- **Absolute Units**: Fixed measurements (px, in, cm, mm, pt, pc)
- **Relative Units**: Measurements relative to something else (%, em, rem, vw, vh)
- **Pixel (px)**: Single dot on a screen
- **Em (em)**: Relative to the element's font-size
- **Rem (rem)**: Relative to the root element's font-size
- **Viewport**: The visible area of a web page
- **Viewport Width (vw)**: 1% of viewport width
- **Viewport Height (vh)**: 1% of viewport height

### Font Terms
- **Font Family**: The typeface to use
- **Font Weight**: Thickness of characters (100-900)
- **Font Style**: Normal, italic, or oblique
- **Line Height**: Space between lines of text
- **Letter Spacing**: Space between characters
- **Word Spacing**: Space between words
- **Text Transform**: Capitalization control
- **Text Decoration**: Lines added to text (underline, overline, line-through)
- **Serif**: Fonts with decorative strokes
- **Sans-serif**: Fonts without decorative strokes
- **Monospace**: Fonts where all characters have equal width
- **Fallback Fonts**: Alternative fonts if the first choice isn't available

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## Assignments

### Assignment 1: Color Palette Creator
Create a webpage that demonstrates all color formats by building a color palette showcase.
[View Assignment 1](Assignments/Assignment (English).md)

### Assignment 2: Responsive Typography
Build a typography specimen page using various font properties and units.
[View Assignment 2](assignment2.md)

### Assignment 3: Complete Style Guide
Create a comprehensive style guide combining colors, units, and fonts.
[View Assignment 3](assignment3.md)

### Solutions
- [Assignment 1 Solution](assignment1-solution.md)
- [Assignment 2 Solution](assignment2-solution.md)
- [Assignment 3 Solution](assignment3-solution.md)

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## Summary

### Key Takeaways

1. **CSS Colors**
   - Multiple formats available: named, hex, RGB, RGBA, HSL, HSLA
   - Use RGBA/HSLA for transparency effects
   - HSL is intuitive for creating color variations
   - Always consider contrast for accessibility

2. **CSS Units**
   - Absolute units (px) for fixed sizes
   - Relative units (%, em, rem) for flexible designs
   - Viewport units (vw, vh) for responsive layouts
   - Choose units based on context and needs

3. **CSS Fonts**
   - Always provide font fallbacks
   - Use rem for consistent sizing
   - Combine properties for complete typography control
   - Consider readability with appropriate line-height

### Best Practices
- Use semantic color names in your CSS for maintainability
- Prefer rem over em for more predictable sizing
- Always include generic font families as fallbacks
- Test your designs at different screen sizes
- Maintain good contrast ratios for accessibility

[Back to Top](#css-colors-units-and-fonts---lecture-notes)

---

## Resources

### Documentation
- [MDN CSS Colors](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- [MDN CSS Units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
- [MDN CSS Fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/font)

### W3Schools References
- [W3Schools CSS Colors](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools CSS Units](https://www.w3schools.com/css/css_units.asp)
- [W3Schools CSS Fonts](https://www.w3schools.com/css/css_font.asp)

### Tools
- WebStorm IDE for code editing
- Git for version control
- GitHub for code repository

### Color Tools
- Browser DevTools color picker
- System color picker utilities

[Back to Top](#css-colors-units-and-fonts---lecture-notes)