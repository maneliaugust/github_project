# Back-End Development Basics

## Introduction

While front-end development is what users *see*, back-end development is what makes a website actually *work*. Every time you log into an account, submit a form, make a purchase, or load personalized content, the back-end is handling all of that behind the scenes.

Back-end development involves three key components: **servers**, **databases**, and **APIs**. Together, they form the engine that powers dynamic web applications.

---

## Servers

### What Is a Server?

A **server** is a computer (or a software program) that listens for requests from clients (browsers) and sends back responses. When you visit a website, your browser is the *client* and the website's computer is the *server*.

### How the Client-Server Model Works

```
[User's Browser]  →  HTTP Request  →  [Web Server]
[User's Browser]  ←  HTTP Response ←  [Web Server]
```

1. The browser sends a **request** (e.g., "Give me the homepage").
2. The server receives the request, processes it, and sends a **response** (e.g., the HTML page).

### Types of Web Servers

| Server Software | Description |
|---|---|
| **Apache** | One of the oldest and most widely used web servers. Popular in PHP environments. |
| **Nginx** | Known for high performance and handling many simultaneous connections. |
| **Node.js (built-in HTTP)** | JavaScript runtime that can act as its own web server. |
| **Gunicorn / uWSGI** | Python-based application servers often used with Django or Flask. |

### Local vs. Remote Servers

- **Local development server** – Runs on your own computer while you build the app. Used for testing.
- **Remote/production server** – A server accessible on the internet. Hosted by services like AWS, DigitalOcean, Heroku, or Vercel.

---

## Databases

### What Is a Database?

A **database** is an organized system for storing and retrieving data. Without databases, every piece of data on a website would disappear the moment the server restarted.

Databases store things like:
- User accounts and passwords
- Product listings and prices
- Blog posts and comments
- Orders and transaction history

### Types of Databases

There are two main categories:

#### Relational Databases (SQL)

Store data in structured tables with rows and columns — similar to a spreadsheet. Tables can be linked together using relationships.

```sql
-- Example: Selecting all users over 18
SELECT name, email FROM users WHERE age > 18;
```

| Database | Description |
|---|---|
| **MySQL** | The most widely used relational database. Great for beginners. |
| **PostgreSQL** | Powerful, feature-rich, and open-source. Common in professional projects. |
| **SQLite** | Lightweight and file-based. Perfect for small projects and learning. |

#### Non-Relational Databases (NoSQL)

Store data as flexible documents (often JSON-like objects) rather than rigid tables. Better for unstructured or rapidly changing data.

```json
{
  "user_id": "001",
  "name": "Alice",
  "email": "alice@example.com",
  "orders": ["order_101", "order_102"]
}
```

| Database | Description |
|---|---|
| **MongoDB** | The most popular NoSQL database. Stores documents in JSON-like format. |
| **Firebase** | Google's real-time database, popular for mobile and web apps. |
| **Redis** | Used for fast in-memory storage and caching. |

### Which Should Beginners Learn First?

Start with **MySQL or SQLite** — understanding relational databases and SQL is a fundamental skill that transfers across many technologies.

---

## APIs

### What Is an API?

An **API (Application Programming Interface)** is a set of rules that allows different software systems to communicate with each other. In web development, APIs typically let the front-end communicate with the back-end without needing to reload the entire page.

Think of an API like a waiter in a restaurant:
- You (the client) place an order (a request).
- The waiter (the API) takes your order to the kitchen (the server/database).
- The kitchen prepares the food and the waiter brings it back (the response).

### REST APIs

**REST (Representational State Transfer)** is the most common style of web API. REST APIs communicate using standard HTTP methods:

| HTTP Method | Action | Example |
|---|---|---|
| `GET` | Retrieve data | Get a list of all users |
| `POST` | Create new data | Register a new user |
| `PUT` / `PATCH` | Update existing data | Update a user's email |
| `DELETE` | Remove data | Delete a user account |

### Example API Request and Response

**Request:** `GET https://api.example.com/users/1`

**Response:**
```json
{
  "id": 1,
  "name": "Alice Johnson",
  "email": "alice@example.com",
  "role": "admin"
}
```

### Why APIs Matter

- They allow front-end and back-end to be developed independently.
- They enable third-party integrations (e.g., using Google Maps on your website, processing payments via Stripe, sending emails via Mailgun).
- They support mobile apps that share the same back-end as the website.

---

## Introduction to Back-End Languages

### Node.js (JavaScript)

**Node.js** lets you run JavaScript on the server — not just in the browser. This is a popular choice for beginners who already know front-end JavaScript, since they can use one language for both sides.

```javascript
// Simple Node.js web server
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello from the server!');
});

server.listen(3000, () => {
  console.log('Server running at http://localhost:3000');
});
```

**Frameworks built on Node.js:**
- **Express.js** – Minimal and flexible. The most popular Node.js framework.
- **NestJS** – Structured and TypeScript-first. Good for larger applications.

---

### Python

Python is known for its clean, readable syntax and is widely used in web development, data science, and automation.

```python
# Simple Flask web server (Python)
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return 'Hello from Flask!'

if __name__ == '__main__':
    app.run(debug=True)
```

**Python web frameworks:**
- **Django** – Full-featured and "batteries included." Great for large, data-driven apps.
- **Flask** – Lightweight and flexible. Great for beginners and small projects.
- **FastAPI** – Modern and high-performance. Great for building APIs quickly.

---

### PHP

PHP is one of the oldest server-side languages and still powers a massive portion of the web — including **WordPress**, which runs over 40% of all websites.

```php
<?php
  $name = "Alice";
  echo "Hello, " . $name . "!";
?>
```

**PHP frameworks:**
- **Laravel** – Elegant and expressive. The most popular modern PHP framework.
- **Symfony** – Highly flexible, used in enterprise applications.

---

## Summary

- **Servers** receive requests from browsers and send back responses.
- **Databases** store and retrieve persistent data — user accounts, content, transactions.
- **APIs** allow the front-end and back-end (and third-party services) to communicate.
- **Node.js** is a great first back-end choice if you already know JavaScript.
- **Python** (with Flask or Django) is beginner-friendly and extremely versatile.
- **PHP** is mature and widely used, especially in content management systems.

> **Next Chapter:** [Chapter 5 – Development Best Practices →](chapter5-best-practices.md)