# SpireX Sidebar - Documentation

This document provides a deeper explanation of the components and customization points for the **SpireX Sidebar** demo.

## Components

### 1) Sidebar (HTML)

Defined in `index.html`:

- Wrapper: `<div class="sidebar" id="sidebar">`
- Title: `<h2>coderajay</h2>`
- Navigation: list of links using Font Awesome icons

### 2) Toggle Button (HTML)

Defined in `index.html`:

- `<button class="toggle-btn" id="toggleBtn">`
- Uses an icon: `<i class="fa-solid fa-bars"></i>`

### 3) Main Content Area (HTML)

Defined in `index.html`:

- `<div class="content"> ... </div>`

Currently, the “content” area only contains the toggle button. You can add your page content here.

## Styling / Layout (CSS)

All styling lives in `style.css`.

### Sidebar behavior

- Hidden state: `.sidebar { left: -250px; }`
- Visible state: `.sidebar.active { left: 0; }`
- Animation: `transition: left 0.3s ease;`

### Toggle button

- Fixed positioning: `.toggle-btn { position: fixed; bottom: 20px; left: 20px; }`
- Circular button with shadow and hover scale

### Responsive behavior

At `max-width: 768px`:

- Sidebar width becomes `200px`

> Note: If you change sidebar width, make sure the hidden offset (`left: -...px`) matches the new width.

## Interactivity (JavaScript)

Implemented in `script.js`:

- Gets references:
  - `sidebar = document.getElementById("sidebar")`
  - `toggleBtn = document.getElementById("toggleBtn")`
- Adds click handler:
  - `sidebar.classList.toggle("active")`

This is a simple and reliable pattern: CSS handles the animation; JS only toggles the class.

## Customization Guide

### Add real pages

Replace `href="#"` with real routes/links.

### Add sections / nested navigation

You can add nested lists, section headers, or badges inside the sidebar.

### Change animation direction

To slide from the right instead of left, you can:

- Set `.sidebar` to use `right` instead of `left`
- Update the hidden and active positions accordingly

### Improve accessibility

Recommended improvements:

- Add `aria-label` to the toggle button
- Add focus styles for links
- Ensure sufficient color contrast

## Known Limitations

- Sidebar links currently point to `#` (placeholders).
- Content area is minimal; you’ll likely want to expand it.

## Contribution

Pull requests are welcome—please open an issue first for major changes.
