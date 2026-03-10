# Glossary of Terms

## Introduction

Web development comes with its own vocabulary. This glossary defines the most important terms you'll encounter as a beginner, organized alphabetically for easy reference.

Bookmark this chapter and return to it whenever you come across an unfamiliar term.

---

## A

### API (Application Programming Interface)
A set of rules and protocols that allows different software applications to communicate with each other. In web development, APIs typically let the front-end of a website request data from the back-end, or connect to third-party services. APIs usually communicate by sending and receiving data in JSON format over HTTP.

*Example: When a weather app shows you today's forecast, it's using a weather API to fetch that data from an external service.*

### Attribute
Additional information added to an HTML element inside the opening tag. Attributes modify the behavior or appearance of the element.

```html
<img src="photo.jpg" alt="A sunset photo" width="400">
```
In this example, `src`, `alt`, and `width` are attributes of the `<img>` element.

---

## B

### Back-End
The server-side of a web application — the part users don't see. The back-end handles business logic, data processing, authentication, and communication with databases. Common back-end languages include Python, JavaScript (Node.js), PHP, and Ruby.

*Contrast with: Front-End*

### Browser
A software application used to access and display websites. Common browsers include Google Chrome, Mozilla Firefox, Safari, Microsoft Edge, and Opera. Each browser has its own rendering engine that interprets HTML, CSS, and JavaScript.

### Bug
An error or flaw in code that causes it to behave incorrectly or unexpectedly. Fixing bugs is called **debugging**.

---

## C

### Cache
A temporary storage location that saves copies of files so they can be loaded faster in the future. Browsers cache web pages, images, and scripts so repeat visits load more quickly.

### CLI (Command Line Interface)
A text-based interface for interacting with a computer by typing commands, as opposed to using a graphical interface with buttons and menus. Also called the terminal or command prompt.

*Examples: Terminal on Mac/Linux, Command Prompt or PowerShell on Windows.*

### CSS (Cascading Style Sheets)
A stylesheet language used to describe the visual presentation of an HTML document. CSS controls colors, fonts, sizes, spacing, layout, and animations.

```css
h1 {
  color: navy;
  font-size: 2rem;
}
```

*See also: HTML, Responsive Design*

---

## D

### Database
An organized system for storing, managing, and retrieving data. Web applications use databases to persist information like user accounts, posts, and products. Two main types: relational (SQL) databases and non-relational (NoSQL) databases.

*Examples: MySQL, PostgreSQL, MongoDB, SQLite.*

### Debugging
The process of finding and fixing errors (bugs) in code. Common debugging methods include reading error messages, using `console.log()` statements, and using browser DevTools.

### DOM (Document Object Model)
A programming interface that represents an HTML document as a tree of objects. JavaScript uses the DOM to dynamically read, modify, and respond to changes in a web page's content and structure.

```javascript
// Accessing and modifying the DOM
document.getElementById("title").textContent = "New Title";
```

---

## E

### Element
A component of an HTML document, defined by an opening tag, optional content, and a closing tag.

```html
<p>This is a paragraph element.</p>
```

### Event
An action or occurrence detected by the browser, such as a mouse click, key press, form submission, or page load. JavaScript can listen for events and respond to them.

```javascript
button.addEventListener("click", function() {
  alert("Clicked!");
});
```

---

## F

### Framework
A pre-written collection of code that provides a structure and set of tools for building applications faster. Frameworks define how your application should be organized.

*Front-end frameworks/libraries: React, Vue, Angular*
*Back-end frameworks: Express (Node.js), Django (Python), Laravel (PHP)*

### Front-End
The client-side of a web application — everything the user sees and interacts with in the browser. Built with HTML, CSS, and JavaScript.

*Contrast with: Back-End*

### Full-Stack
A developer (or approach) that covers both front-end and back-end development. A full-stack developer can build a complete web application from the user interface to the database.

---

## G

### Git
A distributed version control system used to track changes to code over time. Git allows developers to save snapshots of their work, revert to earlier versions, and collaborate with others without overwriting each other's changes.

*See also: GitHub, Version Control*

### GitHub
A web-based platform for hosting Git repositories. GitHub provides cloud storage for code, collaboration tools, pull requests, issue tracking, and a public portfolio for developers.

---

## H

### HTML (HyperText Markup Language)
The standard language for creating the structure and content of web pages. HTML uses tags to define elements like headings, paragraphs, images, and links.

```html
<h1>Hello, World!</h1>
<p>This is a paragraph.</p>
```

### HTTP / HTTPS
**HTTP (HyperText Transfer Protocol)** is the protocol used for transferring data between a browser (client) and a web server. **HTTPS** (the "S" stands for Secure) is the encrypted version, which protects data in transit. Modern websites should always use HTTPS.

---

## I

