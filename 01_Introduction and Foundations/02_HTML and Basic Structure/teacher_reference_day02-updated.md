# Teacher Knowledge Reference – Day 02: Introduction to HTML

---

## 1. What is HTML?

- HTML = HyperText Markup Language
- It is the standard markup language used to create web pages.
- HTML uses **tags** to mark up content and give it structure.

---

## 2. Basic Structure of an HTML Document

### Minimal Valid HTML5 Page:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
```

### Description of Tags:
- `<!DOCTYPE html>`  
  Declares the document as an HTML5 document.
- `<html>`  
  Root element that wraps the entire HTML document.
- `<head>`  
  Contains metadata about the HTML document (not shown to users).
- `<title>`  
  Title of the page that appears in the browser tab.
- `<body>`  
  All visible content is placed here (headings, paragraphs, images, etc.).

---

## 3. Important Teaching Notes

- Emphasize: **All HTML elements are wrapped in angle brackets** `< >`.
- Tags generally come in **opening** and **closing** pairs:
  - `<p>` starts a paragraph, `</p>` ends it.
- Indentation is not required but helps with **readability**.
- HTML is **not case-sensitive**, but best practice is to use lowercase.

---

## 4. Common Student Errors

- Forgetting the `<!DOCTYPE html>` at the top.
- Not properly closing tags.
- Placing content outside the `<body>` tag.
- Saving with the wrong file extension (should be `.html`).
- Not checking in a browser to confirm layout.

---

## 5. Pedagogical Tips

- Use a visual analogy: HTML is the *skeleton* of the web page.
- Model using WebStorm and have students follow along.
- Open browser next to code editor to show immediate changes.
- Walk around to help troubleshoot errors as they type.

---

## 6. Sample Questions to Ask Students

- “What part of this code do users never see?”
- “Why do you think we need the `<head>` if it doesn’t show anything?”
- “What would happen if we removed the `<body>`?”
- “Can you guess what the `<title>` does?”

---

## 7. Extension Opportunities

- Have students change the `<title>` and see it in the tab.
- Allow more advanced students to add an `<h2>` or `<p>` tag inside the `<body>`.

---

## 8. Vocabulary Words

| Term         | Definition                                               |
|--------------|----------------------------------------------------------|
| HTML         | HyperText Markup Language                                |
| Tag          | Code used to define and format content in an HTML page  |
| `<head>`     | Section for meta information like title, CSS links       |
| `<body>`     | Section that contains the visible content                |
| `<!DOCTYPE>` | Declaration for HTML5 standard compliance                |
| `<title>`    | The name shown in the browser’s tab                      |

---

## 9. Teacher Demonstration Example

Type this out in front of the class using WebStorm:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Demo Page</title>
</head>
<body>
  <h1>This is my first web page!</h1>
</body>
</html>
```
Then:
- Save as `demo.html`
- Right-click → Open in Browser
- Ask students to explain what they see and relate it to the code

---



---

## 10. Additional Teaching Strategies

### Use Visuals:
- Draw a diagram of a "web page sandwich":
  - Top layer: `<!DOCTYPE>`
  - Middle layers: `<html>`, `<head>`, `<title>`, `<body>`
  - Content inside the `<body>` like text, headings, etc.

### Incorporate Analogies:
- Think of a website as a **house**:
  - `<!DOCTYPE>` = building permit
  - `<html>` = walls/foundation
  - `<head>` = blueprint & wiring
  - `<body>` = rooms with furniture (content)
  - `<title>` = house’s name on the mailbox

---

## 11. HTML Tag Reference Table (Starter Set)

| Tag         | Purpose                                        | Example                            |
|--------------|------------------------------------------------|-------------------------------------|
| `<!DOCTYPE>` | Declares HTML version (HTML5)                  | `<!DOCTYPE html>`                   |
| `<html>`     | Root tag of the document                       | `<html> ... </html>`                |
| `<head>`     | Meta-information, not shown in the browser     | `<head> ... </head>`                |
| `<title>`    | Title in the browser tab                       | `<title>Welcome</title>`            |
| `<body>`     | Visible content                                | `<body> ... </body>`                |
| `<h1>`–`<h6>`| Headings from largest to smallest              | `<h1>Main Title</h1>`               |
| `<p>`        | Paragraphs                                     | `<p>This is a paragraph.</p>`       |

---

## 12. Common Misconceptions and Fixes

| Misconception                                    | Correction Strategy                                       |
|--------------------------------------------------|-----------------------------------------------------------|
| Thinking `<head>` means header for the page     | Explain it’s for metadata, not visible header             |
| Forgetting to save with `.html` extension       | Model saving the file, point out file extension clearly   |
| Typing tags in uppercase or forgetting closing  | Emphasize lowercase convention & tag pairs                |
| Expecting changes without refreshing browser    | Demonstrate the save → refresh cycle                     |
| Mixing `<head>` and `<body>` content            | Show valid vs invalid tag nesting on projector            |

---

## 13. Optional Practice Prompts

- Challenge: Add an `<h1>` and `<p>` inside `<body>` and personalize it.
- Bonus: Add `<em>` and `<strong>` tags for emphasis (preview upcoming content).
- Group Prompt: Label printed HTML page with pen, identifying each part and explaining its function.

---

## 14. Webstorm Tips for Teachers

- Use **File > New > HTML File** to scaffold a basic template automatically.
- Enable **Live Preview** plugin if available for real-time changes.
- Encourage students to use **right-click > Open in Browser** frequently.
- Show the difference between opening `.html` file in browser vs WebStorm preview pane.

---

## 15. Questions to Check for Understanding

- Can you explain what the `<title>` tag does?
- What will happen if we leave out `<!DOCTYPE html>`?
- Why is indentation helpful if the browser doesn’t care?
- What goes in the `<head>` vs `<body>`?

---

## 16. Suggested Exit Ticket Prompts (Alt Version)

1. Name two tags that are always required in an HTML document.
2. Where should visible content go?
3. What is the role of `<!DOCTYPE html>`?
4. What is the difference between `<head>` and `<body>`?

---

## 17. Optional Video Resources for Students

- [Intro to HTML by freeCodeCamp (YouTube, 6 min)](https://youtu.be/UB1O30fR-EE)
- [HTML Basics for Beginners (1 min preview)](https://youtu.be/pQN-pnXPaVg)

These can be used as review or independent reinforcement.

---
