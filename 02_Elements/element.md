# 02 - HTML Elements & The DOM (Class Notes)

## What exactly is an "Element"?

An **element** is everything from the start tag to the end tag, including whatever is inside it. 
- The tag itself (like `<p>`) is just the marker. 
- The **element** is the whole package: `<p>This is the actual element.</p>`

*Why does this distinction matter? Because when you start writing JavaScript later, you aren't grabbing a "tag". You are targeting an "Element Node" in the computer's memory!*

---

## 1. Anatomy of an Element

Most elements have three distinct parts:
1. **Opening Tag**: `<p>`
2. **Content**: The text or image inside.
3. **Closing Tag**: `</p>` (Always has that forward slash!)

If you forget the closing slash, the browser will assume everything for the rest of the page belongs inside that first element. Huge bug!

## 2. Empty (Void) Elements

Some elements don't wrap around text, so they simply don't need a closing tag. We call these **Void Elements**.

- `<br>`: Forces a line break.
- `<hr>`: Draws a horizontal line.
- `<img>`: Embeds an image.
- `<meta>`: Sets background data.

**Pro Tip:** In the old days (XHTML), you *had* to write them with a self-closing slash like `<br/>`. In modern HTML5, you can just write `<br>`. Both work perfectly, but typing less is usually better!

---

## 3. Advanced Nesting (The DOM Tree)

You can (and will) put elements inside of other elements. This is called **Nesting**.

```html
<!-- Correct Nesting! -->
<div>
    <h1>Welcome</h1>
    <p>This is Aakash's profile.</p>
</div>
```

When you nest elements, you are physically building something called the **Document Object Model (DOM) Tree**.
- The `<div>` is the **Parent**.
- The `<h1>` and `<p>` are its **Children**.
- The `<h1>` and `<p>` are **Siblings** to each other.

### The Golden Rule of Nesting (The "Russian Doll" Rule)
The first element you open MUST be the last element you close. 

```html
<!-- INCORRECT: The browser will try to auto-fix this and might break your layout! -->
<p>This is <b>wrong</p></b>

<!-- CORRECT: The bold tag opened last, so it closes first! -->
<p>This is <b>right</b></p>
```

### The "Block inside Inline" Trap
One of the most common mistakes intermediate developers make is putting a massive structural element (like a `<div>`) inside a tiny text element (like a `<span>`). 
- **Rule of thumb**: Big block elements go on the outside. Small inline elements go on the inside. Never the other way around!




---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
