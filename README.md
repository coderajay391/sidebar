# SpireX Sidebar

A lightweight, responsive sidebar + toggle button demo built with **HTML, CSS, and vanilla JavaScript**.

## Demo / Preview

- Open `index.html` in a browser.

## Features

- Slide-in sidebar (hidden by default, appears when toggled)
- Toggle button fixed at the bottom-left
- FontAwesome icons for the navigation links
- Simple, clean structure that can be reused in other projects

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript (DOM + class toggling)
- Font Awesome (CDN)
- Google Font: **Poppins**

## How it works

- `script.js` listens for a click on the toggle button.
- When clicked, it toggles the `active` class on the sidebar element.
- `style.css` changes the sidebar position from `left: -250px` to `left: 0` when `.sidebar.active` is present.

## Preview
<image src="./assets/sidebar1.png"></image>
<image src="./assets/sidebar2.png"></image>

## Demo
[Demo](assets/sidebar.mp4)

## File Structure

```
frontend/spireX/sidebar/
├── index.html     # Page markup (sidebar + content + button)
├── style.css      # Styling and animations
├── script.js      # Toggle logic
└── assets/        # Optional static files (currently empty)
```

## Setup / Run

1. Go to: `frontend/spireX/sidebar/`
2. Open `index.html` in any browser.

> No build step or dependencies are required (beyond the CDN links in `index.html`).

## Customization

### Update sidebar links

Edit the navigation in `index.html`:

- Replace the `<a href="#"> ... </a>` entries inside the `.sidebar`.

### Change the sidebar width

In `style.css`, update:

- `.sidebar { width: ... }`
- `.sidebar { left: -... }` (the hidden offset should match the width)

### Change toggle button position/style

In `style.css`, update the `.toggle-btn` rules:

- `left` / `bottom`
- `background`, `box-shadow`, hover effects, etc.

## Accessibility notes

- Consider replacing `button` icon-only UI with an accessible label, e.g. `aria-label="Toggle sidebar"`.
- If you add real pages/links, use meaningful `href` values instead of `#`.

## Troubleshooting

- If icons do not load: ensure you have internet access for the Font Awesome CDN.
- If the sidebar doesn’t toggle: verify `script.js` is correctly referenced in `index.html`.

## Contribution

Pull requests are welcome—please open an issue first for major changes.
