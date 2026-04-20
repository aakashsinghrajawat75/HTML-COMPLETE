# HTML5 — Complete Engineering Reference

> HTML is not just a markup language. It is the universal contract between the human who writes the code, the browser that interprets it, and the search engine that indexes it.  
> This repository documents all 18 stages of that contract — from the very first `<!DOCTYPE html>` declaration all the way to native browser GPU rendering APIs.

---

## Repository Architecture

```text
HTML-complete/
├── 01_Basics/                    # DOCTYPE, document shell anatomy, head vs body, comments
├── 02_Elements/                  # Tag structure, DOM Tree nodes, void elements, nesting law
├── 03_Attributes/                # Global vs specific attrs, boolean attrs, data-* hooks
├── 04_Headings_and_Paragraphs/   # Semantic outline, SEO impact, whitespace engine, pre tag
├── 05_Formatting/                # Visual tags vs semantic tags, <del> indexing, sub/sup
├── 06_Styles/                    # Inline CSS, specificity hierarchy, rem vs px units
├── 07_Images/                    # alt text (A11y + SEO), Cumulative Layout Shift, lazy load
├── 08_Tables/                    # Grid semantics, thead/tbody/tfoot, colspan, scope attr
├── 09_Lists/                     # Nav menus, ol counters, legal nesting rules
├── 10_Blocks_and_Classes/        # Block vs inline rendering, Div Soup, BEM methodology
├── 11_Forms/                     # GET vs POST (HTTP), id vs name, label binding, native validation
├── 12_Media/                     # Native players, codec fallback stacks, iframe sandboxing (XSS)
├── 13_Semantic_HTML/             # Machine readability, article vs section, aside, WCAG zones
├── 14_Entities_and_Symbols/      # Escape sequences, XSS attack vector, nbsp line-binding
├── 15_Data_Attributes/           # data-* separation of concerns, JS bridge hooks, valid HTML
├── 16_Accessibility_A11y/        # ARIA roles, aria-live, tabindex=-1 modal traps
├── 17_Advanced_Head_and_SEO/     # Viewport, OG + Twitter Cards, CSP whitelists, Schema.org JSON-LD
└── 18_HTML5_Graphics_and_APIs/   # SVG math vs Canvas pipeline, Geolocation, Web Storage, Notifications
```

---

## Learning Path — What This Repository Actually Teaches

This guide is split into three distinct engineering layers. Don't skip ahead — each layer builds the mental model needed for the next one.

### Layer 1 — Document Foundations (Modules 01–03)
Understanding *what* HTML actually is at the rendering-engine level. The difference between a tag, an element, and a DOM node. How attribute name/value pairs get parsed by the browser's tokenizer.

### Layer 2 — Content Engineering (Modules 04–13)
Building real web content the way a professional does. The key insight of this layer: every single HTML decision has three consequences — visual layout, search engine ranking, and accessibility impact. Most beginners only think about the first one.

### Layer 3 — Platform Engineering (Modules 14–18)
This is where HTML stops being a "beginner" language and becomes a sophisticated application platform. Entities for XSS prevention. Data attributes for JavaScript framework bridges. CSP headers for blocking hacker-injected scripts. JSON-LD for Google Rich Results. The SVG vs Canvas rendering pipeline decision. Native hardware APIs for GPS, push notifications, and persistent storage.

---

## Module Reference

### 01 — HTML Basics
*DOCTYPE declaration, browser parsing engine, metadata vs body, UTF-8 charset, SEO title tag*
| File | What it demonstrates |
|------|----------------------|
| `01_intro.html` | The minimal valid HTML5 boilerplate with every required line explained |
| `02_head_anatomy.html` | What lives in `<head>` and why it's invisible to the user but critical to machines |
| `03_comments.html` | Code comments as debugging tools — commenting out broken code without deleting it |

### 02 — Elements & The DOM
*Tag anatomy, DOM tree parent/child/sibling hierarchy, void elements, the Russian Doll nesting law*
| File | What it demonstrates |
|------|----------------------|
| `01_elements.html` | The difference between a tag and a full element (opening + content + closing) |
| `02_nested_elements.html` | Correct nesting order — why first-in must be last-out |
| `03_empty_elements.html` | Void elements: `<br>`, `<hr>`, `<img>`, `<meta>` — no closing tag, no content |

