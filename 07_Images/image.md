# 07 - Advanced Image Architecture (Class Notes)

## The Evolution of the `<img>` Tag

Embedding an image seems simple enough, but managing images is actually one of the hardest parts of modern web engineering. Heavy images are the #1 reason websites load slowly or crash on mobile phones!

**The Golden Syntax:**
`<img src="URL" alt="Description">`
*(Remember: Images are "Void Elements," meaning they do not get a closing `</img>` tag!)*

---

## 1. The Critical `alt` Attribute (A11y & SEO)

Aakash reminds everyone: if you forget the `alt` (Alternate Text) attribute, your code is fundamentally broken.

- **For Screen Readers:** If Khushi is visually impaired, the screen reader cannot see the photo. It will read the `alt` text aloud instead.
- **For Broken Links:** If the server crashes and the image won't load, the `alt` text is physically displayed in the broken box so the user still has context.
- **For Google Bots:** Search engine algorithms cannot "look" at JPEGs. They strictly read your `alt` text to figure out what the image actually is so they can rank it in Google Images!

---

## 2. Beating Cumulative Layout Shift (CLS)

Have you ever been reading a news article on your phone, and suddenly an image loads in and pushes all the text down, causing you to tap the wrong button? That jarring glitch is called **Cumulative Layout Shift (CLS)**.

**How to stop it:**
You must *always* explicitly declare the `width` and `height` of an image in the HTML!

```html
<!-- The browser instantly reserves a 500x300 empty box before the image even finishes downloading! -->
<img src="heavy_photo.jpg" width="500" height="300" alt="Landscape">
```
*Advanced Note: When you declare the dimensions manually, the browser mathematically reserves that exact amount of whitespace on the screen immediately. When the image finally finishes downloading, it pops perfectly into the pre-made slot without shifting the text around it!*

---

## 3. Advanced Loading Mechanics (Lazy Loading)

By default, if you have 100 images on a single web page, the browser will desperately try to download all 100 of them the second you open the page, instantly freezing your computer.

HTML5 introduced an incredibly powerful native hook called **Lazy Loading**!

```html
<!-- This image won't even start downloading until the user actually scrolls down to look at it! -->
<img src="bottom_photo.jpg" loading="lazy" alt="Footer map">
```

Charv suggests adding `loading="lazy"` to every image that isn't instantly visible at the very top of the screen. It can speed up your website's initial load time by thousands of percent!





---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
