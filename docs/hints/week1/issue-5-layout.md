# Issue #5: Create the Main Layout - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

You need a responsive grid that automatically adjusts the number of columns based on screen width.

Think about:
- Which CSS layout system lets you create grids with automatic column counts?
- How can you set a minimum card width but let them grow to fill space?
- What's the difference between `auto-fill` and `auto-fit`?

---

## Hint 2: Getting Warmer

**CSS Grid is the answer:**
- `display: grid` on the container
- `grid-template-columns` controls column sizing
- Look up `repeat()`, `auto-fill`, and `minmax()` functions

**The magic formula:**
- `repeat(auto-fill, minmax(MIN_WIDTH, 1fr))`
- This creates as many columns as fit, each at least MIN_WIDTH but growing equally

**Additional layout concerns:**
- Add gap between cards with the `gap` property
- The main content area needs padding
- Consider a max-width so content doesn't stretch too wide on huge screens

---

## Hint 3: Detailed Structure

**HTML context:**
```html
<main class="main-content">
  <h2 class="section-title">All Bookmarks</h2>
  <div class="bookmark-grid">
    <!-- bookmark cards go here -->
  </div>
</main>
```

**CSS:**
```css
.main-content {
  flex: 1;
  padding: 24px;
  max-width: 1200px;
}

.section-title {
  margin-bottom: 20px;
  font-size: 1.5rem;
  color: var(--color-text);
}

.bookmark-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 16px;
}
```

**Overall page layout (for context):**
```css
.app-container {
  display: flex;
  min-height: calc(100vh - var(--header-height));
}
```

This makes the sidebar and main content sit side-by-side, with main content taking remaining space.
