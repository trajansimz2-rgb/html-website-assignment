# HTML Website Development Assignment

Student Name: [Your Name]
Student ID: [Your ID]
GitHub Repository: [Your Repository URL]

---

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

> Note for whoever's grading this: this site is normally backed by a live
> database (Supabase) with real congregation data. For this submission all
> real credentials and personal records have been removed/replaced with
> placeholder "Demo Publisher" data so it's safe to make public — see the
> note near the top of `assets/app.js`.

## Question 2: HTML Elements

1. **Which 5 elements did you find most challenging to implement and why?**
   [Fill in based on your own experience — candidates from this project:
   `<section>` (deciding which admin-panel tab panes deserved to be sections
   vs. plain containers), `<article>` (recognizing the three login modes —
   publisher, secretary, accounts — as self-contained pieces of content),
   `<form>`/`<input>` combinations with `maxlength`/`inputmode` for the PIN
   field, `<noscript>` (writing a sensible fallback message for a JS-heavy
   app), and nested `<div>` structuring for the admin modal's tab system.]

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
   [Fill in — likely `<section>`, since splitting the admin panel into eight
   labelled sections (one per tab) made it easy to show/hide the right one and
   kept each piece of functionality clearly separated in the markup.]

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
   [Fill in — candidates: `placeholder` on every input, which shows what
   format is expected (e.g. `placeholder="••••"` on the PIN field) without
   needing extra label text; or `alt` on the logo image, which keeps the page
   meaningful even if the image doesn't load; or `inputmode="numeric"` on the
   PIN field, which brings up a numeric keypad on mobile.]

## Question 4: Development Process

1. **How did you plan your website structure before coding?**
   [Fill in with your actual process — e.g. mapped out the three user roles
   this site needed to support (publisher, secretary, accounts servant) and
   what each one needed to see, before deciding on the login/app/admin-panel
   structure.]

2. **What was your approach to testing and debugging your HTML?**
   [Fill in — e.g. opened the file directly in a browser after each change,
   used browser DevTools to inspect the DOM and confirm elements had the
   right `id`s for JavaScript to find them, and checked the console for
   errors after every edit.]

3. **What challenges did you face and how did you overcome them?**
   [Fill in based on your actual experience — e.g. making sure tag renames
   (like `<div>` → `<section>`) didn't break existing JavaScript, since the
   app was already functional before the semantic cleanup.]

## Question 5: Git & GitHub Implementation

1. **What Git commands did you use during development?**
   [Fill in — typically: `git init`, `git add .`, `git commit -m "..."`,
   `git branch -M main`, `git remote add origin <url>`, `git push -u origin main`.]

2. **How many commits did you make and what was your commit message strategy?**
   [Fill in with your actual commit count and habits.]

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
   [Fill in — e.g. wrap the login forms in real `<form>` elements with proper
   submit handling, add more ARIA attributes for accessibility, or add a
   dedicated settings page.]

---

## Technical Requirements Checklist

- [x] 25+ different HTML elements used (31 used)
- [x] 15+ different HTML attributes used (22 used)
- [x] Semantic HTML structure implemented
- [x] Website works in a web browser
- [ ] GitHub repository with all code
- [x] README.md file with documentation (this file)
- [ ] Instructor added as collaborator (`instructor-webdev`)
- [ ] Instructor followed on GitHub
- [ ] Google Classroom submission completed