### 03 — Attributes
*Global vs element-specific attributes, boolean attributes, data-* custom hooks*
| File | What it demonstrates |
|------|----------------------|
| `01_href_attribute.html` | Hypertext references — absolute URLs, relative paths, anchor jumps |
| `02_src_and_alt_attributes.html` | Image sourcing and why missing `alt` breaks both accessibility and SEO |
| `03_core_attributes.html` | `id`, `class`, `title` — identifiers, grouping, and mouse-hover tooltips |

### 04 — Headings & Paragraphs
*Semantic document outline, Google crawler behavior, User Agent stylesheet, whitespace collapsing*
| File | What it demonstrates |
|------|----------------------|
| `01_headings.html` | The h1–h6 heading hierarchy — only one `<h1>` per page, never skip levels |
| `02_paragraphs.html` | Why `<p>` auto-spaces itself (User Agent stylesheet built into every browser) |
| `03_whitespace.html` | The collapsing rule — why 50 spaces in your code render as 1 space on screen |
| `04_preformatted_text.html` | `<pre>` forces the browser to respect every space and line break you type |

### 05 — Text Formatting
*Semantic vs visual tags, screen reader inflection, `<del>` and search engine de-indexing*
| File | What it demonstrates |
|------|----------------------|
| `01_bold_and_italics.html` | `<b>`/`<i>` (visual only) vs `<strong>`/`<em>` (semantic + visual) |
| `02_mark_and_small.html` | `<mark>` for search result highlighting, `<small>` for legal disclaimers |
| `03_deleted_and_inserted.html` | `<del>` tells Google the content is invalid — not just visually struck out |
| `04_subscript_and_superscript.html` | Mathematically locked baseline positioning for H₂O and X² formulas |

### 06 — Inline Styles
*CSS specificity hierarchy, inline vs external stylesheet priority, rem vs px unit theory*
| File | What it demonstrates |
|------|----------------------|
| `01_colors.html` | `color` (foreground) and `background-color` applied at element level |
| `02_fonts_and_sizes.html` | `font-family` typefaces, and `px` vs `%` vs `rem` scaling units |
| `03_alignment.html` | `text-align: justify` — how news articles stretch word spacing to flush margins |

### 07 — Images
*`alt` text for A11y and Google Image ranking, Cumulative Layout Shift (CLS) prevention, lazy loading*
| File | What it demonstrates |
|------|----------------------|
| `01_image_basics.html` | `src` (location) and `alt` (fallback text and screen reader description) |
| `02_image_dimensions.html` | Declaring `width` and `height` to pre-reserve DOM space and eliminate CLS |
| `03_linking_images.html` | Nesting `<img>` inside `<a>` to make the entire image a clickable button |

### 08 — Data Tables
*Grid semantics, semantic section wrappers, colspan/rowspan, `scope` for accessible data grids*
| File | What it demonstrates |
|------|----------------------|
| `01_basic_table.html` | The minimum: `<table>`, `<tr>`, `<th>`, `<td>` |
| `02_table_structure.html` | `<thead>`, `<tbody>`, `<tfoot>` — why browsers auto-repeat `<thead>` on printed pages |
| `03_spanning.html` | `colspan` destroys column walls, `rowspan` destroys row floors |

### 09 — Lists & Navigation
*The hidden secret: `<ul>` builds nav menus, `ol` counter manipulation, legal nesting rules*
| File | What it demonstrates |
|------|----------------------|
| `01_unordered_lists.html` | `<ul>` bullet points — and why this same tag builds website nav menus in CSS |
| `02_ordered_lists.html` | Numbered sequences — `start="5"` and `reversed` attribute for countdowns |
| `03_description_lists.html` | `<dl>`, `<dt>`, `<dd>` — dictionary and glossary structure |

