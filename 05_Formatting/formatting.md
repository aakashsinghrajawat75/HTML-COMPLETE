# 05 - HTML Text Formatting (Class Notes)

## The Great Divide: Visual Style vs Semantic Meaning

Back in the early days of the web, developers used HTML tags to physically change how things looked. If they wanted bold text, they used `<b>`. If they wanted italics, they used `<i>`. 

**This is now considered bad practice in modern development.**

Today, styling is the responsibility of CSS, not HTML. So why do we still have formatting tags? 
Because modern HTML formatting isn't about making text *look* different; it's about making text *mean* something different to screen readers and web-scrapers.

---

## 1. Bold and Italics (The Semantic Upgrade)

When you want to emphasize text, you have two sets of tools.

### The Visual Tags (Legacy)
- `<b`> (Bold)
- `<i>` (Italic)
*These tags literally just change the font visually. A visually impaired person listening to the site through a screen reader won't hear any difference in tone when the reader hits a `<b>` tag.*

### The Semantic Tags (Modern HTML5)
- `<strong>` (Strong Importance)
- `<em>` (Emphasized)
*These tags visually look identical to bold and italics... BUT they also inject semantic code. Deepanshu ensures that when a screen reader hits a `<strong>` tag, the robot voice physically changes its inflection to sound louder and more urgent!*

**Golden Rule:** Always use `<strong>` and `<em>` instead of `<b>` and `<i>`!

---

## 2. Text Modification and Highlighting

Sometimes you need to show that a document has been edited, or to highlight a search result.

- **`<mark>`**: Literally acts like a yellow highlighter pen. Excellent for highlighting query matches in search results!
- **`<del>`**: (Deleted text). Draws a line straight through the word (strikethrough).
- **`<ins>`**: (Inserted text). Draws an underline beneath the word.

```html
<!-- Jay is tracking document edits! -->
<p>The meeting is on <del>Monday</del> <ins>Tuesday</ins>.</p>
```
*Why this matters: If you just use CSS to draw a line through "Monday", a search engine might still index the meeting as being on Monday. By using `<del>`, you explicitly tell Google's algorithm that the text is no longer valid!*

---

## 3. Math and Science Typography

If you are displaying chemical formulas or algebra, you absolutely need to shift the physical baseline of the characters.

- **`<sub>` (Subscript)**: Drops the text half a character downward. (e.g., $H_2O$)
- **`<sup>` (Superscript)**: Raises the text half a character upward. (e.g., $X^2$)

```html
<p>Aakash wrote the formula for water: H<sub>2</sub>O.</p>
<p>Kunal squared the number: 10<sup>2</sup> = 100.</p>
```

These are essential because simply shrinking the font size and moving it with CSS is wildly inaccurate across different browsers. `<sub>` and `<sup>` are mathematically locked to the document's typography baseline!




---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
