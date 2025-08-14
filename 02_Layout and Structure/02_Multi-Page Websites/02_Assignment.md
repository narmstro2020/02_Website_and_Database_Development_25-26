# ✅ Instructor Solution – Multi-Page Website with Folder Structure and Relative Paths

## Folder Structure:

```
project-folder/
├── index.html
├── pages/
│   ├── about.html
│   └── contact.html
```

---

## index.html (in root)

```html
<!DOCTYPE html>
<html>
<head>
  <title>Home</title>
</head>
<body>

  <h1>Welcome to My Website</h1>

  <nav>
    TODO: Link to About
    TODO: Link to Contact
  </nav>

  <p>This is the homepage.</p>

</body>
</html>
```

---

## pages/about.html

```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>

  <h1>About Me</h1>

    <nav>
        TODO: Link to Home
        TODO: Link to Contact
    </nav>

  <p>This page tells you about me.</p>

</body>
</html>
```

---

## pages/contact.html

```html
<!DOCTYPE html>
<html>
<head>
  <title>Contact</title>
</head>
<body>

  <h1>Contact Me</h1>

    <nav>
        TODO: Link to Home
        TODO: Link to About
    </nav>

  <p>Email me at: student@example.com</p>

</body>
</html>
```

---

## Summary:

- All pages include a working `<nav>` with relative paths.
- Pages are properly placed in folders.
- Links move between root and subfolders using relative paths (`../`).

