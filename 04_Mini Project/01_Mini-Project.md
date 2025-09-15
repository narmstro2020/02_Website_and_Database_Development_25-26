# Multi-Page Website Project with HTML & CSS

## Project Overview
Create a professionally styled multi-page website about a topic you're passionate about. This could be a hobby, favorite subject, sport, game, book series, movie franchise, music genre, or any appropriate topic that interests you. Your website will demonstrate your understanding of HTML structure, semantic elements, CSS styling, and multi-page navigation.

**Duration:** 7 class periods (86 minutes each)  
**Tools:** WebStorm, Git, GitHub

## Project Requirements

### Technical Requirements

#### 1. **Website Structure** (Minimum 5 pages)
- index.html (Home page)
- At least 4 additional pages
- styles.css (External stylesheet linked to all pages)
- All pages must be properly linked together with navigation

#### 2. **Required HTML Elements**
Each element type must appear at least once across your website:

**Document Structure:**
- Proper DOCTYPE declaration
- html, head, and body tags
- Meaningful title tags (different for each page)
- Link to external CSS file

**Semantic Structure:**
- header (site header with navigation)
- main (main content area)
- footer (site footer)
- section (content sections)
- article (at least 2 articles)

**Content Elements:**
- All heading levels used appropriately (h1 through h6)
- Multiple paragraphs (p)
- Emphasis (em) and strong emphasis (strong)
- Line breaks (br) where appropriate

**Lists:**
- At least one unordered list (ul)
- At least one ordered list (ol)
- Proper list items (li)

**Links and Navigation:**
- Navigation menu linking all pages
- At least 3 external links (using target="_blank")
- Proper use of relative paths for internal links

**Images:**
- Minimum 5 images across the site
- All images must have:
  - Proper src attributes
  - Descriptive alt text
  - title attributes
  - width and height attributes

#### 3. **Required CSS Styling**
Your styles.css file must demonstrate:

**Selectors:**
- Element selectors (at least 5 different elements)
- Class selectors (at least 5 different classes)
- ID selectors (at least 2 different IDs)

**Text & Font Properties:**
- font-family (with font stack)
- font-size
- font-weight
- text-align
- text-decoration
- color

**Box Model Properties:**
- margin
- padding
- border (with different styles)
- width and/or height

**Background Properties:**
- background-color
- background-image (at least once)


**Visual Design:**
- Consistent color scheme (3-5 colors)
- Consistent typography
- Styled navigation menu
- Hover effects on links

#### 4. **File Organization**
- Create an "images" folder for all image files
- Create a "css" folder for your stylesheet
- Use clear, descriptive file names (no spaces, lowercase)
- Organize any sub-pages in logical folders if needed

#### 5. **Version Control**
- Initialize Git repository on Day 1
- Make meaningful commits after each work session (minimum 7 commits)
- Push to GitHub repository
- Write clear commit messages

## Daily Schedule

### Day 1: Planning & Setup (86 minutes)
- Choose your topic and color scheme
- Plan your 5+ pages and content outline
- Create project folder structure
- Initialize Git repository and GitHub repository
- Create index.html with basic structure
- Create css/styles.css file
- Link CSS to HTML
- Add basic CSS reset/setup
- Initial commit and push

### Day 2: Homepage Structure & Basic Styles (86 minutes)
- Complete index.html structure
- Add header with site title
- Create navigation menu structure
- Add main content sections
- Begin CSS styling:
  - Set up color variables/scheme
  - Style body, headers, and basic typography
  - Create navigation styling
- Commit and push changes

### Day 3: Homepage Completion & Second Page (86 minutes)
- Finish homepage styling
- Add images with CSS styling
- Create second page with consistent header/nav
- Apply CSS classes and IDs
- Style specific components
- Commit and push changes

### Day 4: Third & Fourth Pages (86 minutes)
- Create two additional pages
- Ensure consistent styling across pages
- Add unique content requiring different CSS
- Implement hover effects
- Style lists and articles
- Commit and push changes

### Day 5: Final Page & Advanced Styling (86 minutes)
- Create final required page
- Implement background images
- Add border styles and box model refinements
- Create special styling for specific sections
- Ensure all required CSS properties are used
- Commit and push changes

