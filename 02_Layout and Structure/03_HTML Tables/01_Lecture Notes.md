# HTML Tables - Lecture Notes

## Table of Contents

| Topic | Description |
|-------|------------|
| [Introduction](#introduction) | Overview of HTML tables and their purpose |
| [Vocabulary](#vocabulary) | Key terms and definitions |
| [Basic Table Structure](#basic-table-structure) | Core table elements |
| [Table Headers and Data](#table-headers-and-data) | Working with headers and data cells |
| [Table Sections](#table-sections) | Organizing tables with thead, tbody, tfoot |
| [Spanning Cells](#spanning-cells) | Creating cells that span multiple rows or columns |
| [Table Styling Attributes](#table-styling-attributes) | Basic table presentation |
| [Table Accessibility](#table-accessibility) | Making tables accessible |
| [Nested Tables](#nested-tables) | Tables within tables |
| [Visual Examples](#visual-examples) | Complete table examples |
| [Additional Resources](#additional-resources) | Documentation and learning resources |
| [Summary](#summary) | Key takeaways |

---

## Introduction
[Back to Top](#table-of-contents)

HTML tables are used to display data in a structured, grid-like format with rows and columns. Just like how we use tables in everyday life (like schedules, price lists, or sports scores), HTML tables help us organize and present information clearly on web pages.

### When to Use Tables
- Displaying tabular data (schedules, statistics, comparisons)
- Creating structured layouts for data
- Presenting information that has relationships between rows and columns

### When NOT to Use Tables
- For page layout (use CSS instead)
- For non-tabular content
- When a list would be more appropriate

---

## Vocabulary
[Back to Top](#table-of-contents)

| Term | Definition | Example |
|------|------------|---------|
| **Table** | A structured set of data made up of rows and columns | `<table>` |
| **Row** | A horizontal line of cells in a table | `<tr>` |
| **Cell** | An individual unit of data in a table | `<td>` or `<th>` |
| **Header Cell** | A cell that contains header information | `<th>` |
| **Data Cell** | A cell that contains data | `<td>` |
| **Caption** | A title or description for the table | `<caption>` |
| **Column** | A vertical line of cells in a table | No specific tag |
| **Border** | The line around table cells | `border` attribute |
| **Colspan** | Number of columns a cell should span | `colspan="2"` |
| **Rowspan** | Number of rows a cell should span | `rowspan="2"` |

---

## Basic Table Structure
[Back to Top](#table-of-contents)

### The Essential Elements

Every HTML table starts with the `<table>` tag and contains rows (`<tr>`) which contain cells (`<td>` or `<th>`).

```html
<!DOCTYPE html>
<html>
<head>
    <title>Basic Table</title>
</head>
<body>
    <h1>My First Table</h1>
    
    <table>
        <tr>
            <td>Row 1, Cell 1</td>
            <td>Row 1, Cell 2</td>
        </tr>
        <tr>
            <td>Row 2, Cell 1</td>
            <td>Row 2, Cell 2</td>
        </tr>
    </table>
</body>
</html>
```

### Table Structure Hierarchy

```
<table>                  <!-- Container for the entire table -->
    <tr>                 <!-- Table Row -->
        <td>...</td>     <!-- Table Data cell -->
        <td>...</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
    </tr>
</table>
```

### Adding a Border

To make the table structure visible, we can add a border attribute:

```html
<table border="1">
    <tr>
        <td>Cell with border</td>
        <td>Another cell</td>
    </tr>
</table>
```

---

## Table Headers and Data
[Back to Top](#table-of-contents)

### Using Header Cells (`<th>`)

Header cells are used to describe the data in a column or row. By default, text in `<th>` elements is bold and centered.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Table with Headers</title>
</head>
<body>
    <h1>Student Grades</h1>
    
    <table border="1">
        <tr>
            <th>Student Name</th>
            <th>Math</th>
            <th>Science</th>
        </tr>
        <tr>
            <td>Alice</td>
            <td>95</td>
            <td>88</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>87</td>
            <td>92</td>
        </tr>
    </table>
</body>
</html>
```

### Row Headers

Headers can also be used for rows:

```html
<table border="1">
    <tr>
        <th>Monday</th>
        <td>Math</td>
        <td>English</td>
    </tr>
    <tr>
        <th>Tuesday</th>
        <td>Science</td>
        <td>History</td>
    </tr>
</table>
```

---

## Table Sections
[Back to Top](#table-of-contents)

Tables can be divided into three semantic sections:
- `<thead>` - Table header section
- `<tbody>` - Table body section  
- `<tfoot>` - Table footer section

### Complete Example with Sections

```html
<!DOCTYPE html>
<html>
<head>
    <title>Table Sections</title>
</head>
<body>
    <h1>Sales Report</h1>
    
    <table border="1">
        <caption>Quarterly Sales Data</caption>
        
        <thead>
            <tr>
                <th>Product</th>
                <th>Q1</th>
                <th>Q2</th>
                <th>Q3</th>
                <th>Q4</th>
            </tr>
        </thead>
        
        <tbody>
            <tr>
                <td>Laptops</td>
                <td>120</td>
                <td>135</td>
                <td>155</td>
                <td>180</td>
            </tr>
            <tr>
                <td>Tablets</td>
                <td>80</td>
                <td>85</td>
                <td>95</td>
                <td>110</td>
            </tr>
            <tr>
                <td>Phones</td>
                <td>200</td>
                <td>210</td>
                <td>225</td>
                <td>250</td>
            </tr>
        </tbody>
        
        <tfoot>
            <tr>
                <th>Total</th>
                <td>400</td>
                <td>430</td>
                <td>475</td>
                <td>540</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```

### Benefits of Using Sections
- Better semantic structure
- Easier to style with CSS
- Screen readers can better interpret the table
- The browser can print table headers and footers on each page

---

## Spanning Cells
[Back to Top](#table-of-contents)

### Column Spanning (`colspan`)

Makes a cell span across multiple columns:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Column Spanning</title>
</head>
<body>
    <h1>Schedule</h1>
    
    <table border="1">
        <tr>
            <th>Time</th>
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
        </tr>
        <tr>
            <td>9:00 AM</td>
            <td colspan="3">Team Meeting (All Days)</td>
        </tr>
        <tr>
            <td>10:00 AM</td>
            <td>Math</td>
            <td>Science</td>
            <td>English</td>
        </tr>
    </table>
</body>
</html>
```

### Row Spanning (`rowspan`)

Makes a cell span across multiple rows:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Row Spanning</title>
</head>
<body>
    <h1>Course Schedule</h1>
    
    <table border="1">
        <tr>
            <th>Day</th>
            <th>Morning</th>
            <th>Afternoon</th>
        </tr>
        <tr>
            <td rowspan="2">Monday</td>
            <td>HTML Basics</td>
            <td>CSS Introduction</td>
        </tr>
        <tr>
            <td>HTML Tables</td>
            <td>CSS Selectors</td>
        </tr>
        <tr>
            <td>Tuesday</td>
            <td>JavaScript Basics</td>
            <td>Practice Lab</td>
        </tr>
    </table>
</body>
</html>
```

### Complex Spanning Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Complex Table</title>
</head>
<body>
    <h1>Class Timetable</h1>
    
    <table border="1">
        <tr>
            <th rowspan="2">Day</th>
            <th colspan="2">Morning Sessions</th>
            <th colspan="2">Afternoon Sessions</th>
        </tr>
        <tr>
            <th>9:00-10:30</th>
            <th>10:30-12:00</th>
            <th>1:00-2:30</th>
            <th>2:30-4:00</th>
        </tr>
        <tr>
            <td>Monday</td>
            <td>HTML</td>
            <td>CSS</td>
            <td colspan="2">Lab Practice</td>
        </tr>
        <tr>
            <td>Tuesday</td>
            <td colspan="2">JavaScript Workshop</td>
            <td>Git</td>
            <td>GitHub</td>
        </tr>
    </table>
</body>
</html>
```

---

## Table Styling Attributes
[Back to Top](#table-of-contents)

### Basic Attributes

While CSS is preferred for styling, HTML provides some basic attributes:

```html
<table border="1" width="500" cellpadding="10" cellspacing="5">
    <tr>
        <th width="200">Name</th>
        <th>Score</th>
    </tr>
    <tr>
        <td align="center">John</td>
        <td align="right">95</td>
    </tr>
</table>
```

### Common Attributes

| Attribute | Purpose | Example |
|-----------|---------|---------|
| `border` | Sets table border width | `border="1"` |
| `width` | Sets table width | `width="500"` or `width="100%"` |
| `cellpadding` | Space inside cells | `cellpadding="10"` |
| `cellspacing` | Space between cells | `cellspacing="5"` |
| `align` | Horizontal alignment | `align="left/center/right"` |
| `valign` | Vertical alignment | `valign="top/middle/bottom"` |

---

## Table Accessibility
[Back to Top](#table-of-contents)

### Using Caption

The `<caption>` element provides a title for the table:

```html
<table border="1">
    <caption>Monthly Expenses for 2024</caption>
    <tr>
        <th>Month</th>
        <th>Rent</th>
        <th>Food</th>
    </tr>
    <tr>
        <td>January</td>
        <td>$1000</td>
        <td>$400</td>
    </tr>
</table>
```

### Scope Attribute

The `scope` attribute helps screen readers understand header relationships:

```html
<table border="1">
    <tr>
        <th scope="col">Product</th>
        <th scope="col">Price</th>
    </tr>
    <tr>
        <th scope="row">Laptop</th>
        <td>$999</td>
    </tr>
    <tr>
        <th scope="row">Mouse</th>
        <td>$25</td>
    </tr>
</table>
```

---

## Nested Tables
[Back to Top](#table-of-contents)

Tables can contain other tables, though this should be used sparingly:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Nested Tables</title>
</head>
<body>
    <h1>Department Structure</h1>
    
    <table border="1">
        <tr>
            <th>Department</th>
            <th>Teams</th>
        </tr>
        <tr>
            <td>Engineering</td>
            <td>
                <table border="1">
                    <tr>
                        <td>Frontend</td>
                        <td>5 members</td>
                    </tr>
                    <tr>
                        <td>Backend</td>
                        <td>7 members</td>
                    </tr>
                </table>
            </td>
        </tr>
        <tr>
            <td>Marketing</td>
            <td>
                <table border="1">
                    <tr>
                        <td>Digital</td>
                        <td>3 members</td>
                    </tr>
                    <tr>
                        <td>Print</td>
                        <td>2 members</td>
                    </tr>
                </table>
            </td>
        </tr>
    </table>
</body>
</html>
```

---

## Visual Examples
[Back to Top](#table-of-contents)

### Example 1: Simple Product Catalog

```html
<!DOCTYPE html>
<html>
<head>
    <title>Product Catalog</title>
</head>
<body>
    <h1>Our Products</h1>
    
    <table border="1" width="600" cellpadding="5">
        <caption>Available Items</caption>
        <thead>
            <tr>
                <th>Product ID</th>
                <th>Name</th>
                <th>Category</th>
                <th>Price</th>
                <th>In Stock</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>001</td>
                <td>Laptop Pro</td>
                <td>Electronics</td>
                <td>$1,299</td>
                <td>Yes</td>
            </tr>
            <tr>
                <td>002</td>
                <td>Wireless Mouse</td>
                <td>Accessories</td>
                <td>$29</td>
                <td>Yes</td>
            </tr>
            <tr>
                <td>003</td>
                <td>USB-C Cable</td>
                <td>Accessories</td>
                <td>$15</td>
                <td>No</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Example 2: Sports League Table

```html
<!DOCTYPE html>
<html>
<head>
    <title>League Standings</title>
</head>
<body>
    <h1>Soccer League Standings</h1>
    
    <table border="1" cellpadding="8">
        <caption>Season 2024 Rankings</caption>
        <thead>
            <tr>
                <th>Position</th>
                <th>Team</th>
                <th>Played</th>
                <th>Won</th>
                <th>Drew</th>
                <th>Lost</th>
                <th>Points</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td align="center">1</td>
                <td><strong>Eagles FC</strong></td>
                <td align="center">10</td>
                <td align="center">8</td>
                <td align="center">1</td>
                <td align="center">1</td>
                <td align="center"><strong>25</strong></td>
            </tr>
            <tr>
                <td align="center">2</td>
                <td>Lions United</td>
                <td align="center">10</td>
                <td align="center">7</td>
                <td align="center">2</td>
                <td align="center">1</td>
                <td align="center">23</td>
            </tr>
            <tr>
                <td align="center">3</td>
                <td>Thunder SC</td>
                <td align="center">10</td>
                <td align="center">6</td>
                <td align="center">3</td>
                <td align="center">1</td>
                <td align="center">21</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="7" align="center">
                    <em>Last updated: Today</em>
                </td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```

### Example 3: Restaurant Menu

```html
<!DOCTYPE html>
<html>
<head>
    <title>Restaurant Menu</title>
</head>
<body>
    <h1>Café Menu</h1>
    
    <table border="1" width="500" cellpadding="10">
        <caption>Today's Specials</caption>
        <thead>
            <tr>
                <th colspan="3">Breakfast Menu (7 AM - 11 AM)</th>
            </tr>
            <tr>
                <th>Item</th>
                <th>Description</th>
                <th>Price</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Pancakes</td>
                <td>Stack of 3 with syrup</td>
                <td>$8.99</td>
            </tr>
            <tr>
                <td>Omelet</td>
                <td>3 eggs with cheese and veggies</td>
                <td>$10.99</td>
            </tr>
            <tr>
                <td>French Toast</td>
                <td>With powdered sugar</td>
                <td>$7.99</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="3" align="center">
                    All items include coffee or juice
                </td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```

---

## Additional Resources
[Back to Top](#table-of-contents)

### Official Documentation
- [MDN Web Docs - HTML Tables](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables)
- [MDN - `<table>` Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
- [MDN - `<tr>` Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr)
- [MDN - `<td>` Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td)
- [MDN - `<th>` Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th)

### W3Schools Tutorials
- [W3Schools - HTML Tables](https://www.w3schools.com/html/html_tables.asp)
- [W3Schools - Table Headers](https://www.w3schools.com/tags/tag_th.asp)
- [W3Schools - Table Borders](https://www.w3schools.com/html/html_table_borders.asp)
- [W3Schools - Table Sizes](https://www.w3schools.com/html/html_table_sizes.asp)
- [W3Schools - Colspan & Rowspan](https://www.w3schools.com/html/html_table_colspan_rowspan.asp)

### WebStorm Tips
- Use code completion by typing `<table` and pressing Tab
- Format your HTML with Ctrl+Alt+L (Windows) or Cmd+Option+L (Mac)
- Use Live Edit to see changes in real-time

### Git Commands for Your Project
```bash
# Initialize repository
git init

# Add your table files
git add index.html

# Commit your work
git commit -m "Add HTML table exercises"

# Push to GitHub
git push origin main
```

---

## Summary
[Back to Top](#table-of-contents)

### Key Concepts Learned

1. **Table Structure**
   - Tables are created with `<table>` element
   - Tables contain rows (`<tr>`) which contain cells (`<td>` or `<th>`)
   - Always close your tags properly

2. **Table Elements**
   - `<table>` - Container for the entire table
   - `<tr>` - Table row
   - `<td>` - Table data cell
   - `<th>` - Table header cell (bold and centered by default)
   - `<caption>` - Table title/description

3. **Table Sections**
   - `<thead>` - Groups header content
   - `<tbody>` - Groups body content
   - `<tfoot>` - Groups footer content

4. **Spanning Cells**
   - `colspan` - Cell spans multiple columns
   - `rowspan` - Cell spans multiple rows

5. **Basic Styling Attributes**
   - `border` - Adds borders to table
   - `width` - Sets table/cell width
   - `cellpadding` - Space inside cells
   - `cellspacing` - Space between cells
   - `align` - Horizontal alignment
   - `valign` - Vertical alignment

### Best Practices
- Use tables only for tabular data
- Include table headers for better understanding
- Add captions to describe table content
- Use semantic sections (thead, tbody, tfoot)
- Consider accessibility with scope attributes
- Keep tables simple and readable

### Common Mistakes to Avoid
- Using tables for page layout (use CSS instead)
- Forgetting to close tags
- Incorrect colspan/rowspan values
- Missing table headers
- Not considering mobile responsiveness

### Next Steps
- Practice creating different types of tables
- Learn CSS to style tables more effectively
- Explore responsive table designs
- Study table accessibility guidelines

---

**Remember:** Tables are powerful tools for organizing data. Master the basics first, then explore more advanced features as needed. Always test your tables in different browsers and consider how they'll look on different screen sizes!

[Back to Top](#table-of-contents)