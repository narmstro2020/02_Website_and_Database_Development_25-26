# Styling Forms and Tables with CSS

## Table of Contents

| Topic | Description |
|-------|-------------|
| [Introduction](#introduction) | Overview of forms and tables styling |
| [Vocabulary](#vocabulary) | Key terms and definitions |
| [1. Styling Tables with CSS](#1-styling-tables-with-css) | Learn to style HTML tables |
| [2. Styling Forms with CSS](#2-styling-forms-with-css) | Learn to style HTML forms |
| [Visual Examples](#visual-examples) | Complete working examples |
| [Summary](#summary) | Key takeaways |
| [Resources](#resources) | Additional learning materials |

---

## Introduction

Welcome to our lesson on styling forms and tables with CSS! Forms and tables are essential components of web development. Tables help us organize data in rows and columns, while forms allow users to input and submit information. In this lesson, we'll learn how to make these elements visually appealing and user-friendly using CSS.

### What You'll Learn:
- How to style table borders, spacing, and backgrounds
- How to create attractive and accessible forms
- Best practices for form and table design
- CSS properties specific to forms and tables

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## Vocabulary

### Table-Related Terms
- **border-collapse**: CSS property that determines whether table borders are separated or collapsed into a single border
- **border-spacing**: CSS property that sets the distance between the borders of adjacent table cells
- **caption-side**: CSS property that positions a table caption
- **thead**: HTML element that groups header content in a table
- **tbody**: HTML element that groups body content in a table
- **tfoot**: HTML element that groups footer content in a table
- **nth-child()**: CSS pseudo-class selector that matches elements based on their position

### Form-Related Terms
- **fieldset**: HTML element that groups related form controls
- **legend**: HTML element that provides a caption for a fieldset
- **placeholder**: HTML attribute that provides hint text in form inputs
- **focus**: The state when a form element is selected/active
- **:focus**: CSS pseudo-class that styles an element when it has focus
- **:hover**: CSS pseudo-class that styles an element when mouse hovers over it
- **:disabled**: CSS pseudo-class that styles disabled form elements
- **outline**: CSS property that draws a line around elements (often seen on focus)

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## 1. Styling Tables with CSS

Tables are powerful tools for displaying structured data. Let's learn how to make them beautiful and functional.

### Basic Table Structure Review

```html
<table>
    <caption>Student Grades</caption>
    <thead>
        <tr>
            <th>Name</th>
            <th>Grade</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alice</td>
            <td>A</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>B+</td>
        </tr>
    </tbody>
</table>
```

### Essential Table Styling Properties

#### 1. Border Collapse

The `border-collapse` property controls how table borders behave:

```css
/* Separate borders (default) */
table {
    border-collapse: separate;
    border-spacing: 2px;
}

/* Collapsed borders (recommended) */
table {
    border-collapse: collapse;
}
```

#### 2. Adding Borders

```css
table {
    border: 2px solid #333;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
}
```

#### 3. Styling Table Headers

```css
th {
    background-color: #4CAF50;
    color: white;
    font-weight: bold;
    text-align: left;
    padding: 12px;
}
```

#### 4. Alternating Row Colors (Zebra Stripes)

```css
/* Even rows */
tbody tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Odd rows */
tbody tr:nth-child(odd) {
    background-color: white;
}
```

#### 5. Hover Effects

```css
tbody tr:hover {
    background-color: #ddd;
    cursor: pointer;
}
```

### Complete Table Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Styled Table</title>
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
            margin: 20px 0;
            font-family: Arial, sans-serif;
        }
        
        caption {
            font-size: 1.2em;
            margin-bottom: 10px;
            font-weight: bold;
            color: #333;
        }
        
        th {
            background-color: #4CAF50;
            color: white;
            padding: 12px;
            text-align: left;
        }
        
        td {
            padding: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        tbody tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tbody tr:hover {
            background-color: #f5f5f5;
        }
    </style>
</head>
<body>
    <table>
        <caption>Product Inventory</caption>
        <thead>
            <tr>
                <th>Product</th>
                <th>Quantity</th>
                <th>Price</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Laptop</td>
                <td>15</td>
                <td>$999</td>
            </tr>
            <tr>
                <td>Mouse</td>
                <td>50</td>
                <td>$25</td>
            </tr>
            <tr>
                <td>Keyboard</td>
                <td>30</td>
                <td>$75</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Responsive Tables

For better mobile viewing:

```css
/* Container for horizontal scroll on small screens */
.table-container {
    overflow-x: auto;
}

table {
    min-width: 600px;
}
```

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## 2. Styling Forms with CSS

Forms are how users interact with your website. Good form design improves user experience and increases completion rates.

### Basic Form Structure Review

```html
<form>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Submit">
</form>
```

### Essential Form Styling Techniques

#### 1. Basic Input Styling

```css
input[type="text"],
input[type="email"],
input[type="password"],
textarea {
    width: 100%;
    padding: 10px;
    margin: 8px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
    box-sizing: border-box;
}
```

#### 2. Label Styling

```css
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}
```

#### 3. Focus States

```css
input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline: none;
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.3);
}
```

#### 4. Button Styling

```css
input[type="submit"],
button {
    background-color: #4CAF50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
}

input[type="submit"]:hover,
button:hover {
    background-color: #45a049;
}
```

#### 5. Fieldset and Legend

```css
fieldset {
    border: 2px solid #ddd;
    border-radius: 4px;
    padding: 20px;
    margin-bottom: 20px;
}

legend {
    font-weight: bold;
    color: #333;
    padding: 0 10px;
}
```

### Complete Form Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Styled Form</title>
    <style>
        * {
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        
        form {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            max-width: 500px;
            margin: 0 auto;
        }
        
        h2 {
            color: #333;
            text-align: center;
            margin-bottom: 30px;
        }
        
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
            font-weight: bold;
        }
        
        input[type="text"],
        input[type="email"],
        input[type="password"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
        }
        
        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="password"]:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: #4CAF50;
            box-shadow: 0 0 5px rgba(76, 175, 80, 0.2);
        }
        
        select {
            cursor: pointer;
        }
        
        textarea {
            resize: vertical;
            min-height: 100px;
        }
        
        input[type="checkbox"],
        input[type="radio"] {
            margin-right: 8px;
        }
        
        .checkbox-group,
        .radio-group {
            margin-bottom: 20px;
        }
        
        .checkbox-group label,
        .radio-group label {
            display: inline;
            font-weight: normal;
            margin-right: 15px;
        }
        
        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #45a049;
        }
        
        fieldset {
            border: 2px solid #ddd;
            border-radius: 4px;
            padding: 15px;
            margin-bottom: 20px;
        }
        
        legend {
            font-weight: bold;
            color: #333;
            padding: 0 10px;
        }
    </style>
</head>
<body>
    <form>
        <h2>Registration Form</h2>
        
        <fieldset>
            <legend>Personal Information</legend>
            
            <label for="firstname">First Name:</label>
            <input type="text" id="firstname" name="firstname" placeholder="Enter your first name">
            
            <label for="lastname">Last Name:</label>
            <input type="text" id="lastname" name="lastname" placeholder="Enter your last name">
            
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" placeholder="your@email.com">
        </fieldset>
        
        <fieldset>
            <legend>Account Details</legend>
            
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" placeholder="Choose a username">
            
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" placeholder="Enter a secure password">
        </fieldset>
        
        <label for="country">Country:</label>
        <select id="country" name="country">
            <option value="">Select your country</option>
            <option value="usa">United States</option>
            <option value="canada">Canada</option>
            <option value="uk">United Kingdom</option>
        </select>
        
        <label for="comments">Comments:</label>
        <textarea id="comments" name="comments" placeholder="Tell us about yourself..."></textarea>
        
        <div class="checkbox-group">
            <label>
                <input type="checkbox" name="newsletter" value="yes">
                Subscribe to newsletter
            </label>
        </div>
        
        <button type="submit">Register</button>
    </form>
</body>
</html>
```

### Form Styling Best Practices

1. **Consistency**: Use consistent spacing, colors, and sizes
2. **Clear Labels**: Always use descriptive labels for accessibility
3. **Visual Feedback**: Provide hover and focus states
4. **Error States**: Style validation messages clearly (using red borders/text)
5. **Mobile-Friendly**: Ensure forms work well on all devices
6. **Logical Grouping**: Use fieldsets to group related fields

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## Visual Examples

### Example 1: Professional Data Table

```html
<!DOCTYPE html>
<html>
<head>
    <title>Professional Table</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        .table-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        caption {
            font-size: 1.5em;
            margin-bottom: 15px;
            text-align: left;
            color: #2c3e50;
        }
        
        th {
            background-color: #3498db;
            color: white;
            padding: 15px;
            text-align: left;
            font-weight: 500;
        }
        
        td {
            padding: 12px 15px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        tbody tr:last-child td {
            border-bottom: none;
        }
        
        tbody tr:hover {
            background-color: #f8f9fa;
            transition: background-color 0.2s;
        }
        
        .status {
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.85em;
            font-weight: bold;
        }
        
        .status-active {
            background-color: #d4edda;
            color: #155724;
        }
        
        .status-pending {
            background-color: #fff3cd;
            color: #856404;
        }
    </style>
</head>
<body>
    <div class="table-container">
        <table>
            <caption>Employee Directory</caption>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Department</th>
                    <th>Email</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>John Smith</td>
                    <td>Engineering</td>
                    <td>john@company.com</td>
                    <td><span class="status status-active">Active</span></td>
                </tr>
                <tr>
                    <td>Sarah Johnson</td>
                    <td>Marketing</td>
                    <td>sarah@company.com</td>
                    <td><span class="status status-active">Active</span></td>
                </tr>
                <tr>
                    <td>Mike Davis</td>
                    <td>Sales</td>
                    <td>mike@company.com</td>
                    <td><span class="status status-pending">Pending</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

### Example 2: Contact Form with Validation Styling

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contact Form</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .form-container {
            background: white;
            border-radius: 10px;
            box-shadow: 0 14px 28px rgba(0,0,0,0.25);
            padding: 40px;
            width: 100%;
            max-width: 450px;
        }
        
        h2 {
            color: #333;
            margin-bottom: 30px;
            text-align: center;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            color: #555;
            font-weight: 500;
            margin-bottom: 8px;
        }
        
        input[type="text"],
        input[type="email"],
        textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 5px;
            font-size: 14px;
            transition: border-color 0.3s;
        }
        
        input[type="text"]:focus,
        input[type="email"]:focus,
        textarea:focus {
            outline: none;
            border-color: #667eea;
        }
        
        input:required {
            background-image: linear-gradient(to right, #fff 0%, #fff 100%);
        }
        
        input:valid {
            border-color: #4caf50;
        }
        
        input:invalid:not(:focus):not(:placeholder-shown) {
            border-color: #f44336;
        }
        
        textarea {
            resize: vertical;
            min-height: 120px;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 14px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            transition: transform 0.2s;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
        }
        
        .required {
            color: #f44336;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Contact Us</h2>
        <form>
            <div class="form-group">
                <label for="name">Name <span class="required">*</span></label>
                <input type="text" id="name" name="name" required placeholder="Your full name">
            </div>
            
            <div class="form-group">
                <label for="email">Email <span class="required">*</span></label>
                <input type="email" id="email" name="email" required placeholder="your@email.com">
            </div>
            
            <div class="form-group">
                <label for="subject">Subject</label>
                <input type="text" id="subject" name="subject" placeholder="Message subject">
            </div>
            
            <div class="form-group">
                <label for="message">Message <span class="required">*</span></label>
                <textarea id="message" name="message" required placeholder="Your message here..."></textarea>
            </div>
            
            <button type="submit" class="submit-btn">Send Message</button>
        </form>
    </div>
</body>
</html>
```

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## Summary

### Key Takeaways

#### Tables
- Use `border-collapse: collapse` for cleaner table designs
- Apply `:nth-child()` selectors for alternating row colors
- Always include proper table structure (thead, tbody, tfoot)
- Add hover effects to improve user interaction
- Use padding to create breathing room in cells

#### Forms
- Style all form states: default, hover, focus, and disabled
- Group related fields with fieldsets
- Use consistent spacing and alignment
- Provide clear visual feedback for user interactions
- Always include labels for accessibility
- Use placeholder text to guide users

### CSS Properties Learned

**Table Properties:**
- `border-collapse`
- `border-spacing`
- `caption-side`
- `:nth-child()`

**Form Properties:**
- `:focus`
- `:hover`
- `:disabled`
- `:valid` / `:invalid`
- `outline`
- `box-shadow`
- `transition`

### Best Practices Recap
1. **Accessibility First**: Always use semantic HTML and proper labels
2. **Consistent Design**: Maintain uniform spacing, colors, and typography
3. **User Feedback**: Provide clear visual states for all interactions
4. **Mobile Responsive**: Test your forms and tables on different screen sizes
5. **Performance**: Use efficient CSS selectors and minimize redundancy

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

## Resources

### Documentation
- [MDN - Styling Tables](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Styling_tables)
- [MDN - Styling Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms)
- [W3Schools - CSS Tables](https://www.w3schools.com/css/css_table.asp)
- [W3Schools - CSS Forms](https://www.w3schools.com/css/css_form.asp)

### CSS References
- [MDN - border-collapse](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
- [MDN - :nth-child()](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)
- [MDN - :focus](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [MDN - fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)

### Tools
- [WebStorm IDE](https://www.jetbrains.com/webstorm/)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

### Additional Learning
- [CSS-Tricks - A Complete Guide to Tables](https://css-tricks.com/complete-guide-table-element/)
- [CSS-Tricks - Form Styling](https://css-tricks.com/tips-for-creating-great-web-forms/)

[↑ Back to Top](#styling-forms-and-tables-with-css)

---

*End of Lecture Notes - Styling Forms and Tables with CSS*
