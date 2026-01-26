# Issue #4: Build the Sidebar - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

The sidebar is a vertical list of category links. One link should look "selected."

Think about:
- What HTML element is used for navigation?
- How do you make a list without bullet points?
- How do you make one link look different (the active one)?

---

## Hint 2: Getting Warmer

**HTML structure:**
- `<aside>` is good for sidebars
- `<nav>` for navigation
- `<ul>` and `<li>` for the list of links
- Add a class like `active` to the selected link

**Styling:**
- Give the sidebar a fixed width (like `200px` or `250px`)
- Remove list bullets with `list-style: none`
- Make links block-level so they fill the width
- Give the active link a different background color

---

## Hint 3: Full Solution

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
  width: 200px;
  background-color: #ffffff;
  padding: 20px 0;
}

.sidebar h2 {
  padding: 0 16px;
  margin-bottom: 12px;
  font-size: 14px;
  color: #666;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.sidebar a {
  display: block;
  padding: 10px 16px;
  color: #333;
  text-decoration: none;
}

.sidebar a:hover {
  background-color: #f5f5f5;
}

.sidebar a.active {
  background-color: #e0e7ff;
  color: #4f46e5;
}
```
