# UI Components Library

**Pure CSS component set** — buttons, cards, forms.  
Zero dependencies. Accessible. Ready to drop into any project.

[![Pure CSS](https://img.shields.io/badge/CSS-Pure-4f46e5?style=flat-square)](./css)
[![No JS required](https://img.shields.io/badge/JS-Not%20required-10b981?style=flat-square)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](./LICENSE)

---

## Live Demo

Open [`index.html`]([index.html](https://hanybin.github.io/ui-components-library/)) in a browser to see the full style guide.

> **Preview (what recruiters see first)**  
> Clean typography, consistent spacing, visible focus states, multiple variants and real form patterns — not just “pretty buttons”.

---

## What’s included

| Component | Variants / Features |
|-----------|---------------------|
| **Buttons** | Primary, Secondary, Success, Danger, Warning, Outline, Ghost, Soft · sizes (sm / default / lg) · loading · disabled · icon · full-width |
| **Cards** | Basic, Elevated, Accent, Stat, Profile · hoverable · header / body / footer slots · badges |
| **Forms** | Text, Email, Select, Textarea · input groups · checkboxes · radios · switch · error / success / disabled states · hints & labels |

All styles are driven by **CSS custom properties** (design tokens). Change the brand color in one place.

---

## Quick start

```html
<link rel="stylesheet" href="css/styles.css" />
```

```html
<!-- Button -->
<button class="btn btn--primary">Save</button>
<button class="btn btn--outline btn--sm">Cancel</button>

<!-- Card -->
<article class="card card--hoverable">
  <div class="card__header">
    <h3 class="card__title">Project name</h3>
    <span class="badge badge--primary">Active</span>
  </div>
  <div class="card__body">
    <p class="card__text">Short description of the project.</p>
  </div>
  <div class="card__footer">
    <button class="btn btn--primary btn--sm">Open</button>
  </div>
</article>

<!-- Form field -->
<div class="form-group">
  <label class="form-label" for="email">Email <span class="required">*</span></label>
  <input class="form-input" type="email" id="email" placeholder="you@company.com" />
  <span class="form-hint">We’ll never share your email.</span>
</div>
```

---

## Structure

```
ui-components-library/
├── index.html          # Live style guide / demo
├── css/
│   ├── styles.css      # Entry point (imports the rest)
│   ├── base.css        # Tokens, reset, layout helpers
│   ├── buttons.css
│   ├── cards.css
│   └── forms.css
├── README.md
└── LICENSE
```

You can import only the files you need, or use `styles.css` for everything.

---

## Customization

All design tokens live in `:root` inside `base.css`:

```css
:root {
  --color-primary: #4f46e5;
  --color-primary-hover: #4338ca;
  --radius-md: 0.5rem;
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
  /* … */
}
```

Override them in your project to match your brand. Dark mode is prepared via `html.dark` (toggle the class on `<html>`).

---

## Accessibility notes

- Visible `:focus-visible` rings on interactive elements
- Proper label / input associations
- Disabled states use `disabled` + reduced opacity (not just color)
- Loading buttons keep structure and announce via `aria` when you add it
- Color contrast aims for WCAG AA on primary surfaces

---

## Browser support

Modern evergreen browsers (Chrome, Firefox, Safari, Edge).  
Uses CSS custom properties, `gap`, `aspect-ratio`, and logical properties.

---

## Why this exists

A focused, production-quality pure-CSS library that demonstrates:

- Systematic design tokens
- Consistent spacing & typography scale
- Component API that is predictable (BEM-like modifiers)
- Attention to states (hover, focus, disabled, error, loading)
- Clean, readable code with zero build step

Suitable as a portfolio piece or as a lightweight starting point for small projects and prototypes.

---

## License

MIT — free for personal and commercial use.
