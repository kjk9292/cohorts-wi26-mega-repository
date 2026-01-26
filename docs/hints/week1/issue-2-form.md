# Issue #2: Build the Add Bookmark Form - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

A form needs labeled inputs that stack vertically. Think about:
- What's the semantic HTML element for forms?
- How do you associate a label with an input? (accessibility matters!)
- What input types exist for URLs vs regular text vs multi-line text?
- How do you create a dropdown selection?

For styling, the form should look like a "card" - elevated from the background.

---

## Hint 2: Getting Warmer

**Form structure:**
- Wrap everything in a `<form>` element
- Each field needs a `<label>` and its corresponding input
- Group each label+input pair in a container div for spacing

**Input types to use:**
- `type="url"` for the URL field
- `type="text"` for the title
- `<textarea>` for description
- `<select>` with `<option>` elements for category

**Card styling tips:**
- Background color: `--color-surface`
- Add padding, border-radius, and maybe a subtle shadow
- Inputs should be full-width (`width: 100%`)

**Focus states:**
- Remove default outline
- Change border color to `--color-primary` on focus

---

## Hint 3: Detailed Structure

**HTML:**
```html
<section class="add-bookmark-section">
  <form class="add-bookmark-form">
    <div class="form-group">
      <label for="url">URL</label>
      <input type="url" id="url" name="url" placeholder="https://example.com" required>
    </div>
    <div class="form-group">
      <label for="title">Title</label>
      <input type="text" id="title" name="title" placeholder="Website name" required>
    </div>
    <div class="form-group">
      <label for="description">Description (optional)</label>
      <textarea id="description" name="description" rows="2" placeholder="What's this bookmark about?"></textarea>
    </div>
    <div class="form-group">
      <label for="category">Category</label>
      <select id="category" name="category">
        <option value="work">Work</option>
        <option value="personal">Personal</option>
        <option value="learning">Learning</option>
        <option value="entertainment">Entertainment</option>
      </select>
    </div>
    <button type="submit" class="form-submit-btn">Save Bookmark</button>
  </form>
</section>
```

**CSS:**
```css
.add-bookmark-form {
  background: var(--color-surface);
  padding: 24px;
  border-radius: var(--radius);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 16px;
}

.form-group label {
  display: block;
  margin-bottom: 4px;
  font-weight: 500;
}

.form-group input,
.form-group textarea,
.form-group select {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid var(--color-border);
  border-radius: var(--radius);
  font-size: 1rem;
}

.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
  outline: none;
  border-color: var(--color-primary);
}

.form-submit-btn {
  background-color: var(--color-primary);
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: var(--radius);
  cursor: pointer;
  width: 100%;
}
```
