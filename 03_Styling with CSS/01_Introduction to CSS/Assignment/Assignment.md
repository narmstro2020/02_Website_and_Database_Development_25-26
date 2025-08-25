# Assignment 3: Multi-Page Website - Template

## Instructions
Create a 3-page website using **external CSS**. All pages should link to the same CSS file.

## Requirements Checklist
- [ ] Create three HTML files: home.html, about.html, contact.html
- [ ] Create one styles.css file
- [ ] Link all HTML pages to the same CSS file
- [ ] Include navigation links between all pages
- [ ] Style headers, paragraphs, and links consistently
- [ ] Use proper HTML structure on all pages

## File Structure
```
assignment3/
│
├── index.html
├── about.html
├── contact.html
└── styles.css
```

## HTML Templates

### index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Home - My Website</title>
    <meta charset="UTF-8">
    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Home Page</h2>
            <p>Welcome to my website! This is the home page.</p>
            <p>Add more content about what your website offers.</p>
        </section>
        
        <section>
            <h3>Featured Content</h3>
            <p>Add some interesting content here.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
```

### about.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>About - My Website</title>
    <meta charset="UTF-8">
    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>About Us</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Our Story</h2>
            <p>Tell your story here.</p>
            <p>Add information about your background.</p>
        </section>
        
        <section>
            <h3>Our Mission</h3>
            <p>Describe your mission or goals.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
```

### contact.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Contact - My Website</title>
    <meta charset="UTF-8">
    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Contact Us</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Get in Touch</h2>
            <p>We'd love to hear from you!</p>
            
            <h3>Contact Information</h3>
            <p><strong>Email:</strong> info@mywebsite.com</p>
            <p><strong>Phone:</strong> (555) 123-4567</p>
            <p><strong>Address:</strong> 123 Web Street, Internet City, WWW 12345</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
```

### styles.css (Template)
```css
/* Reset default styles */
body {
    /* Add styles for body */
}

/* Header styles */
header {
    /* Add header styles */
}

/* Heading styles */
h1 {
    /* Add h1 styles */
}

h2 {
    /* Add h2 styles */
}

h3 {
    /* Add h3 styles */
}

/* Navigation styles */
nav {
    /* Add nav styles */
}

nav ul {
    /* Add styles for navigation list */
}

nav li {
    /* Add styles for list items */
}

/* Link styles */
a {
    /* Add link styles */
}

a:hover {
    /* Add hover effect for links */
}

/* Main content styles */
main {
    /* Add main styles */
}

/* Section styles */
section {
    /* Add section styles */
}

/* Paragraph styles */
p {
    /* Add paragraph styles */
}

/* Footer styles */
footer {
    /* Add footer styles */
}
```

## CSS Properties to Consider
- Background colors and text colors
- Font families and sizes
- Padding and margins
- Text alignment
- Borders
- Display properties for navigation
- Hover effects for links

## Tips
1. Keep your CSS organized with comments
2. Test all navigation links
3. Make sure the CSS file path is correct in all HTML files
4. Use consistent spacing and colors across all pages
5. Consider adding a hover effect to navigation links

## Submission Instructions
1. Create a folder called `assignment3`
2. Place all four files in this folder
3. Test all pages and navigation in your browser
4. Commit to Git with message: "Complete Assignment 3: Multi-Page Website with External CSS"
5. Push to GitHub
