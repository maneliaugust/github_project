# Front-End Development Basics

## Introduction

Front-end development is what you see when you visit any website — the layout, the colors, the buttons, the animations. It is built on three foundational technologies: **HTML**, **CSS**, and **JavaScript**. Every website on the internet, no matter how complex, starts with these three tools.

Understanding how they work individually — and how they work together — is the foundation of all web development.

---

## HTML – The Structure of a Web Page

**HTML (HyperText Markup Language)** defines the *structure* and *content* of a webpage. Think of it as the skeleton of a website.

HTML uses **tags** to mark up content. A tag wraps around content to tell the browser what it is.

### Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>My First Web Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is my first paragraph.</p>
  </body>
</html>
```

- `<!DOCTYPE html>` – Tells the browser this is an HTML5 document.
- `<html>` – The root element that wraps everything.
- `<head>` – Contains metadata (title, character set, linked files). Not visible on the page.
- `<body>` – Contains everything visible on the page.

### Common HTML Elements

| Element | Purpose | Example |
|---|---|---|
| `<h1>` – `<h6>` | Headings (h1 is largest) | `<h1>Title</h1>` |
| `<p>` | Paragraph | `<p>Text here</p>` |
| `<a>` | Hyperlink | `<a href="https://example.com">Click</a>` |
| `<img>` | Image | `<img src="photo.jpg" alt="A photo">` |
| `<ul>` / `<ol>` | Unordered/ordered list | `<ul><li>Item</li></ul>` |
| `<div>` | Generic container/block | `<div>Group of elements</div>` |
| `<span>` | Inline container | `<span>Inline text</span>` |
| `<form>` | User input form | `<form>...</form>` |
| `<input>` | Input field | `<input type="text">` |
| `<button>` | Clickable button | `<button>Submit</button>` |

### Semantic HTML

Modern HTML encourages the use of **semantic tags** — elements that describe their purpose, not just their appearance. This improves accessibility and search engine optimization (SEO).

```html
<!-- Non-semantic (unclear meaning) -->
<div id="header">...</div>
<div id="main">...</div>

<!-- Semantic (clear, meaningful) -->
<header>...</header>
<main>...</main>
<article>...</article>
<footer>...</footer>
```

---

## CSS – The Style of a Web Page

**CSS (Cascading Style Sheets)** controls how HTML elements *look* — their colors, fonts, sizes, spacing, and positioning. Without CSS, every website would just be plain black text on a white background.

### How CSS Works

CSS rules consist of a **selector** (which element to style) and **declarations** (what to change):

```css
selector {
  property: value;
}
```

**Example:**

```css
h1 {
  color: navy;
  font-size: 36px;
  text-align: center;
}

p {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #333333;
}
```

### Three Ways to Add CSS

1. **Inline CSS** – Applied directly to an HTML element (not recommended for large projects):
   ```html
   <p style="color: red;">This is red text.</p>
   ```

2. **Internal CSS** – Written inside a `<style>` tag in the HTML `<head>`:
   ```html
   <style>
     p { color: blue; }
   </style>
   ```

3. **External CSS** (recommended) – Written in a separate `.css` file and linked to HTML:
   ```html
   <link rel="stylesheet" href="styles.css">
   ```

### The CSS Box Model

Every HTML element is treated as a **box**. Understanding the box model is critical for controlling layout and spacing:

```
+---------------------------+
|        Margin             |  ← Space outside the element
|  +---------------------+  |
|  |      Border         |  |  ← The element's border
|  |  +---------------+  |  |
|  |  |    Padding    |  |  |  ← Space inside, between border and content
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |  ← The actual text/image
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

### CSS Layout: Flexbox and Grid

Two modern CSS tools make layout much easier:

**Flexbox** – Best for arranging items in a single row or column:
```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

**CSS Grid** – Best for two-dimensional layouts (rows AND columns):
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* 3 equal columns */
  gap: 20px;
}
```

---

## JavaScript – The Behavior of a Web Page

**JavaScript (JS)** is a programming language that makes web pages *interactive* and *dynamic*. It can respond to user actions, change content on the page, fetch data from servers, and much more.

### JavaScript Basics

```javascript
// Variables
let name = "Alice";
const age = 25;

// Functions
function greet(person) {
  return "Hello, " + person + "!";
}

console.log(greet("Alice")); // Output: Hello, Alice!

// Conditionals
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

// Loops
for (let i = 0; i < 3; i++) {
  console.log("Count: " + i);
}
```

### DOM Manipulation

The **DOM (Document Object Model)** is the browser's representation of your HTML as a tree of objects. JavaScript can access and modify the DOM to change what users see without reloading the page.

```javascript
// Select an element
const heading = document.getElementById("main-title");

// Change its content
heading.textContent = "Updated Title!";

// Change its style
heading.style.color = "blue";

// Respond to a click
const button = document.querySelector("button");
button.addEventListener("click", function() {
  alert("Button was clicked!");
});
```

---

## How Websites Display Content

When a user types a URL into a browser, the following happens:

1. **DNS Lookup** – The browser looks up the IP address of the web server.
2. **HTTP Request** – The browser sends a request to the server asking for the page.
3. **Server Response** – The server sends back HTML, CSS, and JavaScript files.
4. **Parsing HTML** – The browser reads the HTML and builds the DOM tree.
5. **Applying CSS** – The browser applies styles, creating the visual layout.
6. **Running JavaScript** – Scripts execute, adding interactivity and dynamic content.
7. **Rendering** – The final, styled, interactive page appears on screen.

This entire process typically happens in milliseconds.

---

## Summary

- **HTML** provides the structure — headings, paragraphs, images, links.
- **CSS** provides the style — colors, fonts, layout, spacing.
- **JavaScript** provides the behavior — interactivity, dynamic updates, event handling.
- Browsers render pages by parsing HTML, applying CSS, and executing JavaScript.
- Learning semantic HTML, the CSS box model, and basic DOM manipulation are the first milestones of front-end development.

> **Next Chapter:** [Chapter 4 – Back-End Development Basics →](chapter4-key-concepts.md)