# Week 1: HTML & CSS

This week we're building the static UI for our bookmark manager. No JavaScript yet - just pure HTML structure and CSS styling.

## Learning Objectives

- Semantic HTML5 elements
- CSS Flexbox and Grid layouts
- CSS custom properties (variables)
- Component-based thinking (even without JS)
- Responsive design basics

## The Design

We're building a bookmark manager with these sections:

```
┌─────────────────────────────────────────────────────┐
│  Header (Logo + Nav)                                │
├─────────────────────────────────────────────────────┤
│           │                                         │
│  Sidebar  │   Main Content Area                     │
│           │   ┌─────────┐ ┌─────────┐ ┌─────────┐   │
│  - All    │   │ Card 1  │ │ Card 2  │ │ Card 3  │   │
│  - Work   │   └─────────┘ └─────────┘ └─────────┘   │
│  - Personal│   ┌─────────┐ ┌─────────┐              │
│  - Learning│   │ Card 4  │ │ Card 5  │              │
│           │   └─────────┘ └─────────┘              │
├─────────────────────────────────────────────────────┤
│  Footer                                             │
└─────────────────────────────────────────────────────┘
```

## Setup

1. Open `frontend/index.html` in VS Code
2. Install the "Live Server" extension if you haven't
3. Right-click `index.html` → "Open with Live Server"
4. You'll see changes in real-time as you code

## This Week's Issues

Each pair should claim ONE issue. Work together!

| Issue | Description | Difficulty |
|-------|-------------|------------|
| #1 | Build the Header | Easy |
| #2 | Build the Add Bookmark Form | Medium |
| #3 | Build the Bookmark Card | Medium |
| #4 | Build the Sidebar | Easy |
| #5 | Create the Main Layout | Medium |
| #6 | Add Responsive Design | Hard (Bonus) |

## File Structure

```
frontend/
├── index.html      # Main HTML file
├── styles.css      # All styles
└── assets/         # Images, icons (if needed)
```

## HTML Structure Overview

The `index.html` has placeholder sections. Your job is to fill them in based on your issue.

```html
<body>
  <header class="header">         <!-- Issue #1 -->
    <!-- Logo, nav, add button -->
  </header>

  <div class="app-container">
    <aside class="sidebar">       <!-- Issue #4 -->
      <!-- Category list -->
    </aside>

    <main class="main-content">   <!-- Issue #5 -->
      <!-- Add form (#2) + Bookmark grid (#3) -->
    </main>
  </div>

  <footer class="footer">
    <!-- Footer content -->
  </footer>
</body>
```

## CSS Variables

We've set up CSS variables in `styles.css`. Use these for consistency:

```css
:root {
  --color-primary: #6366f1;     /* Indigo - buttons, accents */
  --color-primary-dark: #4f46e5;
  --color-bg: #f8fafc;          /* Light gray background */
  --color-surface: #ffffff;      /* Card backgrounds */
  --color-text: #1e293b;         /* Dark text */
  --color-text-muted: #64748b;   /* Secondary text */
  --color-border: #e2e8f0;       /* Borders */
  --radius: 8px;                 /* Border radius */
  --shadow: 0 1px 3px rgba(0,0,0,0.1);
}
```

## Tips

- **Use semantic HTML**: `<header>`, `<main>`, `<aside>`, `<footer>`, `<nav>`, `<article>`
- **Use Flexbox**: Great for navbars, card layouts, centering
- **Use Grid**: Great for the bookmark card grid
- **Mobile-first**: Start with mobile layout, add media queries for larger screens

## Resources

- [CSS Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [HTML5 Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantic_elements)

## Acceptance Criteria

By the end of Week 1, the app should:

- [ ] Have a header with logo and navigation
- [ ] Have a sidebar with category list
- [ ] Display a form to add new bookmarks
- [ ] Show bookmark cards in a grid layout
- [ ] Look good on both mobile and desktop
- [ ] Use consistent colors and spacing from CSS variables

## Next Week Preview

In Week 2, we'll add JavaScript to:
- Make the "Add Bookmark" form actually work
- Store bookmarks in localStorage
- Delete and edit bookmarks
- Filter by category
