# Rosi — Personal Landing Page

Personal portfolio homepage skeleton for GDGOC ITB Module 1 hands-on task.
Built with plain HTML5 and CSS — no frameworks.

## Structure

```
.
├── assets/
│   ├── logo-dark.png    
│   ├── logo-light.png   
│   └── profile.jpg     
├── index.html            
├── styles.css             
└── README.md
```

## Features

- **Semantic HTML5**: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- **Layout**: Flexbox for the header/hero/footer rows, CSS Grid for the skills section
- **Responsive**: breakpoints at 860px and 640px, tested down to mobile widths
- **Theme-aware logo**: swaps between a light and dark mark depending on the active theme
- **Bonus 1 — CSS variables + dark/light mode**: all colors are defined as custom
  properties in `:root`, overridden inside `body.light-mode`. Toggle button in the
  header swaps the class and persists the choice in `localStorage`.
- **Bonus 2 — Animation**: hero content fades/slides in on load (staggered), the
  nav links get an underline slide on hover, skill cards lift on hover, and the
  hero cursor blinks via `@keyframes`.
- **Bonus 3 — Lighthouse audit**: see below.

## Running locally

No build step needed — just open `index.html` in a browser, or serve it locally:

```bash
python3 -m http.server 5500
# then visit http://localhost:5500
```

## Lighthouse audit (Bonus 3)

Run this yourself once the site is live (e.g. via GitHub Pages) or served locally:

1. Open the page in Chrome.
2. Open DevTools (`F12` or `Ctrl+Shift+I`) → **Lighthouse** tab.
3. Select **Performance** and **Accessibility**, device: Mobile, then **Analyze page load**.
4. Record the "before" scores here, then optimize (e.g. compress/self-host fonts,
   add explicit image dimensions, double-check color contrast) and re-run for "after".
5. Paste both screenshots below.

**Before:**
`[screenshot placeholder — replace after running audit]`

**After:**
`[screenshot placeholder — replace after running audit]`

## Git workflow / commit hygiene

Suggested commit sequence for meaningful history:

```bash
git init
git add index.html styles.css
git commit -m "feat: add landing page skeleton with semantic HTML and CSS layout"

git add assets/
git commit -m "feat: add theme-aware logo and profile photo"

git commit -am "feat: revise hero layout, copy, and logo integration"

git branch -M main
git remote add origin https://github.com/rosianna-maria/portfolio-landing-page.git
git push -u origin main
```

## Roadmap

This landing page is the skeleton for a full portfolio site, to be expanded
module by module with a projects section, blog/writeups, and a resume page.