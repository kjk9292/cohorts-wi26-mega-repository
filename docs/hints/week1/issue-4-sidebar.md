# Issue #4: Build the Sidebar - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

The sidebar is a navigation panel with a list of category links. One link should look "active" (selected).

Think about:
- What semantic HTML element represents a sidebar/complementary content?
- What element is used for navigation with a list of links?
- How do you make links that don't actually go anywhere yet?
- How do you make one item look different (the active state)?

---

## Hint 2: Getting Warmer

**HTML structure:**
- `<aside>` is the semantic element for sidebars
- `<nav>` contains navigation links
- `<ul>` and `<li>` for the list of links
- Add a class like `active` to the "All Bookmarks" link

**Styling approach:**
- Fixed width using `--sidebar-width` variable
- Links should be block-level so they fill the width
- Remove default list styling (bullets, padding)

**States to style:**
- Default link appearance
- Hover state (subtle background change)
- Active state (different background + text color to show it's selected)

---

## Hint 3: Detailed Structure

**HTML:**
```html
<aside class="sidebar">
  <h2>Categories</h2>
  <nav>
    <ul>
      <li><a href="#" class="active">All Bookmarks</a></li>
      <li><a href="#">Work</a></li>
      <li><a href="#">Personal</a></li>
      <li><a href="#">Learning</a></li>
      <li><a href="#">Entertainment</a></li>
    </ul>
  </nav>
</aside>
```

**CSS:**
```css
.sidebar {
  width: var(--sidebar-width);
  background: var(--color-surface);
  border-right: 1px solid var(--color-border);
  padding: 24px 0;
}

.sidebar h2 {
  padding: 0 16px;
  margin-bottom: 16px;
  font-size: 0.875rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: var(--color-text-light);
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.sidebar a {
  display: block;
  padding: 10px 16px;
  color: var(--color-text);
  text-decoration: none;
  transition: background 0.2s;
}

.sidebar a:hover {
  background: var(--color-bg);
}

.sidebar a.active {
  background: var(--color-primary-light);
  color: var(--color-primary-dark);
  font-weight: 500;
}
```
