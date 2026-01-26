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

### Acceptance Criteria
- [ ] Header spans full width
- [ ] Logo on left, button on right
- [ ] Button has hover effect (darker shade)
- [ ] Looks clean and professional

**Stuck?** Try the hints in `docs/hints/week1/issue-1-header.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-1-header/index.html` in your browser.

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

### Acceptance Criteria
- [ ] All form fields are present and labeled
- [ ] Inputs have proper focus states
- [ ] Form looks like a card (shadow, rounded corners)
- [ ] Submit button matches the app's style

**Stuck?** Try the hints in `docs/hints/week1/issue-2-form.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-2-form/index.html` in your browser.

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

### Example Bookmarks to Create
1. GitHub - Work
2. YouTube - Entertainment
3. MDN Web Docs - Learning
4. Gmail - Personal
5. Stack Overflow - Learning
6. Netflix - Entertainment

### Acceptance Criteria
- [ ] Cards display all required information
- [ ] Long URLs are truncated with ellipsis
- [ ] Description is limited to 2 lines
- [ ] Category badge is styled as a pill/tag
- [ ] Delete button is subtle but visible on hover
- [ ] Cards have hover effect (slight lift/shadow)

**Stuck?** Try the hints in `docs/hints/week1/issue-3-card.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-3-card/index.html` in your browser.

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

### Acceptance Criteria
- [ ] Sidebar has fixed width
- [ ] All categories are listed
- [ ] "All Bookmarks" looks selected
- [ ] Hover effect on non-active items
- [ ] Clean spacing and typography

**Stuck?** Try the hints in `docs/hints/week1/issue-4-sidebar.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-4-sidebar/index.html` in your browser.

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

### Additional Tasks
- [ ] Add proper padding to the main content area
- [ ] Style the section title heading
- [ ] Ensure content doesn't get too wide (max-width)

### Acceptance Criteria
- [ ] Grid adapts from 1 to 3+ columns based on width
- [ ] Cards don't stretch too wide
- [ ] Consistent spacing throughout
- [ ] Section title is styled nicely

**Stuck?** Try the hints in `docs/hints/week1/issue-5-layout.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-5-layout/index.html` in your browser - resize the window!

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

### Acceptance Criteria
- [ ] No horizontal scrolling on mobile
- [ ] All content is readable on small screens
- [ ] Touch targets are at least 44px
- [ ] Layout looks intentional, not broken

**Stuck?** Try the hints in `docs/hints/week1/issue-6-responsive.md` - start with Hint 1!

**See it working:** Open `frontend/examples/issue-6-responsive/index.html` in your browser - resize to see breakpoints!

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
