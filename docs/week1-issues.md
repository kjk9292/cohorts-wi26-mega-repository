# Week 1 Issues

Copy these to GitHub Issues. Each pair claims one issue.

---

## Issue #1: Build the Header

**Labels:** `week-1`, `html`, `css`, `difficulty:easy`

### Description
Create the header/navbar for the bookmark manager.

### Requirements
- [ ] Logo or app name on the left ("Bookmark Manager" or an icon)
- [ ] "Add Bookmark" button on the right
- [ ] Fixed height (use `--header-height` variable)
- [ ] White background with subtle bottom border
- [ ] Use flexbox for layout

### HTML Structure
```html
<header class="header">
  <h1 class="logo">Bookmark Manager</h1>
  <button class="add-btn">+ Add Bookmark</button>
</header>
```

### CSS Hints
- `display: flex` with `justify-content: space-between`
- `align-items: center`
- `padding: 0 24px`
- Button: `background-color: var(--color-primary)`, `color: white`

### Acceptance Criteria
- [ ] Header spans full width
- [ ] Logo on left, button on right
- [ ] Button has hover effect (darker shade)
- [ ] Looks clean and professional

---

## Issue #2: Build the Add Bookmark Form

**Labels:** `week-1`, `html`, `css`, `difficulty:medium`

### Description
Create a form for adding new bookmarks. The form won't work yet (that's Week 2) - just build the HTML and CSS.

### Requirements
- [ ] URL input field (required)
- [ ] Title input field (required)
- [ ] Description textarea (optional)
- [ ] Category dropdown with options: Work, Personal, Learning, Entertainment
- [ ] Submit button
- [ ] Form is inside a card-like container

### HTML Structure
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

### CSS Hints
- Form container: `background: var(--color-surface)`, `padding: 24px`, `border-radius: var(--radius)`
- Inputs: `width: 100%`, `padding: 10px 12px`, `border: 1px solid var(--color-border)`
- Focus state: `outline: none`, `border-color: var(--color-primary)`
- Submit button: Same style as header button

### Acceptance Criteria
- [ ] All form fields are present and labeled
- [ ] Inputs have proper focus states
- [ ] Form looks like a card (shadow, rounded corners)
- [ ] Submit button matches the app's style

---

## Issue #3: Build the Bookmark Card

**Labels:** `week-1`, `html`, `css`, `difficulty:medium`

### Description
Create the bookmark card component. Build 4-6 example cards with hardcoded data.

### Requirements
- [ ] Favicon/icon placeholder (can be a colored div or emoji for now)
- [ ] Title as a clickable link
- [ ] URL (truncated if too long)
- [ ] Description (max 2 lines)
- [ ] Category badge
- [ ] Delete button

### HTML Structure (one card)
```html
<article class="bookmark-card">
  <div class="bookmark-icon">
    <!-- Placeholder: use a div with background color or an emoji -->
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

### Example Bookmarks to Create
1. GitHub - Work
2. YouTube - Entertainment
3. MDN Web Docs - Learning
4. Gmail - Personal
5. Stack Overflow - Learning
6. Netflix - Entertainment

### CSS Hints
- Card: `display: flex`, `gap: 12px`, `padding: 16px`
- Icon: `width: 40px`, `height: 40px`, `border-radius: var(--radius)`, `background: var(--color-primary-light)`
- URL truncation: `text-overflow: ellipsis`, `overflow: hidden`, `white-space: nowrap`
- Category badge: `display: inline-block`, `padding: 2px 8px`, `font-size: 0.75rem`
- Delete button: `opacity: 0.5`, on hover `opacity: 1`, `color: var(--color-danger)`

### Acceptance Criteria
- [ ] Cards display all required information
- [ ] Long URLs are truncated with ellipsis
- [ ] Description is limited to 2 lines
- [ ] Category badge is styled as a pill/tag
- [ ] Delete button is subtle but visible on hover
- [ ] Cards have hover effect (slight lift/shadow)

---

## Issue #4: Build the Sidebar

**Labels:** `week-1`, `html`, `css`, `difficulty:easy`

### Description
Create the sidebar with category navigation.

### Requirements
- [ ] "Categories" heading
- [ ] List of category links
- [ ] "All Bookmarks" should appear selected/active
- [ ] Hover states on links
- [ ] Fixed width (use `--sidebar-width` variable)

### HTML Structure
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

### CSS Hints
- Sidebar: `width: var(--sidebar-width)`, `background: var(--color-surface)`, `border-right: 1px solid var(--color-border)`
- Links: `display: block`, `padding: 10px 16px`, `color: var(--color-text)`
- Hover: `background: var(--color-bg)`
- Active: `background: var(--color-primary-light)`, `color: var(--color-primary-dark)`, `font-weight: 500`

### Acceptance Criteria
- [ ] Sidebar has fixed width
- [ ] All categories are listed
- [ ] "All Bookmarks" looks selected
- [ ] Hover effect on non-active items
- [ ] Clean spacing and typography

---

## Issue #5: Create the Main Layout

**Labels:** `week-1`, `html`, `css`, `difficulty:medium`

### Description
Set up the CSS Grid layout for the bookmark cards. This works alongside Issue #3.

### Requirements
- [ ] Responsive grid that adjusts columns based on screen width
- [ ] Consistent gap between cards
- [ ] Cards should be minimum 300px wide
- [ ] Maximum 3-4 cards per row on large screens

### CSS Implementation
```css
.bookmark-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 16px;
}
```

### Additional Tasks
- [ ] Add proper padding to `.main-content`
- [ ] Style the `.section-title` heading
- [ ] Ensure content doesn't get too wide (max-width)

### Acceptance Criteria
- [ ] Grid adapts from 1 to 3+ columns based on width
- [ ] Cards don't stretch too wide
- [ ] Consistent spacing throughout
- [ ] Section title is styled nicely

---

## Issue #6: Add Responsive Design (BONUS)

**Labels:** `week-1`, `css`, `difficulty:hard`, `bonus`

### Description
Make the bookmark manager work well on tablets and mobile devices.

### Requirements

#### Tablet (max-width: 768px)
- [ ] Reduce sidebar width or hide it
- [ ] Grid shows 1-2 columns

#### Mobile (max-width: 480px)
- [ ] Hide sidebar completely (we'll add a hamburger menu later)
- [ ] Full-width header with stacked elements if needed
- [ ] Single column grid
- [ ] Form inputs stack vertically
- [ ] Adjust font sizes and padding

### CSS Structure
```css
@media (max-width: 768px) {
  .sidebar {
    width: 200px;
  }

  .bookmark-grid {
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  }
}

@media (max-width: 480px) {
  .sidebar {
    display: none;
  }

  .app-container {
    flex-direction: column;
  }

  .bookmark-grid {
    grid-template-columns: 1fr;
  }

  .header {
    padding: 12px 16px;
  }
}
```

### Acceptance Criteria
- [ ] No horizontal scrolling on mobile
- [ ] All content is readable on small screens
- [ ] Touch targets are at least 44px
- [ ] Layout looks intentional, not broken

---

## How to Claim an Issue

1. Comment on the issue: "Claiming this with @partner-username"
2. Create a branch: `git checkout -b week1/issue-number-short-description`
   - Example: `week1/1-header`
3. Make your changes
4. Push and create a PR
5. Request review from another pair

## Questions?

Drop them in the issue comments or ask in Discord!
