Headphones Landing Page

Implementation of the Headphones responsive web page from the ALX HTML/CSS project.

Project overview

This repository contains a pixel-perfect implementation of the "Headphones" single-page design by Nicolas Philippot. The goal is to recreate the layout, typography, spacing, and interactions exactly as shown in the designer file using only HTML and CSS (no JavaScript, no CSS frameworks).

Key constraints & goals:

No external CSS frameworks (Bootstrap, Tailwind, etc.)

No JavaScript — pure HTML and CSS only

Fully responsive: switch to the mobile version at 480px or less

Max content width: 1000px, centered

Hover / active color for links: #FF6565

Button hover / active: opacity: 0.9

Accessibility best practices (semantic HTML, keyboard focus, ARIA where appropriate)

Fonts

The design uses:

Source Sans Pro (UI text)

Spin Cycle OT (display / logo / accents)

If you don’t have these fonts installed locally, use the supplied Figma assets or add webfont files to the project. For development you can substitute with a similar system font (e.g. system-ui, Inter, Arial) but keep the final assets to match the designer exactly.

Repository structure

alx_html_css/
└── headphones/
    ├── index.html            # main page
    ├── styles.css            # project stylesheet
    ├── assets/               # images, logos, icons, fonts (if supplied)
    │   ├── fonts/
    │   └── images/
    ├── README.md             # this file
    └── accessibility-notes.md (optional)

How to run (development)

Clone the repo and open the headphones folder.

Open index.html in your browser (double-click or Live Server in VS Code).

Resize the browser window to verify the responsive breakpoints, especially the mobile layout at ≤480px.

Implementation notes

Use semantic elements: <header>, <nav>, <main>, <section>, <article>, <footer>.

Keep the content width constrained with a centered container .container { max-width: 1000px; margin: 0 auto; }.

Prefer CSS Grid for the overall layout and Flexbox for smaller components (buttons, nav, lists).

Round floating values to the nearest pixel where necessary; minor rounding differences from the Figma file are acceptable.

Hover and focus states must be visible and match the color cues from the design.

Accessibility checklist

Use appropriate alt text for images.

Ensure sufficient color contrast for text and interactive elements.

Provide :focus styles for keyboard navigation and ensure tab order is logical.

Use aria-label or visually-hidden text for icon-only buttons/links.

Use lang="en" on <html> and set meta viewport for responsive scaling.

Responsive behavior & breakpoints

Mobile: max-width: 480px — switch to the mobile-specific layout as in the design

Tablet / Desktop: adapt layout above 480px — main content centered with max-width: 1000px

Media queries example:

@media (max-width: 480px) {
  /* mobile layout adjustments */
}

Interactions & states

Link hover/active color: #FF6565.

Buttons on hover/active: reduce opacity to 0.9.

Ensure cursor: pointer on clickable elements and aria-pressed/aria-expanded if using toggles.

Testing recommendations

Test in latest Chrome, Firefox, Safari, and Edge.

Test keyboard-only navigation (Tab, Shift+Tab, Enter, Space).

Inspect at common device widths: 320px, 375px, 430px, 480px, 768px, 1024px.

Validate HTML (validator.w3.org) and run CSS through a linter for maintainability.

Submission

Ensure index.html, styles.css and the assets/ folder are committed.

Include screenshots of desktop and mobile results in the repo (optional but recommended).

Credits

Design: Nicolas Philippot — find the final screens on the Figma project provided by ALX.
