# CSS Units Lab: px, em, rem, vw, vh

## Introduction

Welcome to the CSS Units Lab! In this hands-on exercise, you'll learn about different CSS units and how they affect the size and spacing of elements on your webpage. Understanding these units is essential for creating responsive and accessible websites.

**Important:** This is a fill-in-the-blank lab. You'll see `___` placeholders in the CSS code where you need to add the correct measurements using the appropriate units (px, em, rem, vw, or vh). Read the instructions carefully for each section to determine which unit to use!

## Learning Objectives

By the end of this lab, you will be able to:
- Understand the difference between absolute and relative units
- Use px, em, rem, vw, and vh units effectively
- See how these units behave in real-world scenarios
- Make informed decisions about which unit to use

## Prerequisites

- Basic HTML knowledge
- Basic CSS knowledge (selectors, properties)
- A code editor (VS Code, Sublime Text, etc.)
- A web browser

---

## Part 1: Setup

Create a new folder called `css-units-lab` and inside it, create two files:
- `index.html`
- `styles.css`

### index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Units Lab</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Units Lab</h1>
    </header>

    <main>
        <!-- You'll add content here during the exercises -->
    </main>
</body>
</html>
```

---

## Part 2: Understanding px (Pixels)

**px** is an absolute unit. 1px is always 1px, regardless of parent elements or screen size.

### Exercise 2.1: Using Pixels

Add this HTML inside your `<main>` tag:

```html
<section class="px-section">
    <h2>Pixels (px)</h2>
    <div class="box px-box">200px × 200px</div>
    <p class="px-text">This text is 16px</p>
</section>
```

**Instructions:** Fill in the blanks below using **pixel (px)** values:
- Make the box exactly 200 pixels wide and 200 pixels tall
- Set the text size to 16 pixels
- Add 20 pixels of margin

Add this CSS to `styles.css`:

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: ___;  /* TODO: Add 20 pixels of padding */
}

.px-box {
    width: ___;  /* TODO: Make this 200 pixels wide */
    height: ___;  /* TODO: Make this 200 pixels tall */
    background-color: #3498db;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.px-text {
    font-size: ___;  /* TODO: Make this 16 pixels */
    margin: ____;  /* TODO: Add 10 pixels top/bottom, 0 left/right */
}
```

**Try this:** 
- Zoom in and out on your browser (Ctrl/Cmd + Plus/Minus)
- Notice how pixel sizes remain fixed relative to the screen

---

## Part 3: Understanding em

**em** is a relative unit based on the font-size of the parent element. 1em = the current font-size.

### Exercise 3.1: Using em

Add this HTML to your `<main>`:

```html
<section class="em-section">
    <h2>Em Units</h2>
    <div class="parent-16">
        <p>Parent font-size: 16px</p>
        <p class="em-text">This text is 1.5em (24px)</p>
        <div class="em-box">Width: 10em (160px)</div>
    </div>
    
    <div class="parent-24">
        <p>Parent font-size: 24px</p>
        <p class="em-text">This text is 1.5em (36px)</p>
        <div class="em-box">Width: 10em (240px)</div>
    </div>
</section>
```

**Instructions:** Fill in the blanks using **em** values:
- In `.parent-16`, the base font-size is 16px, so 1em = 16px
- Make the text 1.5 times the parent size (1.5em)
- Make the box width 10 times the font-size (10em)
- Make the box height 5 times the font-size (5em)

Add this CSS:

```css
.parent-16 {
    font-size: 16px;
    border: 2px solid #2ecc71;
    padding: ___;  /* TODO: Add 15 pixels of padding */
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.parent-24 {
    font-size: 24px;
    border: 2px solid #e74c3c;
    padding: ___;  /* TODO: Add 15 pixels of padding */
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.em-text {
    font-size: ___;  /* TODO: Make this 1.5 times the parent font-size using em */
    color: #34495e;
}

.em-box {
    width: ___;  /* TODO: Make this 10 times the font-size using em */
    height: ___;  /* TODO: Make this 5 times the font-size using em */
    background-color: #9b59b6;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 10 pixels top/bottom, 0 left/right */
}
```

**Observe:**
- The same `1.5em` produces different sizes in different parents
- In `.parent-16`: 1.5em = 1.5 × 16px = 24px
- In `.parent-24`: 1.5em = 1.5 × 24px = 36px
- Em units compound (nested em elements multiply)

### Exercise 3.2: Em Compounding

Add this HTML:

```html
<section class="em-compound">
    <h2>Em Compounding Example</h2>
    <div class="level-1">
        Level 1 (1em)
        <div class="level-2">
            Level 2 (1em of parent = 1.2em of root)
            <div class="level-3">
                Level 3 (1em of parent = 1.44em of root)
            </div>
        </div>
    </div>
</section>
```

