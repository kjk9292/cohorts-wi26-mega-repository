# Issue #3: Build the Bookmark Cards - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

Each card shows info about one bookmark: title, URL, and category.

Think about:
- What HTML element is good for a self-contained piece of content?
- How do you make a link open in a new tab?
- How do you make something look like a "card"?

---

## Hint 2: Getting Warmer

**HTML elements:**
- `<article>` or `<div>` for each card
- `<a>` for the clickable title (use `target="_blank"` to open in new tab)
- `<p>` for the URL
- `<span>` for the category label

**Card styling:**
- Add a border: `border: 1px solid #ccc`
- Or add a shadow: `box-shadow: 0 2px 4px rgba(0,0,0,0.1)`
- Add padding inside the card
- Add border-radius for rounded corners

**Category badge:**
- Give it a background color
- Add small padding
- Make it inline with `display: inline-block`

---

## Hint 3: Full Solution

**HTML (one card):**
```html
<article class="bookmark-card">
  <h3 class="card-title">
    <a href="https://github.com" target="_blank">GitHub</a>
  </h3>
  <p class="card-url">https://github.com</p>
  <span class="card-category">Work</span>
</article>
```

**CSS:**
```css
.bookmark-card {
  background-color: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 16px;
  margin-bottom: 12px;
}

.card-title {
  margin: 0 0 8px 0;
}

.card-title a {
  color: #333;
  text-decoration: none;
}

.card-title a:hover {
  color: #6366f1;
}

.card-url {
  color: #666;
  font-size: 14px;
  margin: 0 0 8px 0;
}

.card-category {
  display: inline-block;
  background-color: #e0e7ff;
  color: #4f46e5;
  padding: 4px 12px;
  border-radius: 20px;
  font-size: 12px;
}
```
