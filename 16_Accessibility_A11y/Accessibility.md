# 16 - Web Accessibility (A11y) (Class Notes)

## What is A11y?

A11y stands for Accessibility (There are 11 letters between the "A" and the "y"). It is the rigorous engineering discipline of modifying HTML code so that physically or visually impaired users can seamlessly interact with your application using Assistive Technologies like Screen Readers and Braille Keyboards.

It is so critical that in modern corporate software engineering, if your website fails WCAG (Web Content Accessibility Guidelines) logic standards, your company can physically be sued!

---

## 1. Modifying Base Tags with ARIA

Sometimes you don't use standard semantic HTML. Maybe you built a fancy dropdown menu out of generic `<div>` tags. A blind user's screen reader hits the `<div>` and assumes it's just a flat wall of text, completely ignoring your complex interaction code!

**The Solution: ARIA** (Accessible Rich Internet Applications).
ARIA attributes physically override the default behavior of your generic HTML, forcing the screen reader to treat them as custom components!

```html
<!-- We override the blind div, forcing the screen reader to announce this as a clickable Button! -->
<div role="button" aria-pressed="false">Submit Application</div>
```

Other massive Aria protocols:
- **`aria-hidden="true"`**: Completely strips the HTML element from the blind user's screen reader, hiding useless decorative UI elements so they don't have to listen to the robot read out an advertisement.
- **`aria-live="polite"`**: Forces the screen reader to pause what it's saying and immediately read out a live notification banner if one pops up on the screen dynamically!

---

## 2. Hijacking Keyboard Workflows (`tabindex`)

Many users with motor disabilities physically cannot use a computer mouse. They rely entirely on "Tabbing" through an entire website linearly using a keyboard.

By default, the browser jumps focus down the HTML page starting from line 1. But Jay explains we can manually override this jumping sequence using the advanced `tabindex`!

```html
<a href="#" tabindex="1">I will be the absolute first thing focused!</a>
<p tabindex="-1">I have been forcibly removed from the keyboard loop entirely!</p>
<a href="#" tabindex="0">I will just be slotted in naturally where the browser wants me.</a>
```

Advanced Hack: Giving a tag `tabindex="-1"` is how Deepanshu builds complex invisible Modals (popups). It ensures a keyboard user doesn't accidentally blindly tab onto a button they can't even see yet!




---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