**Instructions:** Observe how em values multiply in nested elements:
- Level 1: Set to 1em (same as parent)
- Level 2: Set to 1.2em (1.2 times Level 1)
- Level 3: Set to 1.2em (1.2 times Level 2, which is 1.2 × 1.2 = 1.44 times root)

Add this CSS:

```css
.level-1 {
    font-size: ___;  /* TODO: Set to 1em */
    padding: ___;  /* TODO: Add 15 pixels */
    background-color: #ecf0f1;
}

.level-2 {
    font-size: ___;  /* TODO: Make this 1.2 times its parent using em */
    padding: ___;  /* TODO: Add 15 pixels */
    background-color: #bdc3c7;
    margin-top: ___;  /* TODO: Add 10 pixels */
}

.level-3 {
    font-size: ___;  /* TODO: Make this 1.2 times its parent using em (will compound!) */
    padding: ___;  /* TODO: Add 15 pixels */
    background-color: #95a5a6;
    margin-top: ___;  /* TODO: Add 10 pixels */
}
```

**Understanding Compounding:**
- If root font-size is 16px:
  - Level 1: 1em = 16px
  - Level 2: 1.2em of 16px = 19.2px
  - Level 3: 1.2em of 19.2px = 23.04px (this is the compounding effect!)

---

## Part 4: Understanding rem (Root Em)

**rem** is relative to the root element's (`<html>`) font-size. This prevents compounding issues.

### Exercise 4.1: Using rem

Add this HTML:

```html
<section class="rem-section">
    <h2>Rem Units</h2>
    <div class="parent-16">
        <p>Parent font-size: 16px</p>
        <p class="rem-text">This text is 1.5rem (always 24px if root is 16px)</p>
        <div class="rem-box">Width: 10rem (always 160px)</div>
    </div>
    
    <div class="parent-24">
        <p>Parent font-size: 24px</p>
        <p class="rem-text">This text is 1.5rem (still 24px!)</p>
        <div class="rem-box">Width: 10rem (still 160px!)</div>
    </div>
</section>
```

**Instructions:** Fill in the blanks using **rem** values:
- First, set the root font-size to 16px
- Remember: rem is ALWAYS relative to the root, not the parent
- 1.5rem = 1.5 × 16px = 24px (no matter what the parent is!)

Add this CSS:

```css
html {
    font-size: ___;  /* TODO: Set root font-size to 16 pixels - this is what rem is based on! */
}

.rem-text {
    font-size: ___;  /* TODO: Make this 1.5 times the ROOT font-size using rem */
    color: #e67e22;
}

.rem-box {
    width: ___;  /* TODO: Make this 10 times the ROOT font-size using rem */
    height: ___;  /* TODO: Make this 5 times the ROOT font-size using rem */
    background-color: #16a085;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 10 pixels top/bottom, 0 left/right */
}
```

**Compare:** Notice how rem stays consistent regardless of parent font-size!
- In both `.parent-16` and `.parent-24`, the `.rem-text` is always 24px
- This is because rem always looks at the root (`<html>`), not the parent

---

## Part 5: Understanding vw (Viewport Width)

**vw** stands for viewport width. 1vw = 1% of the viewport's width.

### Exercise 5.1: Using vw

Add this HTML:

```html
<section class="vw-section">
    <h2>Viewport Width (vw)</h2>
    <div class="vw-box-50">50vw wide</div>
    <div class="vw-box-75">75vw wide</div>
    <p class="vw-text">This text is 5vw</p>
</section>
```

**Instructions:** Fill in the blanks using **vw** (viewport width) values:
- Make one box 50% of the viewport width
- Make another box 75% of the viewport width
- Make text size 5% of the viewport width
- Remember: 1vw = 1% of viewport width, so 50vw = 50% of viewport width

Add this CSS:

```css
.vw-box-50 {
    width: ___;  /* TODO: Make this 50% of the viewport width using vw */
    height: ___;  /* TODO: Make this 100 pixels tall */
    background-color: #f39c12;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.vw-box-75 {
    width: ___;  /* TODO: Make this 75% of the viewport width using vw */
    height: ___;  /* TODO: Make this 100 pixels tall */
    background-color: #d35400;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.vw-text {
    font-size: ___;  /* TODO: Make font size 5% of viewport width using vw */
    color: #c0392b;
}
```

**Try this:**
- Resize your browser window horizontally
- Watch how the elements change size proportionally
- On a 1000px wide screen: 50vw = 500px, 75vw = 750px
- On a 1200px wide screen: 50vw = 600px, 75vw = 900px

---

## Part 6: Understanding vh (Viewport Height)

**vh** stands for viewport height. 1vh = 1% of the viewport's height.

### Exercise 6.1: Using vh

Add this HTML:

