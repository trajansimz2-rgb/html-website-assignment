
# HTML Website Development Assignment

Student Name: Trajan Simfukwe
Student ID: 2512237271
GitHub Repository: https://github.com/trajansimz2-rgb/html-website-assignment

## Question 1: Website Creation

I built a **congregation publisher records and accounts management website** —
a personal project I've been developing that lets members log in to view their
service reports, and lets a secretary and accounts servant manage records,
territory assignments, and monthly accounts (S-24 transaction log / S-30
report) through an admin panel. The `index.html` file uses **31 different HTML
elements** and **22 different HTML attributes**, well above the 25/15 minimum,
with semantic structure (`<header>`, `<nav>`, `<main>`, `<article>`,
`<section>`, `<footer>`) and clearly organized sections for login, the main
app, and the admin panel.

## Question 2: HTML Elements

1. **Which 5 elements did you find most challenging to implement and why?**
   As someone new to HTML, the most challenging part was not only writing tags from
   scratch but also understanding what already existed in the file: `<section>` vs
   `<article>` (learning the difference between a labelled division of
   content and a self-contained piece), the `<form>`-related inputs like
   `maxlength` and `inputmode` on the PIN field, and `<noscript>`, which I
   hadn't encountered before and had to look up.

2. **How did you use semantic elements to structure your content?**
   `<header>` wraps the top navigation bar; `<nav>` holds the nav links inside
   it; `<main>` holds the primary content area that gets filled in per user
   (`#main-content`); the three login modes (publisher / secretary / accounts)
   are each an `<article>`, since each is a self-contained, independent block
   of content; every tab inside the admin panel (Reports, Add Publisher, Edit
   Publisher, Change PIN, Territories, Summary, Service Year, Accounts) is a
   `<section>`, since each is a distinct, named division of the page; and
   `<footer>` holds the copyright line at the bottom of the page.

3. **Which element was most useful for organizing your layout and why?**
   `<section>` — splitting the admin panel into eight separate sections
   (Reports, Add Publisher, Territories, Accounts, etc.) made it easy to
   understand which part of the page did what, even without deep coding
   experience.

## Question 3: HTML Attributes

1. **Which 3 attributes were essential for making your website functional?**
   `id` (every interactive element — inputs, selects, buttons, tab panes — is
   targeted by JavaScript through its `id`, so this is what makes the whole
   app work), `onclick`/`onchange` (wire up every button and dropdown to the
   right function), and `class` (used both for CSS styling and, in several
   places, as the hook JavaScript uses to find and toggle groups of elements
   like `.admin-tab-pane`).

2. **How did you use the `class` and `id` attributes differently?**
   `id` is always unique — one element, one purpose (e.g. `id="pub-pin"` is
   the one PIN input; `id="atab-accounts"` is the one Accounts tab pane).
   `class` is reused across many elements that share behavior or styling,
   e.g. every admin tab pane has `class="admin-tab-pane"` so JavaScript can
   select and hide all of them at once, while each one's unique `id` picks
   out the specific one to show.

3. **Which attribute helped improve user experience the most and why?**
   `placeholder`, since it shows what format is expected in a field (like the
   PIN box showing `••••`) without me needing to read extra instructions.

## Question 4: Development Process

1. **How did you plan your website structure before coding?**
   I started from an existing project I'd been developing and focused on
   understanding its three main user roles — publisher, secretary, and
   accounts servant — and how the login and admin panel needed to support
   each one.

2. **What was your approach to testing and debugging your HTML?**
   I opened `index.html` directly in my browser after each change and
   checked that the page still loaded correctly and nothing looked broken.

3. **What challenges did you face and how did you overcome them?**
   As a beginner, the biggest challenge was understanding HTML/GitHub
   terminology I hadn't encountered before — things like "repository,"
   "commit," and "collaborator." I worked through each concept step by step
   rather than trying to learn everything at once.

## Question 5: Git & GitHub Implementation

1. **What Git commands did you use during development?**
   I used GitHub's browser-based file upload rather than the command line,
   so no terminal Git commands were needed — I dragged my files directly
   into the repository through GitHub's web interface.

2. **How many commits did you make and what was your commit message strategy?**
    It's 5: one for uploading the files, and the 4 for editing this README.

3. **Why is version control important for web development projects?**
   Version control keeps a full history of every change, so a mistake can be
   reverted without losing other work, and it's what makes it safe to
   experiment — like renaming elements for better semantics — because you can
   always go back if something breaks.

## Question 6: Code Quality & Best Practices

1. **How did you ensure your HTML was valid and error-free?**
   Every opening tag has a matching closing tag with correct nesting (no
   mismatched or unclosed elements), form fields use `label`/`for` pairing
   where applicable, and images include `alt` text.

2. **What best practices did you follow for writing clean, readable code?**
   Consistent indentation, lowercase tag and attribute names, `id` names that
   describe purpose rather than appearance (`atab-accounts`, not `tab3`),
   HTML comments marking each major section (e.g. `<!-- TAB: Accounts -->`),
   and choosing the semantic element that matches each piece of content's
   actual role rather than defaulting to `<div>` everywhere.

3. **How would you improve your website if you had more time?**
   I'd like to learn enough HTML/CSS to make small style changes myself, and
   understand the JavaScript well enough to add new features on my own rather
   than relying on outside help.

---

## Technical Requirements Checklist

- [x] 25+ different HTML elements used (31 used)
- [x] 15+ different HTML attributes used (22 used)
- [x] Semantic HTML structure implemented
- [x] Website works in a web browser
- [x] GitHub repository with all code
- [x] README.md file with documentation (this file)
- [ ] Instructor added as collaborator (`instructor-webdev`)
- [ ] Instructor followed on GitHub
- [ ] Google Classroom submission completed
