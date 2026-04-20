# 01 - HTML Basics (Class Notes)

## What actually is HTML?

**HTML** stands for **HyperText Markup Language**.
- **HyperText**: Just a fancy word for links. It means web pages are connected to each other so you can jump around.
- **Markup Language**: This is important to remember—HTML is *not* a programming language like Python or C++. You can't do math or write logic loops with it. We just use "tags" to wrap around our text to tell the browser what it is (like a heading, a paragraph, or a button).

*Think of it this way: HTML is the skeleton of the website. CSS is the skin to make it look good. JavaScript is the muscle to make it move.*

---

## The Core Document Structure (Boilerplate)

Every single webpage needs this exact skeleton to operate properly. If you type `!` and press Enter in VSCode, it generates this automatically!

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Aakash's First Page</title>
    </head>
    <body>
        <h1>Hello World</h1>
        <p>This is what you actually see on screen.</p>
    </body>
</html>
```

Here is exactly what each line is doing:

### 1. The Browser Rule: `<!DOCTYPE html>`
- Always put this on line 1.
- **Why we need it**: It tells the web browser (like Chrome or Safari) to read our code using the newest, cleanest standard (HTML5). Without it, the browser might try to read it like it's from 1999 and break our layout.

### 2. The Main Wrapper: `<html>`
- This tag wraps around literally everything else.
- Notice the `lang="en"` part? That tells Google Translate and screen readers that our page is in English. It's a small detail, but super professional.

### 3. The Brain: `<head>`
- Everything inside the `<head>` tag is **invisible** on the actual webpage. This is just background info for the browser and search engines.
- **`<meta charset="UTF-8">`**: This is a lifesaver. It tells the browser to use a specific character dictionary that includes every language symbol and emoji. If you forget this, emojis might turn into weird broken squares.
- **`<title>`**: This is the text that shows up in the tab at the top of your browser. More importantly, this is the exact text Google uses as the blue clickable link when your site shows up in a search!

### 4. The Canvas: `<body>`
- Everything inside the `<body>` tag is the physical stuff you can see and click on. All your paragraphs, images, and links go exactly between `<body>` and `</body>`.

---

## Leaving Notes in the Code (Comments)

Comments are notes you write directly in the code that the browser completely ignores. They will never show up on the live website.

**How to write one:** You open it with `<!--` and close it with `-->`.

```html
<!-- Charv, don't forget to fix this spelling mistake tomorrow! -->
<h1>Welcome to my website.</h1>
```

**Pro Tip:** Top students use comments to temporarily "hide" broken code without deleting it. If an image is broken, just wrap it in a comment until you can fix it later!

```html
<p>Working code</p>

<!-- Hiding this broken image for now!
<img src="broken-file.jpg">
-->
```

---

## Golden Rules
1. **Always use lowercase for your tags.** While `<HTML>` technically works, nobody does that in the real world. Keep it cleanly lowercase `<html>`.
2. **Indent your code!** Browsers don't care about spaces or enters, but humans do. If you nest a tag inside another tag, hit the `Tab` key so it's easy to read. Messy code is impossible to debug later!



---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