```html
<section class="vh-section">
    <h2>Viewport Height (vh)</h2>
    <div class="vh-box-25">25vh tall</div>
    <div class="vh-box-50">50vh tall</div>
</section>
```

**Instructions:** Fill in the blanks using **vh** (viewport height) values:
- Make one box 25% of the viewport height
- Make another box 50% of the viewport height
- Remember: 1vh = 1% of viewport height, so 25vh = 25% of viewport height

Add this CSS:

```css
.vh-box-25 {
    width: ___;  /* TODO: Make this 200 pixels wide */
    height: ___;  /* TODO: Make this 25% of the viewport height using vh */
    background-color: #8e44ad;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}

.vh-box-50 {
    width: ___;  /* TODO: Make this 200 pixels wide */
    height: ___;  /* TODO: Make this 50% of the viewport height using vh */
    background-color: #2c3e50;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: ____;  /* TODO: Add 20 pixels top/bottom, 0 left/right */
}
```

**Try this:**
- Resize your browser window vertically
- See how the boxes adjust to viewport height
- On a 800px tall screen: 25vh = 200px, 50vh = 400px
- On a 1000px tall screen: 25vh = 250px, 50vh = 500px

---

## Part 7: Practical Challenges

### Challenge 1: Build a Responsive Card

Create a card component that uses multiple unit types. This challenge tests your understanding of when to use each unit!

**Requirements:**
- Width: 90% of viewport width (use vw)
- Max-width: 400 pixels (use px)
- Padding: 1.5 times the root font-size (use rem)
- Minimum height: 30% of viewport height (use vh)
- Title font-size: 2 times the root font-size (use rem)
- Body text font-size: 1 times the root font-size (use rem)

```html
<section class="challenge-section">
    <h2>Challenge 1: Responsive Card</h2>
    <div class="card">
        <h3 class="card-title">My Responsive Card</h3>
        <p class="card-body">This card uses multiple CSS units to be responsive and accessible.</p>
    </div>
</section>
```

**Try to write the CSS yourself first!** Fill in all the blanks with the appropriate units:

```css
.card {
    width: ___;  /* TODO: 90% of viewport width */
    max-width: ___;  /* TODO: Maximum 400 pixels */
    min-height: ___;  /* TODO: Minimum 30% of viewport height */
    padding: ___;  /* TODO: 1.5 times root font-size */
    background-color: #ecf0f1;
    border-radius: ___;  /* TODO: 8 pixels */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    margin: ____;  /* TODO: 20 pixels top/bottom, auto left/right */
}

.card-title {
    font-size: ___;  /* TODO: 2 times root font-size */
    color: #2c3e50;
    margin-top: 0;
}

.card-body {
    font-size: ___;  /* TODO: 1 times root font-size */
    line-height: 1.6;
    color: #34495e;
}
```

<details>
<summary>Click to see solution</summary>

```css
.card {
    width: 90vw;
    max-width: 400px;
    min-height: 30vh;
    padding: 1.5rem;
    background-color: #ecf0f1;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    margin: 20px auto;
}

.card-title {
    font-size: 2rem;
    color: #2c3e50;
    margin-top: 0;
}

.card-body {
    font-size: 1rem;
    line-height: 1.6;
    color: #34495e;
}
```
</details>

### Challenge 2: Full-Page Hero Section

Create a hero section that takes up the full viewport and has responsive text sizing.

**Requirements:**
- Height: 100% of viewport height (use vh)
- Title font-size: Use clamp() with 2rem minimum, 8vw preferred, 6rem maximum
- Subtitle font-size: Use clamp() with 1rem minimum, 3vw preferred, 2rem maximum
- Title margin: 0
- Subtitle top margin: 1rem

```html
<section class="hero">
    <h1 class="hero-title">Welcome</h1>
    <p class="hero-subtitle">Learning CSS Units</p>
</section>
```

**Try it yourself!** This is an advanced challenge using the `clamp()` function:

```css
.hero {
    height: ___;  /* TODO: Make this take up 100% of viewport height */
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
}

.hero-title {
    font-size: clamp(___, ___, ___);  /* TODO: min 2rem, preferred 8vw, max 6rem */
    margin: ___;  /* TODO: 0 margin */
}

.hero-subtitle {
    font-size: clamp(___, ___, ___);  /* TODO: min 1rem, preferred 3vw, max 2rem */
    margin-top: ___;  /* TODO: 1rem top margin */
}
```

**What is clamp()?**
- `clamp(MIN, PREFERRED, MAX)` is a CSS function that sets a value between a minimum and maximum
- Example: `clamp(1rem, 5vw, 3rem)` means:
  - Never smaller than 1rem
  - Prefers 5vw (responsive to viewport)
  - Never larger than 3rem

<details>
<summary>Click to see solution</summary>

