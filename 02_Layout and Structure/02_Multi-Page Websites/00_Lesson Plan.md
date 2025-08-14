# 🧠 WARRIOR Protocol-Based Lesson Plan

**Unit/Topic:** Multi-Page Websites – Folder Structure & Relative Paths  
**# Days:** 1  
**Quarter:** 1  

---

## 🕒 Timing Overview

| Section     | Time (min) | Activity Description                                                           |
|-------------|------------|--------------------------------------------------------------------------------|
| Welcome     | 5          | Warm-up discussion on navigating websites and tabs                             |
| Aim         | 2          | Set the objective for building multi-page sites with folders and relative links|
| Review      | 8          | Recall `<a href>`, file saving, and file naming practices                      |
| Relevant    | 25         | Teach folder structure, internal linking, and relative paths                   |
| Interactive | 25         | Code-along to build a 3-page site using folders and relative paths             |
| Ownership   | 15         | Students create their own site with homepage and subpages                      |
| Resonate    | 6          | Exit ticket and optional peer site preview                                    |
| **Total**   | **86**     |                                                                                |

---

## 🔵 W – Welcome

**Teacher’s Role:**
- Ask: “How do you usually move around on a website?”
- Share a few examples like header nav, sidebars, or footers.
- Use responses to take attendance and connect to linking concepts.

**Student’s Role:**
- Respond about how they move from one page to another online.

**Purpose:**
- Establish relevance of page navigation and prepare for relative links.

---

## 🟢 A – Aim

**Objective (posted and read aloud):**  
> *By the end of today’s class, you will be able to create a multi-page website using folders and relative paths for linking pages together.*

**Why this matters:**
- Nearly all websites use multiple pages; understanding folder structure makes this scalable.

**Monitoring:**
- Check students’ link paths during code walkthroughs and review exit tickets.

---

## 🟡 R – Review

**Teacher’s Role:**
- Ask:
  - “What does `<a href>` do?”
  - “How do we name our files in HTML?”
- Project yesterday’s single-page HTML structure.

**Student’s Role:**
- Answer questions and identify where linking might happen between pages.

**Modification Strategy:**
- If students struggled previously, provide working page templates to test folder linking.

---

## 🟠 R – Relevant Instruction

**Activity: Teach Folder Organization and Linking (25 mins)**

**Teacher’s Role:**
- Teach:
  - Creating folders like `/images`, `/pages`, `/css`
  - Placing HTML files in different folders
  - Linking pages using `../` and nested paths
  - Example: `href="pages/about.html"` or `href="../index.html"`
- Project folder tree diagram and examples on screen

**Instructional Methods:**
☑ Mini-lesson  
☑ Visual diagram  
☑ Live folder walkthrough in WebStorm  
☑ Anchor chart/poster for relative path syntax

**Opportunities to Respond:**
1. “What would the path be from `pages/about.html` to `index.html`?”
2. “How would you link to a file in a subfolder?”

**Differentiation:**
- Scaffold with pre-made folder templates
- Enrich with image or CSS file linking

---

## 🔴 I – Interactive

**Activity: Code-Along Multi-Page Site (25 mins)**

**Teacher’s Role:**
- Walk students through:
  1. Creating folders and placing HTML files
  2. Linking nav menus across multiple pages
  3. Previewing links in browser

**Student’s Role:**
- Create:
  - index.html in root
  - about.html in `/pages`
  - contact.html in `/pages`
- Link them with `<a href>` using relative paths

**Fun Element:**
- Add emojis or themed styling for nav bars

---

## 🟣 O – Ownership

**Activity: Build Your Own 3-Page Site (15 mins)**

**Teacher’s Role:**
- Set challenge: homepage + 2 subpages + working links
- Encourage folder use for organization

**Student’s Role:**
- Build a basic personal site:
  - Home page (index.html)
  - About Me (pages/about.html)
  - Hobbies (pages/hobbies.html)
- Ensure all pages link to each other correctly

**Voice/Choice:**
- Pick topic (portfolio, game review, pet showcase)

**Community Connection:**
- Ask students to show a peer or family member how to navigate the site

---

## 🟤 R – Resonate

**Activity: Exit Ticket + Site Preview (6 mins)**

**Teacher’s Role:**
- Ask:
  1. What is a relative path?
  2. How would you link from a subfolder to your homepage?
- Optional: Have 1-2 students demo their folder structure to the class

**Student’s Role:**
- Submit answers and reflect on what was confusing or successful

**Assessment:**
- Review project folders and link behavior for understanding

---

## 📦 Supplies

- Student computers with WebStorm
- Sample folder templates
- Whiteboard or projector folder structure visual
- Exit ticket prompt handout or Google Form
- Code-along reference site and solution files
