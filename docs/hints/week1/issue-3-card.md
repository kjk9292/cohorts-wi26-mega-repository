# Issue #3: Build the Bookmark Card - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

Each card shows a bookmark with: icon, title (clickable), URL, description, category, and delete button.

Think about:
- How do you lay out an icon on the left with content on the right?
- What HTML element is semantic for a self-contained piece of content?
- How do you make text that's too long show "..." instead of overflowing?
- How do you limit text to a certain number of lines?

---

## Hint 2: Getting Warmer

**Layout approach:**
- Use flexbox on the card: icon, content area, and delete button in a row
- The content area holds the stacked text (title, url, description, category)

**HTML elements:**
- `<article>` for each card (semantic!)
- `<a>` with `target="_blank"` for the clickable title
- `<span>` for the category badge
- `<button>` for delete

**Text truncation (CSS):**
- Single line truncation: `white-space: nowrap`, `overflow: hidden`, `text-overflow: ellipsis`
- Multi-line truncation: Look up `-webkit-line-clamp`

**Delete button UX:**
- Start with low opacity, increase on hover
- Use `--color-danger` for the color

---

## Hint 3: Detailed Structure

**HTML (one card):**
```html
<article class="bookmark-card">
  <div class="bookmark-icon">
    <span>G</span>
  </div>
  <div class="bookmark-content">
    <h3 class="bookmark-title">
      <a href="https://github.com" target="_blank">GitHub</a>
    </h3>
    <p class="bookmark-url">https://github.com</p>
    <p class="bookmark-description">
      Where the world builds software. Millions of developers use GitHub for version control.
    </p>
    <span class="bookmark-category">Work</span>
  </div>
  <button class="bookmark-delete" aria-label="Delete bookmark">
    &times;
  </button>
</article>
```

**CSS:**
```css
.bookmark-card {
  display: flex;
  gap: 12px;
  padding: 16px;
  background: var(--color-surface);
  border-radius: var(--radius);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.2s, transform 0.2s;
}

.bookmark-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  transform: translateY(-2px);
}

.bookmark-icon {
  width: 40px;
  height: 40px;
  border-radius: var(--radius);
  background: var(--color-primary-light);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: var(--color-primary-dark);
  flex-shrink: 0;
}

.bookmark-content {
  flex: 1;
  min-width: 0; /* Important for text truncation! */
}

.bookmark-title a {
  color: var(--color-text);
  text-decoration: none;
  font-weight: 500;
}

.bookmark-title a:hover {
  color: var(--color-primary);
}

.bookmark-url {
  font-size: 0.875rem;
  color: var(--color-text-light);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.bookmark-description {
  font-size: 0.875rem;
  color: var(--color-text-light);
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.bookmark-category {
  display: inline-block;
  padding: 2px 8px;
  font-size: 0.75rem;
  background: var(--color-primary-light);
  color: var(--color-primary-dark);
  border-radius: 999px;
}

.bookmark-delete {
  background: none;
  border: none;
  font-size: 1.25rem;
  cursor: pointer;
  opacity: 0.5;
  color: var(--color-danger);
  transition: opacity 0.2s;
}

.bookmark-delete:hover {
  opacity: 1;
}
```

**Example bookmarks to create:**
1. GitHub - Work
2. YouTube - Entertainment
3. MDN Web Docs - Learning
4. Gmail - Personal
5. Stack Overflow - Learning
6. Netflix - Entertainment