```css
.hero {
    height: 100vh;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
}

.hero-title {
    font-size: clamp(2rem, 8vw, 6rem);
    margin: 0;
}

.hero-subtitle {
    font-size: clamp(1rem, 3vw, 2rem);
    margin-top: 1rem;
}
```
</details>

---

## Summary: When to Use Each Unit

### Use **px** when:
- You need precise, fixed sizes (borders, shadows)
- Creating pixel-perfect designs
- Size should never change

### Use **em** when:
- You want size relative to parent element
- Creating modular components
- You understand the compounding effect

### Use **rem** when:
- You want size relative to root font-size
- Creating consistent spacing systems
- Avoiding compounding issues
- Making accessible, scalable interfaces (recommended!)

### Use **vw** when:
- You want width relative to viewport
- Creating fluid typography
- Building responsive layouts

### Use **vh** when:
- You want height relative to viewport
- Creating full-screen sections
- Building splash screens or heroes

---

## Bonus: Best Practices

1. **Set a root font-size** for easy rem calculations:
   ```css
   html {
       font-size: 16px; /* 1rem = 16px */
   }
   ```

2. **Use rem for most spacing and sizing:**
   ```css
   .button {
       padding: 0.75rem 1.5rem;
       font-size: 1rem;
       border-radius: 0.25rem;
   }
   ```

3. **Combine units with clamp() for responsive typography:**
   ```css
   h1 {
       font-size: clamp(2rem, 5vw, 4rem);
   }
   ```

4. **Use viewport units carefully** - they can cause issues on mobile with address bars

---

## Additional Resources

- [MDN: CSS Values and Units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
- [A Complete Guide to CSS Units](https://www.w3schools.com/cssref/css_units.php)
- Practice with browser DevTools to see computed values

---

## Quiz

Test your understanding:

1. If the root font-size is 16px, what is 2rem in pixels?
2. If a parent element has font-size of 20px, what is 2em in pixels?
3. On a 1200px wide screen, what is 50vw in pixels?
4. What's the main advantage of rem over em?
5. When would you use vh instead of px for height?

<details>
<summary>Answers</summary>

1. 32px (2 × 16px)
2. 40px (2 × 20px)
3. 600px (50% of 1200px)
4. rem doesn't compound; it always references the root element
5. When you want the height to be responsive to the viewport size, like full-screen sections
</details>

---

Congratulations! You've completed the CSS Units Lab. Keep practicing and experiment with different combinations to see what works best for your projects!

---

## Answer Key

<details>
<summary><strong>Click here to check your answers after completing the lab</strong></summary>

### Part 2: Pixels (px)

```css
body {
    padding: 20px;
}

.px-box {
    width: 200px;
    height: 200px;
    margin: 20px 0;
}

.px-text {
    font-size: 16px;
    margin: 10px 0;
}
```

### Part 3: Em Units

```css
.parent-16 {
    padding: 15px;
    margin: 20px 0;
}

.parent-24 {
    padding: 15px;
    margin: 20px 0;
}

.em-text {
    font-size: 1.5em;
}

.em-box {
    width: 10em;
    height: 5em;
    margin: 10px 0;
}

.level-1 {
    font-size: 1em;
    padding: 15px;
}

.level-2 {
    font-size: 1.2em;
    padding: 15px;
    margin-top: 10px;
}

.level-3 {
    font-size: 1.2em;
    padding: 15px;
    margin-top: 10px;
}
```

### Part 4: Rem Units

```css
html {
    font-size: 16px;
}

.rem-text {
    font-size: 1.5rem;
}

.rem-box {
    width: 10rem;
    height: 5rem;
    margin: 10px 0;
}
```

### Part 5: Viewport Width (vw)

```css
.vw-box-50 {
    width: 50vw;
    height: 100px;
    margin: 20px 0;
}

.vw-box-75 {
    width: 75vw;
    height: 100px;
    margin: 20px 0;
}

.vw-text {
    font-size: 5vw;
}
```

### Part 6: Viewport Height (vh)

```css
.vh-box-25 {
    width: 200px;
    height: 25vh;
    margin: 20px 0;
}

.vh-box-50 {
    width: 200px;
    height: 50vh;
    margin: 20px 0;
}
```

### Challenge 1: Responsive Card

```css
.card {
    width: 90vw;
    max-width: 400px;
    min-height: 30vh;
    padding: 1.5rem;
    border-radius: 8px;
    margin: 20px auto;
}

.card-title {
    font-size: 2rem;
}

.card-body {
    font-size: 1rem;
}
```

### Challenge 2: Full-Page Hero

```css
.hero {
    height: 100vh;
}

.hero-title {
    font-size: clamp(2rem, 8vw, 6rem);
    margin: 0;
}

.hero-subtitle {
    font-size: clamp(1rem, 3vw, 2rem);
    margin-top: 1rem;
}
```

</details>
