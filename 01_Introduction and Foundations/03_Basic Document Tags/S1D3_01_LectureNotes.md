# 👩‍🏫 Lecture Notes – Day 03: HTML Text Elements

---

## 🎯 Objective

By the end of this lesson, students will be able to write and explain the purpose of the following HTML text elements:

- Headings: `<h1>` to `<h6>`
- Paragraphs: `<p>`
- Emphasis: `<strong>`, `<em>`
- Line breaks: `<br>`

---

## 🧱 1. HTML Headings

HTML has six levels of headings, from most important (`<h1>`) to least important (`<h6>`).

### Example:
```html
<h1>This is a Heading 1</h1>
<h2>This is a Heading 2</h2>
<h3>This is a Heading 3</h3>
<h4>This is a Heading 4</h4>
<h5>This is a Heading 5</h5>
<h6>This is a Heading 6</h6>
```

### Notes:
- Headings help **organize content**.
- `<h1>` should be used once per page for the main heading.

---

## 📄 2. Paragraphs

Use `<p>` to define blocks of text content.

### Example:
```html
<p>This is a paragraph of text. It will be displayed as a block with space above and below it.</p>
```

---

## 💪 3. Emphasis and Importance

Use `<strong>` for **importance** (usually bold)  
Use `<em>` for *emphasis* (usually italic)

### Example:
```html
<p>Learning to code is <strong>very important</strong>.</p>
<p>You should <em>always</em> test your code.</p>
```

You can **nest** them:
```html
<p>This is <strong>really <em>important</em></strong>.</p>
```

---

## 🔁 4. Line Breaks

Use `<br>` to insert a line break without starting a new paragraph.

### Example:
```html
<p>Roses are red,<br>
Violets are blue,<br>
HTML is fun,<br>
And so are you!</p>
```

---

## 🧪 5. Full Practice Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Text Elements</title>
</head>
<body>

  <h1>Welcome to My Web Page</h1>
  <h2>About Me</h2>
  <p>Hello! My name is Sam and I love <strong>coding</strong> and <em>designing</em> websites.</p>

  <h3>Favorite Quote:</h3>
  <p>
    Stay hungry,<br>
    Stay foolish.
  </p>

  <h4>Hobbies</h4>
  <p>I enjoy biking, painting, and gaming.</p>

</body>
</html>
```

---

## 🧠 Comprehension Questions

1. What tag do you use for the largest heading?
2. What’s the difference between `<br>` and `<p>`?
3. Which tag should you use for strong importance?
4. How many `<h1>` tags should be on a page?

---

## 🧰 Tips for Students

- Use **WebStorm** to type and test each tag.
- Don’t forget closing tags like `</p>`, `</strong>`, and `</em>`.
- Use indentation and spacing to keep your code readable.
- Save your file as `yourname_day03.html` and open in a browser to test.

---

## 📚 Vocabulary Recap

| Tag         | Description                          |
|-------------|--------------------------------------|
| `<h1>`–`<h6>` | Headings (levels 1 to 6)             |
| `<p>`       | Paragraph                            |
| `<strong>`  | Bold/Important text                  |
| `<em>`      | Italic/Emphasized text               |
| `<br>`      | Line break (no closing tag required) |

---

