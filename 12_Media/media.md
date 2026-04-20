# 12 - Media Elements & Iframes (Class Notes)

## The Native Player Revolution

Before HTML5, embedding a video on a webpage was an absolute nightmare. Developers had to use buggy third-party plugins like Adobe Flash just to play a simple video. 

Today, `<video>` and `<audio>` are baked natively right into the core of the web browser. 

---

## 1. Native Controls vs Custom APIs

If you simply type `<video src="vid.mp4"></video>`, the video will load, but it **will not play**. There is no play button!

- **The Easy Way:** Adding the `controls` boolean attribute. This forces the browser (Chrome, Firefox, Safari) to auto-generate a native play/pause/volume interface for you instantly. Every browser's interface looks totally different.
- **The Advanced Way:** Deepanshu completely strips away the `controls` attribute, hiding the native interface. He then builds custom slick buttons using standard HTML and CSS, and ties them to the video using the native JavaScript `HTMLMediaElement` API to perfectly customize his player's branding!

---

## 2. Redundant Source Code Engine

Why do we sometimes see `<source>` tags stuffed inside a `<video>` tag instead of just using the standard `src=""` attribute?

Because browser companies are fundamentally at war over file codecs! Apple Safari prefers `.mov` files, while Google Chrome prefers `.webm` files.

**The Solution:**
Kunal solves this by stacking multiple sources in a row. The browser's engine will read from the top down. If it can't read the first file format natively, it silently skips to the second one!

```html
<video controls width="500">
    <!-- Chrome plays this instantly and ignores the others -->
    <source src="movie.webm" type="video/webm">
    <!-- Safari fails the webm, so it drops down and plays this instead! -->
    <source src="movie.mp4" type="video/mp4">
    <!-- The ultimate fallback error message -->
    Your browser is ancient and cannot play modern video files.
</video>
```

---

## 3. The Incredible (`Iframes`) & Web Security

An `<iframe>` (Inline Frame) acts like a literal window cut out of your webpage, looking directly at another completely separate website.

It is universally how we embed Google Maps, Spotify players, and YouTube videos into personal portfolios. It offloads all the heavy video downloading onto Google's massive global servers instead of our tiny personal servers!

### Iframe Sandboxing (Advanced Security)

When you cut a window into another website on your own homepage, what stops that other website from firing malicious JavaScript popups or logging into your user's accounts?

**The `sandbox` attribute!**

```html
<!-- Safely isolating an external window -->
<iframe src="https://example.com" sandbox="allow-scripts allow-same-origin"></iframe>
```
Gagan explains that using `sandbox` throws the external window into a literal digital prison cell. They cannot run plugins, open popups, or execute top-level scripts unless you explicitly declare it in the attribute whitelist!




---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
