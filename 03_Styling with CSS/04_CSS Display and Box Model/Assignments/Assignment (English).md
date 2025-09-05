# Assignment: Box Model Spacing

## Objective
Create a card layout that demonstrates mastery of the CSS Box Model. You will build three information cards with proper spacing using margin, padding, and borders.

## Requirements
1. Create three cards displaying different types of content
2. Use padding to create internal spacing within each card
3. Use margins to separate cards from each other
4. Add borders to define card boundaries
5. Center the card container on the page
6. Make cards the same height regardless of content

## Starter HTML Structure
styles.css
```css
        /* Reset default styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            /* TODO: Add padding to body */
        }
        
        .container {
            /* TODO: Set max-width */
            /* TODO: Center container using margin */
            /* TODO: Add background color */
            /* TODO: Add padding */
        }
        
        h1 {
            /* TODO: Add margin bottom */
            /* TODO: Center text */
            /* TODO: Add color */
        }
        
        .cards {
            /* TODO: Set up container for cards */
        }
        
        .card {
            /* TODO: Set width (consider using percentages) */
            /* TODO: Add padding for internal spacing */
            /* TODO: Add margin for external spacing */
            /* TODO: Add border */
            /* TODO: Set background color */
            /* TODO: Set minimum height */
        }
        
        .card h2 {
            /* TODO: Add margin bottom */
            /* TODO: Add padding bottom */
            /* TODO: Add bottom border */
            /* TODO: Set color */
        }
        
        .card p {
            /* TODO: Add margin bottom for paragraph spacing */
            /* TODO: Set line height */
        }
        
        .card-footer {
            /* TODO: Add margin top */
            /* TODO: Add padding top */
            /* TODO: Add top border */
            /* TODO: Set text alignment */
        }
        
        .button {
            /* TODO: Remove default button styles */
            /* TODO: Add padding */
            /* TODO: Add margin */
            /* TODO: Add border */
            /* TODO: Set background color */
            /* TODO: Set text color */
            /* TODO: Add cursor pointer */
        }
        
        .button:hover {
            /* TODO: Add hover effect */
        }
        
        /* Special card styles */
        .featured {
            /* TODO: Add special styling for featured card */
            /* TODO: Consider different border or background */
        }


```

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Box Model Card Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Our Services</h1>
        
        <div class="cards">
            <div class="card">
                <h2>Web Design</h2>
                <p>Create beautiful, responsive websites that work on all devices. Our designs are modern, clean, and user-friendly.</p>
                <p>We use the latest technologies including HTML5, CSS3, and modern frameworks.</p>
                <div class="card-footer">
                    <button class="button">Learn More</button>
                </div>
            </div>
            
            <div class="card featured">
                <h2>Development</h2>
                <p>Build robust web applications with clean, maintainable code. From simple sites to complex applications.</p>
                <p>Full-stack development services with a focus on performance and security.</p>
                <p>Special offer: Get 20% off your first project!</p>
                <div class="card-footer">
                    <button class="button">Get Started</button>
                </div>
            </div>
            
            <div class="card">
                <h2>Consulting</h2>
                <p>Expert advice to help your business succeed online. We analyze your needs and provide tailored solutions.</p>
                <div class="card-footer">
                    <button class="button">Contact Us</button>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

## Tasks to Complete

### Task 1: Container Setup
1. Set a max-width for the container (suggestion: 1200px)
2. Center the container using margin auto
3. Add padding to create space inside the container

### Task 2: Card Styling
1. Add internal padding to each card (try 20px)
2. Add margins between cards (suggestion: 15px)
3. Add a border to define card edges
4. Set a minimum height so all cards are equal

### Task 3: Content Spacing
1. Add margin to headings and paragraphs
2. Create visual separation between card header and content
3. Style the card footer with borders and spacing

### Task 4: Featured Card
1. Give the featured card a different border color or style
2. Consider adding a different background color
3. Maybe increase padding or add a box shadow

### Task 5: Button Styling
1. Remove default button appearance
2. Add padding for better click area
3. Style with colors and borders
4. Add hover effects

## Expected Result
- Three evenly spaced cards in a row
- Consistent internal spacing within each card
- Clear visual hierarchy with headers, content, and footers
- Featured card stands out from others
- Buttons are styled and interactive
