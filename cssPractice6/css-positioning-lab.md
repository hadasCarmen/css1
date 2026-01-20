# CSS Positioning Lab for Beginners

## Introduction
In this lab, you'll learn about three important CSS position values: `relative`, `absolute`, and `fixed`. By the end, you'll understand when and how to use each one.

---

## Part 1: Understanding the Basics

### Position Values:
- **`relative`** - Element is positioned relative to its normal position in the document flow
- **`absolute`** - Element is positioned relative to its nearest positioned ancestor (or the body if none exists)
- **`fixed`** - Element is positioned relative to the viewport (browser window) and stays in place when scrolling

---

## Part 2: Exercises

For each scenario below, fill in the blank with the correct position value: `relative`, `absolute`, or `fixed`.

### Exercise 1: Sticky Header
**Scenario:** You want to create a navigation bar that stays at the top of the page even when the user scrolls down.

```css
.navbar {
    position: ___________;
    top: 0;
    left: 0;
    width: 100%;
}
```

---

### Exercise 2: Shifted Element
**Scenario:** You want to move a button 10px down and 20px to the right from where it would normally appear, but you want it to still take up its original space in the layout.

```css
.button {
    position: ___________;
    top: 10px;
    left: 20px;
}
```

---

### Exercise 3: Badge on a Card
**Scenario:** You have a product card, and you want to place a "Sale!" badge in the top-right corner of the card. The card should be the reference point for positioning the badge.

```css
.product-card {
    position: ___________;
}

.sale-badge {
    position: ___________;
    top: 10px;
    right: 10px;
}
```

---

### Exercise 4: Centered Modal Overlay
**Scenario:** You want to create a modal dialog that appears centered on the screen, positioned relative to the browser window (not the page content).

```css
.modal {
    position: ___________;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

---

### Exercise 5: Footer Icon (Absolute to Body)
**Scenario:** You want to place a small icon in the bottom-right corner of the entire webpage (relative to the body element), and no parent container should affect its position.

```css
body {
    position: ___________;
}

.footer-icon {
    position: ___________;
    bottom: 20px;
    right: 20px;
}
```

---

### Exercise 6: Tooltip Above Button
**Scenario:** You have a button with a tooltip that should appear directly above it. The button is the reference point for the tooltip's position.

```css
.button-container {
    position: ___________;
}

.tooltip {
    position: ___________;
    bottom: 100%;
    left: 50%;
    transform: translateX(-50%);
}
```

---

### Exercise 7: Floating Action Button
**Scenario:** You want a circular "Add" button to float in the bottom-right corner of the viewport and remain visible even when the user scrolls through a long page.

```css
.fab-button {
    position: ___________;
    bottom: 30px;
    right: 30px;
}
```

---

### Exercise 8: Nudging an Image
**Scenario:** You want to move an image slightly upward (by 5px) from its normal position in the layout, but keep the surrounding elements in their original positions.

```css
.image {
    position: ___________;
    top: -5px;
}
```

---

## Part 3: Bonus Challenge

Create a card component with:
- A container with `position: relative`
- An image inside the card
- A "Featured" ribbon positioned in the top-left corner using `position: absolute`
- A floating heart icon in the bottom-right corner using `position: absolute`

Write the HTML and CSS for this component below:

```html
<!-- Your HTML here -->
```

```css
/* Your CSS here */
```

---

## Key Takeaways
- Use `relative` to nudge elements from their normal position while keeping their space in the layout
- Use `absolute` to position elements relative to a parent container (the parent must have `position: relative`)
- Use `absolute` with `position: relative` on the body to position elements relative to the entire page
- Use `fixed` to position elements relative to the viewport (great for navbars and floating buttons)

Happy coding! 🚀
