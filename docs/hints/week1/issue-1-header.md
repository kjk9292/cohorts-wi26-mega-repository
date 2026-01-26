# Issue #1: Build the Header - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

You need two elements side-by-side: logo on the left, button on the right.

Think about:
- Which CSS layout system is best for placing items on opposite ends of a container?
- What HTML elements make sense for a logo/title and an action button?

---

## Hint 2: Getting Warmer

**Layout approach:** Flexbox is your friend here. The key properties you'll need:
- `display: flex` on the header
- A property that pushes items to opposite ends (look up "flexbox space between")
- A property that vertically centers items

**HTML elements to consider:**
- `<header>` as the container
- `<h1>` for the logo/app name
- `<button>` for the add action

**Styling tips:**
- Use the CSS variable `--header-height` for consistent height
- The button should use `--color-primary` for the background

---

## Hint 3: Detailed Structure

**HTML:**
```html
<header class="header">
  <h1 class="logo">Bookmark Manager</h1>
  <button class="add-btn">+ Add Bookmark</button>
</header>
```

**CSS:**
```css
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: var(--header-height);
  padding: 0 24px;
  background: white;
  border-bottom: 1px solid var(--color-border);
}

.add-btn {
  background-color: var(--color-primary);
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: var(--radius);
  cursor: pointer;
}

.add-btn:hover {
  background-color: var(--color-primary-dark);
}
```
