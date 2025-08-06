# 👩‍🏫 Lecture Notes – Day 05: HTML Lists and Links

---

## 🎯 Objective

By the end of this lesson, students will be able to:
- Create unordered and ordered lists with `<ul>`, `<ol>`, and `<li>`
- Link to external websites using `<a href="">`
- Create internal anchor links within the same page

---

## 🧱 1. HTML Lists

### 📝 Unordered List (`<ul>`)
Displays a bulleted list of items.

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

### 🔢 Ordered List (`<ol>`)
Displays a numbered list of items.

```html
<ol>
  <li>Wake up</li>
  <li>Eat breakfast</li>
  <li>Go to school</li>
</ol>
```

### 🧩 List Items (`<li>`)
Must always be nested inside `<ul>` or `<ol>`. Each list item represents a single point.

---

## 🔗 2. HTML Links

### 🌐 External Link
Links to a different website using the `href` attribute.

```html
<a href="https://www.google.com">Visit Google</a>
```

### 📄 Internal Link (to another page)
Links to a different HTML file in the same folder.

```html
<a href="about.html">About Me</a>
```

### 🔁 Anchor Link (jump within the same page)

1. Set an **ID** on the element you want to jump to:

```html
<h2 id="contact">Contact Info</h2>
```

2. Create a link that jumps to that ID:

```html
<a href="#contact">Go to Contact Info</a>
```

---

## 🧪 Full Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Lists and Links</title>
</head>
<body>

  <h1>My Favorite Foods</h1>

  <ul>
    <li>Pizza</li>
    <li>Tacos</li>
    <li>Sushi</li>
  </ul>

  <h2>My Daily Routine</h2>

  <ol>
    <li>Wake up</li>
    <li>Brush teeth</li>
    <li>Go to school</li>
  </ol>

  <p>Click here to visit <a href="https://www.wikipedia.org">Wikipedia</a>.</p>

  <p><a href="#bottom">Jump to the bottom of the page</a></p>

  <h2 id="bottom">Bottom of the Page</h2>
  <p>This is the end of the content.</p>
  <p><a href="#">Back to Top</a></p>

</body>
</html>
```

---

## ❓ Questions to Ask Students

1. What is the difference between `<ul>` and `<ol>`?
2. What tag goes inside a list to define the actual item?
3. What does `href` stand for?
4. How can you link to a specific part of the same page?

---

## 💬 Vocabulary

| Tag        | Description                           |
|------------|---------------------------------------|
| `<ul>`     | Unordered list (bullets)              |
| `<ol>`     | Ordered list (numbers)                |
| `<li>`     | List item                             |
| `<a>`      | Anchor tag for hyperlinks             |
| `href`     | Hyperlink reference attribute         |
| `id`       | Unique identifier used with anchors   |

---

## 🧠 Best Practices

- Use `<ul>` for categories or unordered items
- Use `<ol>` for steps or rankings
- Always close your `<a>` tags and include meaningful link text
- Never link with “click here” – describe the destination

---

