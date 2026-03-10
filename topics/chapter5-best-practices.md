# Development Best Practices

## Introduction

Knowing how to write code is one thing. Knowing how to write *good* code is another. As a beginner, it's tempting to focus purely on making things work — but developing good habits early will make you a faster, more professional developer in the long run.

This chapter covers three essential areas of best practice: writing clean code, using version control with Git and GitHub, and building responsive designs.

---

## Writing Clean Code

Clean code is code that is easy to read, understand, and maintain — not just by you, but by anyone who might work with it in the future (including future you).

### 1. Use Meaningful Names

Names for variables, functions, and files should clearly describe what they do. Avoid vague names like `x`, `data`, or `temp`.

```javascript
// Bad naming
let x = 25;
function calc(a, b) {
  return a * b;
}

// Good naming
let userAge = 25;
function calculateTotalPrice(quantity, pricePerItem) {
  return quantity * pricePerItem;
}
```

### 2. Keep Functions Small and Focused

Each function should do **one thing** and do it well. If a function is doing too many things, break it into smaller functions.

```javascript
// Bad: one function doing everything
function processOrder(order) {
  // validate order
  // calculate total
  // apply discount
  // send email
  // update database
}

// Good: separate responsibilities
function validateOrder(order) { ... }
function calculateTotal(order) { ... }
function applyDiscount(total, discount) { ... }
function sendConfirmationEmail(order) { ... }
```

### 3. Avoid Repeating Yourself (DRY Principle)

DRY stands for **Don't Repeat Yourself**. If you find yourself writing the same code in multiple places, extract it into a reusable function or component.

```javascript
// Bad: repeating the same logic
console.log("Name: " + user1.name + ", Age: " + user1.age);
console.log("Name: " + user2.name + ", Age: " + user2.age);

// Good: reusable function
function displayUser(user) {
  console.log(`Name: ${user.name}, Age: ${user.age}`);
}
displayUser(user1);
displayUser(user2);
```

### 4. Write Comments Where Necessary

Comments explain *why* something is done a certain way, not *what* the code does (good code should be self-explanatory enough for the "what").

```javascript
// Bad comment (states the obvious)
let total = price * quantity; // multiply price by quantity

// Good comment (explains intent or a non-obvious decision)
// Apply a 10% discount for bulk orders (over 100 units)
if (quantity > 100) {
  total = total * 0.9;
}
```

### 5. Format and Indent Your Code Consistently

Consistent indentation makes code far easier to read. Use a linter or formatter (like **Prettier** for JavaScript) to enforce consistent style automatically.

```html
<!-- Bad formatting -->
<ul>
<li>Item 1</li>
  <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Good formatting -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

### 6. Don't Leave Dead Code Behind

Remove code that is commented out, unused variables, and functions that are no longer called. Dead code clutters your project and confuses other developers.

---

## Version Control with Git and GitHub

Version control is a system that records changes to your code over time, allowing you to review history, undo mistakes, and collaborate with others. **Git** is the industry-standard tool for version control, and **GitHub** is the most popular platform for hosting Git repositories.

### Why Version Control Matters

- **Safety net** – You can always revert to a working version if you break something.
- **History** – You can see exactly what changed, when, and why.
- **Collaboration** – Multiple developers can work on the same project without overwriting each other's changes.
- **Portfolio** – Your GitHub profile is often reviewed by employers as proof of your work.

### Core Git Workflow

```bash
# 1. Initialize a new Git repository
git init

# 2. Check the current status of your files
git status

# 3. Stage files you want to include in your next commit
git add index.html
git add .          # Stage all changed files

# 4. Commit your staged changes with a descriptive message
git commit -m "Add navigation bar to homepage"

# 5. Push your changes to GitHub
git push origin main
```

### Writing Good Commit Messages

A good commit message clearly describes *what* changed and ideally *why*.

```bash
# Bad commit messages
git commit -m "fix"
git commit -m "stuff"
git commit -m "asdfgh"

# Good commit messages
git commit -m "Fix broken login button on mobile"
git commit -m "Add password validation to signup form"
git commit -m "Update hero section copy to match new brand guidelines"
```

### Using Branches

Branches allow you to work on new features or fixes in isolation, without disrupting the main working version of your code.

```bash
# Create and switch to a new branch
git checkout -b feature/add-contact-form

# Work on your changes, then commit them
git add .
git commit -m "Add contact form with email validation"

# Switch back to the main branch
git checkout main

# Merge your feature branch into main
git merge feature/add-contact-form
```

### Essential Git Commands Reference

| Command | Description |
|---|---|
| `git init` | Start a new repository |
| `git clone <url>` | Copy a repository from GitHub |
| `git status` | See what files have changed |
| `git add <file>` | Stage a file for committing |
| `git commit -m "msg"` | Save a snapshot with a message |
| `git push` | Upload changes to GitHub |
| `git pull` | Download latest changes from GitHub |
| `git log` | View commit history |
| `git branch` | List branches |
| `git checkout -b <name>` | Create and switch to a new branch |

---

## Responsive Design

A **responsive website** adapts its layout and appearance to fit any screen size — from large desktop monitors to small mobile phones. With over half of global web traffic coming from mobile devices, responsive design is no longer optional.

### 1. Use a Mobile-First Approach

Design for the smallest screen first, then scale up. This ensures mobile users get a good experience and forces you to prioritize the most important content.

```css
/* Mobile-first: default styles apply to small screens */
.container {
  width: 100%;
  padding: 16px;
}

/* Then add larger screen adjustments */
@media (min-width: 768px) {
  .container {
    width: 720px;
    margin: 0 auto;
  }
}

@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
```

### 2. Use CSS Media Queries

**Media queries** allow you to apply different CSS rules based on screen size, resolution, or device type.

```css
/* Hide sidebar on small screens */
.sidebar {
  display: none;
}

/* Show sidebar on larger screens */
@media (min-width: 768px) {
  .sidebar {
    display: block;
    width: 250px;
  }
}
```

### 3. Use Relative Units Instead of Fixed Pixels

Relative units scale with the user's screen or font size, producing more flexible layouts.

| Unit | Description |
|---|---|
| `%` | Relative to the parent element's size |
| `em` | Relative to the current element's font size |
| `rem` | Relative to the root (html) font size |
| `vw` / `vh` | Relative to the viewport width / height |

```css
/* Rigid (bad for responsiveness) */
.card { width: 400px; font-size: 16px; }

/* Flexible (better) */
.card { width: 100%; max-width: 400px; font-size: 1rem; }
```

### 4. Use Flexbox and Grid for Layouts

As covered in Chapter 3, Flexbox and CSS Grid automatically adjust layouts for different screen sizes.

### 5. Make Images Responsive

```css
img {
  max-width: 100%;
  height: auto;
}
```

This single rule prevents images from overflowing their containers on small screens.

### 6. Test on Real Devices

Always test your website on actual mobile devices, not just browser resizing. Use Chrome DevTools' device toolbar (F12 → Toggle Device Toolbar) to simulate different screen sizes during development.

---

## Summary

- **Clean code** is readable, well-named, DRY, and properly formatted. These habits save time and reduce bugs.
- **Git and GitHub** are essential tools for tracking changes, recovering from mistakes, and collaborating with others. Learn them early.
- **Responsive design** ensures your website works well on all screen sizes. Use mobile-first CSS, media queries, and relative units.

> **Next Chapter:** [Chapter 6 – Common Beginner Mistakes →](chapter6-common-mistakes.md)