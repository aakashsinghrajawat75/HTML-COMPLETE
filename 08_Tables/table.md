# 08 - Data Tables (Class Notes)

## The Great Table Layout War

In the 1990s and early 2000s, web developers actually used the `<table>` tag to design entire website layouts! They would slice graphics into hundreds of tiny squares and map them perfectly into invisible table grids. 
**Modern HTML5 strictly forbids this.** 
Today, we use CSS (Grid/Flexbox) to build website layouts. The `<table`> tag is now exclusively reserved for **Tabular Data**—meaning literal data spreadsheets, schedules, and statistical reports.

---

## 1. Building the Data Grid

A table is constructed like an onion, nesting containers inside containers.

- **`<table>`**: The supreme wrapper. Nothing related to the table can exist outside this tag.
- **`<tr>` (Table Row)**: Defines a horizontal slice across the grid.
- **`<th>` (Table Heading)**: Represents a column header. It auto-centers and auto-bolds the text.
- **`<td>` (Table Data)**: The actual data cell holding the information.

### Advanced Structural Semantics
Just as a webpage gets divided into a header, main, and footer, a proper data table should be semantically divided for screen readers and advanced data-scraping bots!
- **`<thead>`**: Wraps around all the top header `<tr>` rows.
- **`<tbody>`**: Wraps around the infinite loop of standard data rows. 
- **`<tfoot>`**: Wraps the very bottom summary row (like a "Total Overtime Hours" calculation).

*Deepanshu strongly recommends using these semantic wrappers because if your generic table data gets too long, printing the webpage will usually duplicate the `<thead>` at the top of every printed piece of physical paper automatically!*

---

## 2. Advanced Spanning 

Sometimes a piece of data is so important it needs to devour the cells next to it to stretch across the screen.

### `colspan` (Stretching Horizontally)
Destroys the wall between the current cell and the cells to its right.
```html
<!-- This single cell will stretch across the space of 3 standard columns! -->
<td colspan="3">Aakash's Yearly Report (Spans Q1, Q2, and Q3)</td>
```

### `rowspan` (Stretching Vertically)
Destroys the floor beneath the current cell, merging it with the rows underneath it.
```html
<!-- This cell reaches down to merge with the cell underneath it! -->
<td rowspan="2">Kunal's Double-Shift Signature</td>
```

---

## 3. The `scope` Attribute (Advanced Accessibility)

If you have a massive grid of data, a blind user's screen reader can easily get completely lost trying to figure out which data belongs to which column. We fix this by manually targeting the *scope* of our table headers!

```html
<!-- We explicitly tell the machine that this header controls the entire COLUMN dropping below it -->
<th scope="col">Student Name</th>

<!-- We tell the machine this header controls the entire ROW extending to the right of it -->
<th scope="row">Semester 1</th>
```
Jay points out: Visually, the `scope` attribute does absolutely nothing. But structurally, it binds the entire data grid together like mathematical iron!





---

## 👨‍💻 Author

> **Aakash**

> **GitHub: [aakashsinghrajawat75](https://github.com/aakashsinghrajawat75)**

---
