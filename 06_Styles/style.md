# 06 - Inline Styles (Class Notes)

## What is the `style` Attribute?

HTML dictates structure. CSS dictates visual style. 

Usually, professional developers write all their CSS in a completely separate file. However, you can inject CSS directly into a specific HTML tag using the **`style`** attribute. We call this **"Inline Styling."**

**The Syntax Rule:**
You must write CSS rules inside the quotes as a `property` paired with a `value`, separated by a colon, and ending with a semicolon.
`<tagname style="property: value;">`

```html
<!-- Example of injecting CSS directly into a paragraph block -->
<p style="color: blue; text-align: center;">This text is blue and centered.</p>
```

---

## 1. The Power of "Specificity"

Why do Advanced Developers care about Inline Styles? Because of **Specificity**.

Browsers follow a strict hierarchy when deciding what color to paint an element.
1. **Low Priority**: External CSS files.
2. **Medium Priority**: CSS written in the `<head>` of the document.
3. **Absolute Highest Priority**: Inline Styles (the `style` attribute).

If your main CSS file says all paragraphs must be black, but you write `<p style="color: red;">`, the text will turn red! Inline styles utterly crush all other styling rules on the page. Khushi warns: Use inline styles sparingly, otherwise they become impossible to override later!

---

## 2. Advanced Typography Sizing

When you change the `font-size` of text, you have to attach a unit of measurement. Beginners usually jump straight to pixels, but advanced developers use relative units!

- **`px` (Pixels)**: Highly exact, but completely rigid. (e.g., `font-size: 24px;`). If a visually impaired user zooms their browser in, pixel-fonts often refuse to scale up properly!
- **`%` (Percentages)**: Scales the text relative to the parent box perfectly. (e.g., `font-size: 150%;`).
- **`rem` (Root Em)**: The ultimate modern unit. `1rem` equals the default browser font size (usually 16px). If you write `font-size: 2rem;`, the text will safely double in size and still scale perfectly on mobile phones or accessibility screen readers!

```html
<p style="font-size: 1.5rem;">Daulat wrote this responsive sizing paragraph.</p>
```

---

## 3. Structural Alignment

By default, text aligns to the left edge of its container. You can manipulate the internal flow of the block using `text-align`.

- `text-align: center;` (Pushes the text to the exact middle).
- `text-align: right;` (Pinches the text against the right margin).
- `text-align: justify;` (A very advanced trick used by news articles! It mathematically stretches the spaces between words so that both the left and right edges lock perfectly flat against the margins of the page).





---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