### 10 — Blocks & Classes
*Browser rendering engine behavior, The Div Soup epidemic, BEM multi-class chaining methodology*
| File | What it demonstrates |
|------|----------------------|
| `01_block_vs_inline.html` | Block: stretches full 100% width. Inline: only wraps its exact content width |
| `02_div_and_span.html` | `<div>` = invisible block container. `<span>` = invisible inline wrapper |
| `03_class_and_id.html` | `id` for unique targeting, `class` for reusable group styling |

### 11 — Forms & HTTP
*GET vs POST method security, `id` vs `name` (frontend vs backend), label binding, native HTML5 validation*
| File | What it demonstrates |
|------|----------------------|
| `01_form_basics.html` | `action`, `method`, text/email/password input types |
| `02_radio_and_checkbox.html` | Radio buttons (single selection) and checkboxes (multi-selection) |
| `03_select_and_textarea.html` | `<select>` dropdowns with `<option>` values and `<textarea>` for large input |

### 12 — Media & Iframes
*Native browser media players, codec fallback stacks, iframe sandbox security isolation*
| File | What it demonstrates |
|------|----------------------|
| `01_video_element.html` | `<video controls>` renders native browser playback UI |
| `02_audio_element.html` | `<audio>` with `<source>` fallback stack for cross-browser codec support |
| `03_iframe_element.html` | `<iframe sandbox>` cuts a secure window into another website |

### 13 — Semantic HTML
*Machine-readable page zones, `<article>` independence rule, `<aside>` skip logic, WCAG zone compliance*
| File | What it demonstrates |
|------|----------------------|
| `01_semantic_meaning.html` | Non-semantic (div soup) vs semantic structure side-by-side |
| `02_header_nav_footer.html` | The outer shell: `<header>`, `<nav>`, `<footer>` |
| `03_main_article_section.html` | Core content: `<main>` (only one allowed), `<article>`, `<section>` |

### 14 — HTML Entities
*Escape sequences for reserved tokens, XSS attack vector prevention, `&nbsp;` line-binding*
| File | What it demonstrates |
|------|----------------------|
| `01_reserved_characters.html` | `&lt;`, `&gt;`, `&amp;` — rendering HTML code as plain visible text |
| `02_special_symbols.html` | `&nbsp;` (non-breaking space), `&copy;`, `&trade;`, `&rarr;` arrows |

### 15 — Data Attributes
*HTML5 custom `data-*` hooks, separation of CSS vs logic concerns, JavaScript framework bridge*
| File | What it demonstrates |
|------|----------------------|
| `01_data_attributes.html` | Attaching invisible machine-readable data to visible DOM nodes |

### 16 — Web Accessibility
*ARIA role overrides, `aria-live` for live notifications, `tabindex=-1` for hidden modal components*
| File | What it demonstrates |
|------|----------------------|
| `01_aria_and_tabindex.html` | `role="button"`, `aria-pressed`, and custom `tabindex` keyboard routing |

### 17 — Advanced `<head>` & SEO
*Viewport rendering, Open Graph + Twitter Card protocols, Content Security Policy, Schema.org JSON-LD*
| File | What it demonstrates |
|------|----------------------|
| `01_opengraph_and_csp.html` | OG tags for social media previews and CSP directive whitelisting |

### 18 — HTML5 Graphics & Native APIs
*SVG math rendering vs Canvas pixel pipeline, Geolocation GPS hook, Web Storage vs Cookies, Notification API*
| File | What it demonstrates |
|------|----------------------|
| `01_canvas_and_svg.html` | SVG (infinite resolution math shapes) vs Canvas (mass pixel rendering for games) |

---

## How to Run

1. No compiler. No build system. No Node.js. HTML is interpreted natively by the browser.
2. Double-click any `.html` file → your default browser opens it instantly.
3. Right-click anywhere on the rendered page → **View Page Source** to see the raw code.
4. In VSCode, install the **Live Server** extension → right-click any `.html` file → **Open with Live Server**. Every time you save a change, the browser auto-refreshes in real time!

---

## Requirements

| Requirement | Details |
|------------|---------|
| Text Editor | VSCode (recommended), Notepad++, Sublime Text |
| Browser | Google Chrome, Firefox, Edge, or Safari |
| Internet | Not required (except for `<iframe>` and external CDN assets) |
| Terminal | Not required for HTML — use it optionally for Git version control |

---

## Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