### IDE (Integrated Development Environment)
A software application that provides a comprehensive set of tools for writing, testing, and debugging code in one place. Features typically include code completion, syntax highlighting, file management, and a built-in terminal.

*Examples: Visual Studio Code, WebStorm, PyCharm.*

---

## J

### JavaScript (JS)
A programming language that runs in the browser (and on servers via Node.js). JavaScript adds interactivity and dynamic behavior to web pages — responding to user actions, updating content, and communicating with servers.

### JSON (JavaScript Object Notation)
A lightweight text format used for storing and transmitting data. JSON is widely used for APIs because it is easy for both humans and machines to read.

```json
{
  "name": "Alice",
  "age": 30,
  "hobbies": ["coding", "reading"]
}
```

---

## L

### Library
A collection of pre-written code that you can use in your own projects to add specific functionality without building it from scratch. Unlike frameworks, libraries give you more control — you call them when needed.

*Examples: jQuery (DOM manipulation), Lodash (JavaScript utilities), React (UI components).*

### Linter
A tool that automatically analyzes code for errors, style inconsistencies, and potential bugs. Linters help enforce coding standards and catch mistakes before they cause problems.

*Examples: ESLint (JavaScript), Stylelint (CSS), Flake8 (Python).*

---

## N

### Node.js
A JavaScript runtime environment that allows JavaScript to run on the server, outside the browser. Node.js is commonly used for building back-end applications and APIs.

---

## R

### Render
The process by which a browser interprets HTML, CSS, and JavaScript and displays the final visual output on screen.

### Repository (Repo)
A storage location for a project's code and its history. In Git, a repository contains all the files, folders, and change history of a project. Repositories can be stored locally or hosted on platforms like GitHub.

### Responsive Design
An approach to web design that ensures a website looks and works well on all screen sizes — from mobile phones to desktop monitors. Achieved using CSS media queries, flexible layouts, and relative units.

---

## S

### Semantic HTML
The use of HTML elements that carry meaning about the content they contain, beyond just their visual appearance. Semantic HTML improves accessibility, SEO, and code readability.

*Examples: `<header>`, `<nav>`, `<main>`, `<article>`, `<footer>` instead of generic `<div>` elements.*

### Server
A computer or software system that receives requests from clients (browsers) and sends back responses (web pages, data, files). Servers can be physical machines or cloud-based virtual machines.

### SQL (Structured Query Language)
A language used to interact with relational databases — creating tables, inserting data, querying records, and updating or deleting information.

```sql
SELECT name, email FROM users WHERE active = 1;
```

---

## T

### Tag
The markup syntax used in HTML to define elements. Tags are enclosed in angle brackets (`< >`). Most elements have an opening tag and a closing tag (which includes a forward slash).

```html
<p>This is a paragraph.</p>
<!--  ↑ opening tag    ↑ closing tag -->
```

---

## U

### URL (Uniform Resource Locator)
The web address used to locate a resource on the internet. A URL includes a protocol, domain name, and optional path.

```
https://www.example.com/about
  ↑        ↑              ↑
protocol  domain         path
```

---

## V

### Version Control
A system that records changes to files over time so that specific versions can be recalled later. Version control allows developers to undo mistakes, track history, and collaborate on the same codebase simultaneously.

*The most widely used version control system is Git.*

---

## W

### Web Application
An application that runs in a web browser rather than being installed on a device. Web applications are more dynamic and interactive than traditional static websites.

*Examples: Gmail, Google Docs, Trello, online banking portals.*

### Web Server
Software that handles HTTP requests and serves web pages or data to clients. Common web servers include Apache, Nginx, and the built-in server in Node.js.

---

## Quick Reference Cheat Sheet

| Term | One-Line Definition |
|---|---|
| HTML | Defines the structure and content of a web page |
| CSS | Controls the visual style and layout |
| JavaScript | Adds interactivity and dynamic behavior |
| Front-End | What users see in the browser |
| Back-End | Server-side logic, databases, and APIs |
| Full-Stack | Development covering both front-end and back-end |
| API | A bridge for communication between software systems |
| DOM | The browser's object-based representation of the HTML page |
| Git | Version control system for tracking code changes |
| GitHub | Cloud platform for hosting and sharing Git repositories |
| Node.js | JavaScript runtime for server-side development |
| Database | Organized storage system for persistent data |
| SQL | Language for interacting with relational databases |
| JSON | Text format used for exchanging data |
| Responsive Design | Design that adapts to all screen sizes |
| Framework | Pre-built structure for organizing an application |
| Library | Pre-written code for adding specific functionality |
| IDE | Code editor with built-in development tools |
| CLI | Text-based interface for running commands |
| HTTP/HTTPS | Protocol for transferring data on the web |

---

> **You've reached the end of the guide!**
> Return to [Chapter 1 – What is Web Development?](../introduction/chapter1-introduction.md) anytime for a refresher, or explore the [Learning Resources](chapter7-resources.md) to keep building your skills.