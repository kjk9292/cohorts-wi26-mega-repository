# Issue #5: Build the Footer - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

A footer sits at the bottom of the page with some simple text (like copyright or credits).

Think about:
- What HTML element is used for footers?
- How do you center text?
- How do you make it look different from the main content?

---

## Hint 2: Getting Warmer

**HTML structure:**
- Use the `<footer>` element
- Add a `<p>` tag with your text inside

**Styling:**
- Center text with `text-align: center`
- Add a background color (white works well)
- Add a top border to separate it from content above
- Use a lighter/muted text color

---

## Hint 3: Full Solution

**HTML:**
```html
<footer class="footer">
  <p>Built with learning by CSES Cohorts</p>
</footer>
```

**CSS:**
```css
.footer {
  text-align: center;
  padding: 16px;
  background-color: #ffffff;
  border-top: 1px solid #e0e0e0;
  color: #666;
}
```
