# Week 1: HTML & CSS

This week we're building the static UI for our bookmark manager. No JavaScript yet - just pure HTML structure and CSS styling.

## Learning Objectives

- Semantic HTML5 elements (`<header>`, `<main>`, `<aside>`, `<footer>`, `<nav>`, `<article>`)
- CSS Flexbox for layouts
- Basic styling (colors, spacing, borders)
- Working with forms and inputs

## The Design

We're building a bookmark manager with these sections:

```
┌────────────────────────────────────────────────────────┐
│  Header (Logo + Button)                                │
├────────────────────────────────────────────────────────┤
│              │                                         │
│   Sidebar    │   Main Content Area                     │
│              │                                         │
│  - All       │   ┌─────────────────────────────────┐   │
│  - Work      │   │      Add Bookmark Form          │   │
│  - Personal  │   └─────────────────────────────────┘   │
│  - Learning  │                                         │
│  - Enter-    │   ┌─────────┐ ┌─────────┐ ┌─────────┐   │
│    tainment  │   │ Card 1  │ │ Card 2  │ │ Card 3  │   │
│              │   └─────────┘ └─────────┘ └─────────┘   │
│              │                                         │
├────────────────────────────────────────────────────────┤
│  Footer                                                │
└────────────────────────────────────────────────────────┘
```

## Setup

1. Open `frontend/index.html` in VS Code
2. Install the "Live Server" extension if you haven't
3. Right-click `index.html` → "Open with Live Server"
4. You'll see changes in real-time as you code

## This Week's Issues

Each pair should claim ONE issue. **All issues can be worked on in parallel!**

| Issue | Description | Difficulty |
|-------|-------------|------------|
| #1 | Build the Header | Easy |
| #2 | Build the Add Bookmark Form | Easy |
| #3 | Build the Bookmark Cards | Medium |
| #4 | Build the Sidebar | Easy |
| #5 | Build the Footer | Easy |

## File Structure

```
frontend/
├── index.html      # Main HTML file (layout is pre-built)
├── styles.css      # Styles (layout is pre-built, add your component styles)
└── examples/       # Working examples for each issue
    ├── issue-1-header/
    ├── issue-2-form/
    ├── issue-3-card/
    ├── issue-4-sidebar/
    ├── issue-5-footer/
    └── full-solution/
```

## How to Work on Your Issue

1. **Find your section** in `index.html` - look for the comment with your issue number
2. **Replace the placeholder** with your HTML code
3. **Add your styles** in `styles.css` under the section for your issue
4. **Check the example** in `frontend/examples/issue-X/` to see what it should look like
5. **Use the hints** in `docs/hints/week1/issue-X.md` if you get stuck

## Tips

- **Use semantic HTML**: `<header>`, `<main>`, `<aside>`, `<footer>`, `<nav>`, `<article>`
- **Use Flexbox**: Great for putting things side-by-side (`display: flex`)
- **Check the examples**: Open them in your browser to see the goal
- **Start simple**: Get the HTML structure right first, then add styling

## Resources

- [CSS Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [HTML5 Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantic_elements)
- [MDN HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)

## Acceptance Criteria

By the end of Week 1, the app should:

- [ ] Have a header with app name and "Add Bookmark" button
- [ ] Have a sidebar with category links
- [ ] Display a form to add new bookmarks
- [ ] Show bookmark cards with title, URL, and category
- [ ] Have a footer at the bottom

## Next Week Preview

In Week 2, we'll add JavaScript to:
- Make the "Add Bookmark" form actually work
- Store bookmarks in localStorage
- Delete bookmarks
- Filter by category
