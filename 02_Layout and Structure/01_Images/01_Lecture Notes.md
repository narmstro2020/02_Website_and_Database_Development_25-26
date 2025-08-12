# 👩‍🏫 Lecture Notes – Day 06: HTML Images and Attributes

---

## 🎯 Objective

By the end of this class, students will:
- Use the `<img>` tag to insert images into a webpage
- Understand and apply the attributes: `src`, `alt`, `title`, `width`, and `height`

---

## 🧱 1. The `<img>` Tag

### 📌 Syntax:
```html
<img src="image.jpg" alt="Description of image">
```

### ✅ Key Characteristics:
- It is **self-closing** (no closing tag like `</img>`)
- Requires the `src` attribute
- Should always include `alt` for accessibility

---

## 🔤 2. Attributes Explained

| Attribute | Description |
|----------|-------------|
| `src`    | Path to the image file (local or URL) |
| `alt`    | Alternate text for screen readers and fallback |
| `title`  | Tooltip that appears when hovered over |
| `width`  | Controls the width of the image (px or %) |
| `height` | Controls the height of the image (px or %) |

---

## 🖼️ 3. Basic Examples

### 🧭 Remote Image:
```html
<img src="https://example.com/pic.jpg" alt="A mountain at sunset">
```

### 💾 Local Image:
```html
<img src="images/cat.png" alt="Cute cat" title="This is a cat">
```

---

## 🔍 4. Resizing Images

You can control size using `width` and `height`:

```html
<img src="dog.jpg" alt="Dog" width="200" height="150">
```

or

```html
<img src="tree.jpg" alt="Tree" width="50%">
```

> ⚠️ Keep aspect ratio in mind — specifying only width will scale proportionally.

---

## 📐 5. Example Code Block

```html
<!DOCTYPE html>
<html>
<head>
  <title>Image Practice</title>
</head>
<body>

  <h1>My Image Gallery</h1>

  <img src="https://upload.wikimedia.org/wikipedia/commons/4/47/PNG_transparency_demonstration_1.png"
       alt="Checkerboard PNG transparency demo"
       title="A transparent image example"
       width="300" height="200">

  <img src="images/dog.jpg"
       alt="My dog smiling"
       title="Doggo!"
       width="250">

</body>
</html>
```

---

## ❓ Check for Understanding

1. What happens if the `src` is incorrect?
2. Why is the `alt` attribute important for accessibility?
3. What does the `title` attribute do?
4. When would you use width as a percent vs pixels?

---

## 💬 Vocabulary Recap

| Term     | Meaning |
|----------|---------|
| `<img>`  | Tag to insert an image |
| `src`    | Image file source |
| `alt`    | Alternate text for the image |
| `title`  | Tooltip text |
| `width`  | Horizontal size of the image |
| `height` | Vertical size of the image |

---

## 🧠 Tips

- Use relevant `alt` text — describe the image for those who cannot see it
- Always test if images load by refreshing in browser
- Start with fixed pixel width (e.g., 300px) before experimenting with % sizes

---

## 🧪 Mini Challenge

```html
<img src="https://placekitten.com/300/200"
     alt="A cute kitten"
     title="This kitten is adorable!"
     width="300" height="200">
```

Ask students to:
- Add this to their file
- Change the `alt`, `title`, and width to reflect their own preferences

---
