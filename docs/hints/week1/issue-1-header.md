# Issue #1: Build the Header - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

You need two things side-by-side: the app name on the left, a button on the right.

Think about:
- What CSS property lets you put things in a row?
- How do you push items to opposite sides of a container?

---

## Hint 2: Getting Warmer

**Layout approach:** Use flexbox!
- `display: flex` makes children line up in a row
- `justify-content: space-between` pushes items to opposite ends

**HTML elements:**
- `<header>` for the container
- `<h1>` for the app name
- `<button>` for the add button

**Basic styling:**
- Give the header some padding so content isn't touching the edges
- Add a background color (white: `#ffffff`)
- Style the button with a background color and white text

---

## Hint 3: Full Solution

**HTML:**
```html
<header class="header">
  <h1>Bookmark Manager</h1>
  <button class="add-btn">+ Add Bookmark</button>
</header>
```

**CSS:**
```css
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 24px;
  background-color: #ffffff;
}

.add-btn {
  background-color: #6366f1;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}
```
