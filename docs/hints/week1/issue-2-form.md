# Issue #2: Build the Add Bookmark Form - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

A form has inputs stacked vertically, each with a label above it.

Think about:
- What HTML element wraps a form?
- How do you connect a label to an input? (for accessibility)
- What's the difference between `<input>`, `<textarea>`, and `<select>`?

---

## Hint 2: Getting Warmer

**Form structure:**
- Wrap everything in a `<form>` element
- Each field needs a `<label>` and an input
- Use `for="id"` on labels to connect them to inputs

**Input types:**
- `<input type="url">` for the URL
- `<input type="text">` for the title
- `<select>` with `<option>` elements for the dropdown

**Styling tips:**
- Give the form a background color (like white or light gray)
- Add padding inside the form
- Make inputs full width with `width: 100%`
- Add some margin between form fields

---

## Hint 3: Full Solution

**HTML:**
```html
<form class="bookmark-form">
  <div class="form-group">
    <label for="url">URL</label>
    <input type="url" id="url" name="url" placeholder="https://example.com">
  </div>

  <div class="form-group">
    <label for="title">Title</label>
    <input type="text" id="title" name="title" placeholder="Website name">
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

  <button type="submit" class="submit-btn">Save Bookmark</button>
</form>
```

**CSS:**
```css
.bookmark-form {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
}

.form-group {
  margin-bottom: 16px;
}

.form-group label {
  display: block;
  margin-bottom: 4px;
  font-weight: bold;
}

.form-group input,
.form-group select {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.submit-btn {
  background-color: #6366f1;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}
```
