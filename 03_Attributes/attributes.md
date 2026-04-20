# 03 - HTML Attributes (Class Notes)

## What are Attributes?

If elements are the "nouns" of HTML, attributes are the "adjectives." They provide extra instructions and data to the browser about how a specific element should behave or look.

**The Golden Syntax Rule:**
Attributes *always* go inside the **Opening Tag**. You never put them in the closing tag. They are almost always formatted as name/value pairs: `name="value"`.

```html
<a href="https://example.com" class="button">Click Me!</a>
```

---

## 1. Global vs. Specific Attributes

Not all tags can use all attributes! You need to know the difference between Global and Specific attributes.

### Global Attributes (Can be used on almost ANY tag)
- **`class`**: Used to group elements together so you can style them all at once in CSS. (e.g., `<p class="highlight">`)
- **`id`**: Used to pinpoint one *entirely unique* element on the page. You should never use the same ID twice on a single webpage! (e.g., `<nav id="main-menu">`)
- **`style`**: Allows you to inject raw CSS styling directly into the element. (e.g., `<h1 style="color: red;">`)
- **`title`**: Creates a cool little tooltip that appears when a user hovers their mouse over the element.

### Specific Attributes (Can only be used on SPECIFIC tags)
- **`href`**: Stands for "Hypertext Reference". Only works on anchor tags (`<a>`) to tell them where to jump to.
- **`src`**: Stands for "Source". Only works on media tags like `<img>` or `<video>` to tell them where the file is located.
- **`alt`**: An alternate text description physically required on `<img>` tags for blind users using screen readers.

---

## 2. Boolean Attributes (Advanced Quirk)

Here is a weird exception: Some attributes don't need a value (no equals sign, no quotes). We call these **Boolean Attributes**. They are like a light switch—if the attribute is there, it's turned ON. If it's deleted, it's turned OFF.

```html
<!-- The 'disabled' attribute is a boolean! -->
<button disabled>You cannot click me</button>

<!-- The 'required' attribute is a boolean! -->
<input type="text" required>
```
*Note: In the background, the browser reads `<button disabled>` as exactly the same thing as `<button disabled="true">`.*

---

## 3. The Custom Data Hook (`data-*`)

What happens when you need to store custom backend database info (like a User ID) directly onto an HTML element so JavaScript can read it later? You shouldn't misuse an `id` or `class` for that.

HTML5 gave us the custom `data-*` attribute!

```html
<!-- JavaScript can easily scan this and pull out the number 101 secretly -->
<li data-user-id="101">Aakash (CGPA: 9.0)</li>
```
**Pro Tip from Kunal:** You can name it whatever you want (`data-secret-code`, `data-favorite-color`), as long as it starts exactly with `data-`. This is how modern web apps actually pass data between HTML and JavaScript!




---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
