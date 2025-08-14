# 👩‍🏫 Lecture Notes – Multi-Page Websites, Folder Structure, and Relative Paths

---

## 🎯 Objective

Students will:
- Create multiple HTML pages
- Organize them into folders
- Use relative paths to link between pages

---

## 📁 1. Folder Structure

A good folder structure keeps your website organized.

### 📦 Example Layout:
```
project-folder/
├── index.html
├── pages/
│   ├── about.html
│   └── contact.html
├── images/
│   └── logo.png
├── css/
│   └── styles.css
```

---

## 🔗 2. Internal Links with Relative Paths

Use the `<a href="...">` tag to create internal links.

### ✅ Examples:
Link to a page in the same folder:
```html
<a href="about.html">About</a>
```

Link to a page in a subfolder:
```html
<a href="pages/about.html">About</a>
```

Link to parent folder:
```html
<a href="../index.html">Home</a>
```

---

## 🔁 3. Navigation Between Pages

### 🧩 Use consistent navigation across all pages:
```html
<nav>
  <a href="../index.html">Home</a>
  <a href="about.html">About</a>
  <a href="contact.html">Contact</a>
</nav>
```

---

## 💻 4. Example: index.html (in root folder)

```html
<!DOCTYPE html>
<html>
<head>
  <title>Home</title>
</head>
<body>

  <h1>Welcome to My Website</h1>
  <nav>
    <a href="pages/about.html">About</a>
    <a href="pages/contact.html">Contact</a>
  </nav>

</body>
</html>
```

---

## 📄 5. Example: about.html (in /pages folder)

```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>

  <h1>About Me</h1>
  <nav>
    <a href="../index.html">Home</a>
    <a href="contact.html">Contact</a>
  </nav>

  <p>This is the about page.</p>

</body>
</html>
```

---

## 🚧 6. Common Errors and Fixes

| Mistake                               | Fix                                                   |
|---------------------------------------|--------------------------------------------------------|
| File not found error (`404`)          | Check spelling and folder names                       |
| Wrong link from subfolder             | Use `../` to go up a level                            |
| Linking images without proper path    | Use `images/filename.jpg` if images are in a folder   |

---

## 🧠 Questions to Ask Students

1. How do you link from a subfolder to a file in the root?
2. What happens if your file path is incorrect?
3. Why is folder structure important for a big project?

---

## 🧰 Tips

- Keep all project files in one main folder.
- Use lowercase names with no spaces (use dashes or underscores).
- Preview your site using “Open in Browser” from your index.html file.

---

## 🧪 Challenge

Create:
- index.html in the root
- about.html and contact.html in a `pages/` folder
- A `<nav>` on all 3 pages that links to each other using relative paths

---

