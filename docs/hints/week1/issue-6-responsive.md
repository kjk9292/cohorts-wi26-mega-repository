# Issue #6: Add Responsive Design (BONUS) - Hints

Try each hint level one at a time. Only move to the next if you're truly stuck!

---

## Hint 1: Conceptual Direction

Responsive design means your layout adapts to different screen sizes. You'll use CSS media queries to apply different styles at different breakpoints.

Think about:
- What changes between desktop, tablet, and mobile views?
- What elements might need to be hidden on small screens?
- How do media queries work? (`@media`)
- What's a "mobile-first" vs "desktop-first" approach?

Common breakpoints: 768px (tablet), 480px (mobile)

---

## Hint 2: Getting Warmer

**Media query syntax:**
```css
@media (max-width: 768px) {
  /* Styles for screens 768px and smaller */
}
```

**What to change at each breakpoint:**

**Tablet (768px):**
- Reduce sidebar width
- Grid might show fewer columns

**Mobile (480px):**
- Hide the sidebar entirely
- Stack layout vertically instead of side-by-side
- Single column grid
- Reduce padding/spacing
- Make sure buttons are big enough to tap (44px minimum)

**Key properties you'll override:**
- `display: none` to hide elements
- `flex-direction: column` for vertical stacking
- `width` adjustments
- `padding` reductions
- Grid column changes

---

## Hint 3: Detailed Structure

```css
/* Tablet */
@media (max-width: 768px) {
  .sidebar {
    width: 200px;
  }

  .bookmark-grid {
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  }

  .main-content {
    padding: 16px;
  }
}

/* Mobile */
@media (max-width: 480px) {
  .sidebar {
    display: none;
  }

  .app-container {
    flex-direction: column;
  }

  .header {
    padding: 12px 16px;
  }

  .logo {
    font-size: 1.25rem;
  }

  .bookmark-grid {
    grid-template-columns: 1fr;
  }

  .main-content {
    padding: 12px;
  }

  .bookmark-card {
    padding: 12px;
  }

  .add-bookmark-form {
    padding: 16px;
  }

  .form-submit-btn,
  .add-btn {
    padding: 12px 16px; /* Bigger touch targets */
  }
}
```

**Testing tips:**
- Use browser dev tools to simulate different screen sizes
- Test on actual devices if possible
- Make sure nothing causes horizontal scrolling
- Check that all text is readable without zooming
