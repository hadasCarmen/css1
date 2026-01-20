# HTML Cheatsheet

## Table of Contents
- [Basic Structure](#basic-structure)
- [Document Metadata](#document-metadata)
- [Text Content](#text-content)
- [Semantic HTML5 Tags](#semantic-html5-tags)
- [Lists](#lists)
- [Links & Media](#links--media)
- [Tables](#tables)
- [Forms](#forms)
- [Inline Elements](#inline-elements)
- [Formatting Tags](#formatting-tags)
- [Embedded Content](#embedded-content)
- [Niche & Special Tags](#niche--special-tags)

---

## Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

---

## Document Metadata

```html
<!-- Character encoding -->
<meta charset="UTF-8">

<!-- Viewport for responsive design -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- SEO meta tags -->
<meta name="description" content="Page description">
<meta name="keywords" content="html, css, javascript">
<meta name="author" content="Your Name">

<!-- Favicon -->
<link rel="icon" type="image/x-icon" href="favicon.ico">

<!-- External CSS -->
<link rel="stylesheet" href="styles.css">

<!-- External JavaScript -->
<script src="script.js"></script>
```

---

## Text Content

```html
<!-- Headings (h1 to h6) -->
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Sub-subheading</h3>
<h4>Level 4 Heading</h4>
<h5>Level 5 Heading</h5>
<h6>Level 6 Heading</h6>

<!-- Paragraphs -->
<p>This is a paragraph of text.</p>

<!-- Line break -->
<br>

<!-- Horizontal rule -->
<hr>

<!-- Preformatted text -->
<pre>
    This text preserves
    spaces and line breaks
</pre>

<!-- Block quote -->
<blockquote cite="https://example.com">
    This is a quotation from somewhere.
</blockquote>

<!-- Division (block container) -->
<div>Block-level container</div>

<!-- Span (inline container) -->
<span>Inline container</span>
```

---

## Semantic HTML5 Tags

```html
<!-- Page header -->
<header>
    <h1>Website Title</h1>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
        </ul>
    </nav>
</header>

<!-- Navigation -->
<nav>
    <a href="#section1">Section 1</a>
    <a href="#section2">Section 2</a>
</nav>

<!-- Main content -->
<main>
    <!-- Article (self-contained content) -->
    <article>
        <h2>Article Title</h2>
        <p>Article content...</p>
    </article>
    
    <!-- Section (thematic grouping) -->
    <section>
        <h2>Section Title</h2>
        <p>Section content...</p>
    </section>
    
    <!-- Aside (sidebar content) -->
    <aside>
        <h3>Related Links</h3>
        <p>Sidebar content...</p>
    </aside>
</main>

<!-- Footer -->
<footer>
    <p>&copy; 2026 Your Website</p>
</footer>

<!-- Figure with caption -->
<figure>
    <img src="image.jpg" alt="Description">
    <figcaption>Image caption</figcaption>
</figure>

<!-- Details/Summary (collapsible) -->
<details>
    <summary>Click to expand</summary>
    <p>Hidden content here</p>
</details>

<!-- Mark (highlighted text) -->
<p>This is <mark>highlighted</mark> text.</p>

<!-- Time element -->
<time datetime="2026-01-18">January 18, 2026</time>
```

---

## Lists

```html
<!-- Unordered list -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Ordered list -->
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>

<!-- Description list -->
<dl>
    <dt>Term 1</dt>
    <dd>Definition 1</dd>
    <dt>Term 2</dt>
    <dd>Definition 2</dd>
</dl>

<!-- Nested lists -->
<ul>
    <li>Item 1
        <ul>
            <li>Subitem 1.1</li>
            <li>Subitem 1.2</li>
        </ul>
    </li>
    <li>Item 2</li>
</ul>
```

---

## Links & Media

```html
<!-- Anchor (link) -->
<a href="https://example.com">External Link</a>
<a href="#section">Internal Link</a>
<a href="mailto:email@example.com">Email Link</a>
<a href="tel:+1234567890">Phone Link</a>
<a href="file.pdf" download>Download File</a>
<a href="https://example.com" target="_blank">Open in New Tab</a>

<!-- Image -->
<img src="image.jpg" alt="Description" width="300" height="200">

<!-- Audio -->
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Your browser does not support audio.
</audio>

<!-- Video -->
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Your browser does not support video.
</video>

<!-- Picture (responsive images) -->
<picture>
    <source media="(min-width: 650px)" srcset="large.jpg">
    <source media="(min-width: 465px)" srcset="medium.jpg">
    <img src="small.jpg" alt="Description">
</picture>

<!-- Iframe -->
<iframe src="https://example.com" width="600" height="400"></iframe>
```

---

## Tables

```html
<!-- Basic table -->
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>

<!-- Table with sections -->
<table>
    <caption>Table Title</caption>
    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>John</td>
            <td>30</td>
        </tr>
        <tr>
            <td>Jane</td>
            <td>25</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Total</td>
            <td>2 people</td>
        </tr>
    </tfoot>
</table>

<!-- Colspan and Rowspan -->
<table>
    <tr>
        <th colspan="2">Merged Columns</th>
    </tr>
    <tr>
        <td rowspan="2">Merged Rows</td>
        <td>Cell 1</td>
    </tr>
    <tr>
        <td>Cell 2</td>
    </tr>
</table>

<!-- Accessible table -->
<table>
    <tr>
        <th scope="col">Column Header</th>
        <th scope="col">Column Header</th>
    </tr>
    <tr>
        <th scope="row">Row Header</th>
        <td>Data</td>
    </tr>
</table>
```

---

## Forms

```html
<!-- Basic form -->
<form action="/submit" method="POST">
    <!-- Text input -->
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <!-- Email input -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <!-- Password -->
    <label for="password">Password:</label>
    <input type="password" id="password" name="password">
    
    <!-- Number -->
    <input type="number" min="0" max="100" step="5">
    
    <!-- Date -->
    <input type="date" name="birthday">
    
    <!-- Radio buttons -->
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
    
    <!-- Checkbox -->
    <input type="checkbox" id="subscribe" name="subscribe">
    <label for="subscribe">Subscribe to newsletter</label>
    
    <!-- Dropdown -->
    <label for="country">Country:</label>
    <select id="country" name="country">
        <option value="">Select...</option>
        <option value="us">USA</option>
        <option value="uk">UK</option>
    </select>
    
    <!-- Textarea -->
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50"></textarea>
    
    <!-- File upload -->
    <input type="file" name="upload" accept="image/*">
    
    <!-- Range -->
    <input type="range" min="0" max="100" value="50">
    
    <!-- Color picker -->
    <input type="color" name="favcolor" value="#ff0000">
    
    <!-- Submit button -->
    <button type="submit">Submit</button>
    <input type="submit" value="Submit">
    
    <!-- Reset button -->
    <button type="reset">Reset</button>
</form>

<!-- Fieldset and Legend -->
<fieldset>
    <legend>Personal Information</legend>
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname">
</fieldset>

<!-- Datalist (autocomplete) -->
<input list="browsers" name="browser">
<datalist id="browsers">
    <option value="Chrome">
    <option value="Firefox">
    <option value="Safari">
</datalist>
```

---

## Inline Elements

```html
<!-- Strong (important text) -->
<strong>Bold/Important text</strong>

<!-- Emphasis -->
<em>Italic/Emphasized text</em>

<!-- Bold (visual only) -->
<b>Bold text</b>

<!-- Italic (visual only) -->
<i>Italic text</i>

<!-- Underline -->
<u>Underlined text</u>

<!-- Small text -->
<small>Small print</small>

<!-- Strikethrough -->
<s>Strikethrough text</s>
<del>Deleted text</del>

<!-- Inserted text -->
<ins>Inserted text</ins>

<!-- Subscript -->
<p>H<sub>2</sub>O</p>

<!-- Superscript -->
<p>x<sup>2</sup></p>

<!-- Code -->
<code>console.log('Hello');</code>

<!-- Keyboard input -->
<kbd>Ctrl</kbd> + <kbd>C</kbd>

<!-- Sample output -->
<samp>Error: File not found</samp>

<!-- Variable -->
<var>x</var> = 5

<!-- Abbreviation -->
<abbr title="HyperText Markup Language">HTML</abbr>

<!-- Citation -->
<cite>The Great Gatsby</cite>

<!-- Quote (inline) -->
<q>This is a short quote</q>
```

---

## Formatting Tags

```html
<!-- Address -->
<address>
    Written by John Doe.<br>
    Visit us at: example.com<br>
    USA
</address>

<!-- Definition -->
<dfn>HTML</dfn> is a markup language.

<!-- Ruby annotation (East Asian) -->
<ruby>
    漢 <rt>kan</rt>
</ruby>

<!-- Bi-directional override -->
<bdo dir="rtl">This text will go right to left</bdo>

<!-- Bi-directional isolation -->
<bdi>User input text</bdi>

<!-- Word break opportunity -->
<p>This is a very<wbr>longword<wbr>example</p>
```

---

## Embedded Content

```html
<!-- Embed external content -->
<embed src="file.pdf" width="500" height="600">

<!-- Object -->
<object data="file.pdf" type="application/pdf" width="500" height="600">
    Alternative text
</object>

<!-- Canvas (for graphics) -->
<canvas id="myCanvas" width="200" height="100"></canvas>

<!-- SVG -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" fill="red" />
</svg>

<!-- MathML (mathematical formulas) -->
<math>
    <mrow>
        <mi>x</mi>
        <mo>=</mo>
        <mn>5</mn>
    </mrow>
</math>
```

---

## Niche & Special Tags

```html
<!-- Dialog (modal) -->
<dialog open>
    <p>This is a dialog box</p>
    <button>Close</button>
</dialog>

<!-- Progress bar -->
<progress value="70" max="100">70%</progress>

<!-- Meter (gauge) -->
<meter value="6" min="0" max="10">6 out of 10</meter>

<!-- Output (calculation result) -->
<output name="result">0</output>

<!-- Base URL -->
<base href="https://example.com/" target="_blank">

<!-- Noscript (fallback) -->
<noscript>JavaScript is required for this site.</noscript>

<!-- Template (hidden content) -->
<template id="myTemplate">
    <p>This is template content</p>
</template>

<!-- Track (for video/audio) -->
<video controls>
    <source src="video.mp4" type="video/mp4">
    <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
</video>

<!-- Data element -->
<data value="12345">Product Code</data>

<!-- Portal (experimental) -->
<portal src="https://example.com"></portal>

<!-- Slot (for Web Components) -->
<slot name="header"></slot>

<!-- Map (image map) -->
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
<map name="workmap">
    <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
    <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map>

<!-- Col and Colgroup (table columns) -->
<table>
    <colgroup>
        <col span="2" style="background-color:red">
        <col style="background-color:yellow">
    </colgroup>
    <tr>
        <td>Data</td>
        <td>Data</td>
        <td>Data</td>
    </tr>
</table>

<!-- Optgroup (grouped options) -->
<select>
    <optgroup label="Fruits">
        <option value="apple">Apple</option>
        <option value="banana">Banana</option>
    </optgroup>
    <optgroup label="Vegetables">
        <option value="carrot">Carrot</option>
        <option value="lettuce">Lettuce</option>
    </optgroup>
</select>
```

---

## HTML Entities (Special Characters)

```html
&lt;    <!-- < -->
&gt;    <!-- > -->
&amp;   <!-- & -->
&quot;  <!-- " -->
&apos;  <!-- ' -->
&nbsp;  <!-- non-breaking space -->
&copy;  <!-- © -->
&reg;   <!-- ® -->
&trade; <!-- ™ -->
&euro;  <!-- € -->
&cent;  <!-- ¢ -->
&pound; <!-- £ -->
&yen;   <!-- ¥ -->
```

---

## Comments

```html
<!-- This is a single line comment -->

<!--
    This is a
    multi-line comment
-->
```

---

## HTML5 Input Types

```html
<input type="text">
<input type="email">
<input type="password">
<input type="number">
<input type="tel">
<input type="url">
<input type="search">
<input type="date">
<input type="time">
<input type="datetime-local">
<input type="month">
<input type="week">
<input type="color">
<input type="range">
<input type="file">
<input type="checkbox">
<input type="radio">
<input type="submit">
<input type="reset">
<input type="button">
<input type="hidden">
```

---

## Global Attributes (Work on any HTML element)

```html
<!-- ID (unique identifier) -->
<div id="unique-id"></div>

<!-- Class (for styling/grouping) -->
<div class="class-name another-class"></div>

<!-- Style (inline CSS) -->
<p style="color: red; font-size: 16px;">Text</p>

<!-- Title (tooltip) -->
<p title="This is a tooltip">Hover over me</p>

<!-- Data attributes (custom data) -->
<div data-user-id="12345" data-role="admin"></div>

<!-- Contenteditable -->
<div contenteditable="true">Edit this text</div>

<!-- Draggable -->
<div draggable="true">Drag me</div>

<!-- Hidden -->
<div hidden>This is hidden</div>

<!-- Spellcheck -->
<textarea spellcheck="true"></textarea>

<!-- Tabindex (keyboard navigation) -->
<div tabindex="0">Focusable element</div>

<!-- Lang (language) -->
<p lang="es">Hola Mundo</p>

<!-- Dir (text direction) -->
<p dir="rtl">Right to left text</p>

<!-- Translate -->
<p translate="no">Don't translate this</p>

<!-- Accesskey (keyboard shortcut) -->
<button accesskey="s">Save</button>
```

---

**Remember:** Always use semantic HTML for better accessibility and SEO! 🚀
