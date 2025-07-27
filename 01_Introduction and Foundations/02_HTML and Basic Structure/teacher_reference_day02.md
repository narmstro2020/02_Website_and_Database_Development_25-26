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

