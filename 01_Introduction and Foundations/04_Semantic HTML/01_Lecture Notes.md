# 👩‍🏫 Lecture Notes – Day 04: Semantic HTML

---

## 🎯 Objective

By the end of this lesson, students will be able to define and use semantic HTML tags:
- `<header>`
- `<footer>`
- `<nav>`
- `<main>`
- `<section>`
- `<article>`

---

## 🧠 What is Semantic HTML?

**Semantic HTML** means using HTML tags that convey **meaning** about the content they contain.  
Instead of using generic `<div>` tags everywhere, semantic elements tell the browser and developer *what the content is*.

---

## 🧱 Why Use Semantic Elements?

- Improves **accessibility** (screen readers understand the layout)
- Helps **SEO** (search engines can better understand your content)
- Makes code easier to **read** and **maintain**

---

## 🔤 Semantic Tags Breakdown

### `<header>`
Used at the top of a page or section. Often contains the site title, logo, or navigation.

```html
<header>
  <h1>My Blog</h1>
  <p>Thoughts, stories, and ideas.</p>
</header>
```

---

### `<nav>`
Defines a block of navigation links.

```html
<nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</nav>
```

---

### `<main>`
Holds the primary content for the page. There should only be **one** `<main>` per page.

```html
<main>
  <h2>Welcome!</h2>
  <p>This is the main content of the page.</p>
</main>
```

---

### `<section>`
Groups related content. Can contain multiple headings and paragraphs.

```html
<section>
  <h2>Upcoming Events</h2>
  <p>We’re hosting a coding camp this summer!</p>
</section>
```

---

### `<article>`
Contains self-contained content like a blog post or news story.

```html
<article>
  <h2>Top 10 VS Code Tips</h2>
  <p>Learn how to boost productivity using VS Code shortcuts...</p>
</article>
```

---

### `<footer>`
Appears at the bottom of a page or section. Contains copyright, links, etc.

```html
<footer>
  <p>&copy; 2025 My Website</p>
  <p><a href="privacy.html">Privacy Policy</a></p>
</footer>
```

---

## 🧪 Full Semantic Page Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Semantic HTML Example</title>
</head>
<body>

  <header>
    <h1>My Personal Portfolio</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projects</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <h2>About Me</h2>
      <p>I am a high school student learning web design and coding.</p>
    </section>

    <section>
      <h2>Featured Project</h2>
      <article>
        <h3>HTML Text Styling Page</h3>
        <p>This page uses headings, paragraphs, and emphasis tags!</p>
      </article>
    </section>
  </main>

  <footer>
    <p>Contact: me@example.com</p>
    <p>&copy; 2025 My Name</p>
  </footer>

</body>
</html>
```

---

## ❓ Questions to Ask Students

1. Why might you use `<article>` instead of `<div>`?
2. What’s the difference between `<section>` and `<div>`?
3. How many `<main>` elements should be on one page?
4. Can you nest `<section>` inside `<main>`?

---

## 📚 Vocabulary Recap

| Tag         | Purpose                                      |
|-------------|----------------------------------------------|
| `<header>`  | Intro content for page/section               |
| `<footer>`  | Closing info like copyright, links           |
| `<nav>`     | Navigation menu                              |
| `<main>`    | Primary content area of a page               |
| `<section>` | Logical grouping of related content          |
| `<article>` | Self-contained unit (e.g., blog, post, news) |

---

## ✅ Best Practices

- Use only **one** `<main>` per page
- Use semantic tags instead of `<div>` whenever possible
- Make sure semantic elements actually match their intended purpose

