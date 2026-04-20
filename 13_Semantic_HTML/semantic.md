# 13 - Semantic HTML (Class Notes)

## The War Against "Div Soup"

HTML5 changed everything. Before HTML5, if you wanted to build a web page, you had to use generic `<div>` tags for absolutely every element. You would end up with `<div class="header">`, `<div class="main">`, `<div id="footer">`. 

To human eyes reading the code, this was obvious. But to Google's Search Engine bots, and to screen-reader software used by blind people? It was completely unreadable. It was just a giant wall of meaningless rectangular boxes.

**Enter Semantic HTML.**
Semantic tags physically describe their meaning directly to the browser instance!

---

## 1. The Core Semantic Shell

Khushi ensures every website follows the standard Semantic Outline. It maps out perfectly like the zones of a newspaper:

- **`<header>`**: The very top block. Usually contains the website logo and the top-level main navigation.
- **`<nav>`**: The exact block that contains your primary navigational links. (Never put footer links or privacy policies in a nav tag!)
- **`<main>`**: This is the absolute most important tag. You are only legally allowed to have exactly **one** `<main>` tag per page. It holds the core story/app of the page, stripping away sidebars and headers.
- **`<footer>`**: The bottom wrapper. Holds copyright info and legal routing.

---

## 2. The `<article>` vs `<section>` Debate

This confuses a lot of intermediate developers! What is the difference between an Article and a Section? Daulat explains:

### `<article>` (Stand-alone Independence)
Use this tag if the content could theoretically be ripped out of the webpage, printed on a piece of paper, handed to someone on the street, and it would *still perfectly make sense by itself*.
- Examples: A blog post, a standalone news story, a complete forum post.

### `<section>` (Thematic Grouping)
Use this tag to group related chunks of data together *inside* a larger piece of work, or directly inside the main body.
- Examples: "Chapter 1", "Contact Info Grid", "My Portfolio Slideshow".

```html
<!-- Correct Advanced Semantic Structure! -->
<main>
    <article>
        <h1>Jay's Complete Guide to Semantics</h1>
        
        <section>
            <h2>Part 1: The Basics</h2>
            <p>Content...</p>
        </section>
        
        <section>
            <h2>Part 2: The Rules</h2>
            <p>Content...</p>
        </section>
    </article>
</main>
```

---

## 3. The `<aside>` Tag

What do you do with content that is tangentially related, but not part of the main story? (Like an author's bio, or an advertising banner?)

You drop it in an **`<aside>`** tag! Screen readers know they can skip right past aside tags if their user just wants to read the core story of the article!






---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
