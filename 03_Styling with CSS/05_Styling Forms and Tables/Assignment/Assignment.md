# Assignment 1: Style a Product Table

## Objective
Style a table displaying at least 5 products with professional styling.

## Requirements
- [ ] Use alternating row colors (zebra stripes)
- [ ] Add hover effects to table rows
- [ ] Style the header with a distinct background color
- [ ] Include a descriptive table caption
- [ ] Use collapsed borders
- [ ] Add appropriate padding to all cells
- [ ] Make the table responsive and visually appealing

## Starter Code

### styles.css 

```css
/* Reset and base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* Add your body styles here */
}

/* Table styles */
table {
    /* Add your table styles here */
}

caption {
    /* Style the table caption */
}

/* Header styles */
thead {
    /* Add thead styles if needed */
}

th {
    /* Style the table headers */
}

/* Body styles */
tbody {
    /* Add tbody styles if needed */
}

td {
    /* Style the table cells */
}

/* Zebra stripes - alternating row colors */
/* Add your nth-child selectors here */

/* Hover effect */
/* Add your hover styles here */
```
### index.html already built

```html
<!DOCTYPE html>
<html>
<head>
    <title>Product Inventory Table</title>
    <style>

        
    </style>
</head>
<body>
    <div class="table-wrapper">
        <table>
            <caption>Product Inventory - Electronics Store</caption>
            <thead>
                <tr>
                    <th>Product Name</th>
                    <th>Category</th>
                    <th>Price</th>
                    <th>Stock Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>MacBook Pro 14"</td>
                    <td>Laptops</td>
                    <td>$1,999.00</td>
                    <td><span class="stock-status in-stock">In Stock</span></td>
                </tr>
                <tr>
                    <td>iPhone 15 Pro</td>
                    <td>Smartphones</td>
                    <td>$999.00</td>
                    <td><span class="stock-status in-stock">In Stock</span></td>
                </tr>
                <tr>
                    <td>iPad Air</td>
                    <td>Tablets</td>
                    <td>$599.00</td>
                    <td><span class="stock-status low-stock">Low Stock</span></td>
                </tr>
                <tr>
                    <td>AirPods Pro</td>
                    <td>Audio</td>
                    <td>$249.00</td>
                    <td><span class="stock-status in-stock">In Stock</span></td>
                </tr>
                <tr>
                    <td>Apple Watch Series 9</td>
                    <td>Wearables</td>
                    <td>$399.00</td>
                    <td><span class="stock-status out-of-stock">Out of Stock</span></td>
                </tr>
                <tr>
                    <td>Magic Keyboard</td>
                    <td>Accessories</td>
                    <td>$299.00</td>
                    <td><span class="stock-status in-stock">In Stock</span></td>
                </tr>
                <tr>
                    <td>Studio Display</td>
                    <td>Monitors</td>
                    <td>$1,599.00</td>
                    <td><span class="stock-status low-stock">Low Stock</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

## Hints
1. Use `border-collapse: collapse` on the table for cleaner borders
2. Consider using colors that match a consistent color scheme
3. For zebra stripes, use `tbody tr:nth-child(even)` and `tbody tr:nth-child(odd)`
4. Add a subtle transition for the hover effect to make it smooth
5. Consider adding different colors or badges for stock status (In Stock, Low Stock, Out of Stock)

## Bonus Challenges
- Add a tfoot section with totals
- Style the stock status with colored badges
- Make the price column right-aligned
- Add a subtle box-shadow to the table

## Submission
Save your file as `product-table.html` and test it in your browser. Make sure all requirements are met before submitting via GitHub.