### Day 6: Polish & Enhancement (86 minutes)
- Review all pages for consistency
- Refine color scheme and typography
- Add finishing touches to CSS
- Optimize images if needed
- Test all links and navigation
- Validate HTML and CSS
- Commit and push changes

### Day 7: Final Review & Submission (86 minutes)
- Final testing of entire site
- Check all required elements are present
- Ensure GitHub repository is complete
- Complete self-assessment checklist
- Prepare for presentation (optional)
- Final commit and push
- Submit GitHub repository link

## Grading Rubric (100 points) (Assessments Category) 

### HTML Structure & Syntax (20 points)
- **Exemplary (19-20):** Perfect HTML syntax, all required tags present and properly nested, meaningful semantic structure
- **Proficient (15-18):** Good HTML syntax with minor errors, most required tags present, good semantic structure
- **Developing (11-14):** Some HTML errors, missing some required tags, inconsistent structure
- **Beginning (0-10):** Many HTML errors, missing many required tags, poor structure

### CSS Implementation (25 points)
- **Exemplary (23-25):** All required CSS properties used effectively, clean and organized stylesheet, creative styling choices
- **Proficient (18-22):** Most required CSS properties present, good organization, effective styling
- **Developing (13-17):** Some required CSS missing, basic styling, some organization issues
- **Beginning (0-12):** Many required CSS properties missing, poor organization, minimal styling

### Visual Design & Consistency (15 points)
- **Exemplary (14-15):** Professional appearance, consistent design throughout, excellent color scheme and typography
- **Proficient (11-13):** Good visual design, mostly consistent, good color choices
- **Developing (8-10):** Basic design, some inconsistencies, adequate color scheme
- **Beginning (0-7):** Poor visual design, many inconsistencies, poor color choices

### Content & Organization (15 points)
- **Exemplary (14-15):** Rich, well-organized content, clear topic focus, excellent information architecture
- **Proficient (11-13):** Good content, mostly organized, clear topic
- **Developing (8-10):** Adequate content, some organization issues
- **Beginning (0-7):** Minimal content, poor organization

### Navigation & Links (10 points)
- **Exemplary (10):** All navigation works perfectly, well-styled menu, all links functional
- **Proficient (8-9):** Most navigation works, good styling, minor issues
- **Developing (6-7):** Some broken links, basic navigation styling
- **Beginning (0-5):** Many broken links, poor or unstyled navigation

### Technical Requirements (10 points)
- **Exemplary (10):** All images load with proper attributes, file structure perfect, CSS properly linked
- **Proficient (8-9):** Most technical requirements met, minor issues
- **Developing (6-7):** Some technical issues, basic requirements met
- **Beginning (0-5):** Many technical problems

### Git & GitHub Usage (5 points)
- **Exemplary (5):** 7+ meaningful commits with clear messages
- **Proficient (4):** 5-6 commits with decent messages
- **Developing (3):** 3-4 commits
- **Beginning (0-2):** Fewer than 3 commits

## Submission Requirements
1. GitHub repository link
2. All files properly uploaded to GitHub
3. Repository must be public or shared with instructor
4. CSS file must be external (not inline or internal styles)

## CSS Examples to Consider
```css
/* Example: Navigation styling */
nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline-block;
    margin: 0 10px;
}

nav a:hover {
    color: #yourcolor;
    text-decoration: underline;
}

/* Example: Using classes and IDs */
.highlight {
    background-color: yellow;
    padding: 5px;
}

#main-header {
    background-color: #333;
    color: white;
    padding: 20px;
}
```

## Tips for Success
- Plan your design and color scheme before coding
- Use a CSS reset or normalize for consistency
- Keep your CSS organized with comments
- Test your site in different browsers
- Use the browser developer tools to debug CSS
- Make regular commits to track progress
- Validate your HTML and CSS

## Resources
- W3Schools CSS Reference: https://www.w3schools.com/css/
- MDN CSS Documentation: https://developer.mozilla.org/en-US/docs/Web/CSS
- HTML Validator: https://validator.w3.org/
- CSS Validator: https://jigsaw.w3.org/css-validator/
- Color Palette Generator: https://coolors.co/

## Academic Integrity
This is an individual project. While you may discuss ideas with classmates, all code must be your own. Copying code from other students or sources without attribution is plagiarism.

---

**Note:** No JavaScript should be used in this project. Focus on creating well-structured HTML with professional CSS styling.
