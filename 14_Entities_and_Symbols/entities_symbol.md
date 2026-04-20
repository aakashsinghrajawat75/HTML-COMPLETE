# 14 - Entities and Symbols (Class Notes)

## The Danger of Raw Code Parsing

Aakash points out a severe problem: What if you are trying to write a tutorial webpage teaching a student how to type the `<script>` tag? If you just physically write the word `<script>` into your HTML file, the web browser will instantly panic, think it's an actual piece of code, and try to execute it as JavaScript!

This is why **HTML Entities** exist. They allow us to safely print reserved code characters identically as flat text on the screen without triggering the programming engine!

---

## 1. Escaping Reserved Characters

An entity is a safe string of text that begins with an ampersand `&` and is cleanly closed with a semicolon `;`. 

If you want to render the structural brackets of HTML, you must **Escape** them:
- `<` becomes `&lt;` (Less Than)
- `>` becomes `&gt;` (Greater Than)

```html
<!-- The browser sees the characters safely and prints out: <div> -->
<p>To create a layout box, use the &lt;div&gt; tag</p>
```

### Advanced Security: Cross-Site Scripting (XSS)
Entities aren't just for tutorials; they are the foundation of Web Security! If you have a comment section on your website, a hacker might type `<script>StealPassword();</script>` into the comment box. If you don't use a backend system to automatically convert their raw code into safe **Entity Strings**, your website will physically execute their virus against every user that visits the page!

---

## 2. Advanced Typography Constraints

Have you ever tried to construct a beautiful, balanced sentence, only for a tiny word to suddenly wrap down to the next line, completely ruining the paragraph structure?

**The Non-Breaking Space (`&nbsp;`)**
This is a magical entity string. It forces the browser to treat two separate words as tightly bonded. The browser will *never* break the words across two separate lines under any condition!

```html
<!-- If the screen shrinks on mobile, "10" and "m/s" will never split apart! -->
<p>The speed of the object is 10&nbsp;m/s.</p>
```

### Business and UI Symbols
You can also use Entities to tap into the secret keyboard of global typography!
- `&copy;` generates the © copyright stamp.
- `&trade;` generates the ™ trademark stamp.
- `&rarr;` generates a perfect mathematical → arrow.





---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
