# MADE 2026 — Handmade Bicycle Show (fan site)

A small static website: a landing page plus 10 linked pages for the "top 10 bikes".

## Open it

Double-click `index.html`, or for best results (so the animations and
cross-page transitions behave exactly right) serve the folder:

```
cd "made-2026-bike-show"
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

```
made-2026-bike-show/
├── index.html            landing page
├── bikes/
│   └── bike-01.html … bike-10.html
├── css/styles.css        single external stylesheet
├── js/main.js            single external script
└── images/               original SVG artwork (see below)
```

## About the images

All artwork in `images/` is **original vector illustration** made for this
site (bikes, the Zidell Yards hero scene, show floor, bike valet, logo).
No real photographs are used, so there are no licensing issues.

To use real photos instead, drop `.jpg`/`.webp` files into `images/` and
update the matching `<img src="…">` in `index.html` and the `bikes/*.html`
pages (or just overwrite e.g. `bike-01.svg` with `bike-01.jpg` and change
the extension in the HTML).

## Colour theme

Defined as CSS custom properties at the top of `css/styles.css`:
orange `#d1611f`, brown `#4a3327` / `#2b1d15`, grey `#8f8a80` / `#e4ddce`,
black `#16130f`, warm paper `#f2ece1`.

## Features

- Sticky header, animated underline nav, scroll-progress bar
- Full-bleed animated hero with parallax
- Reveal-on-scroll, animated stat counters, builder marquee
- **Cross-page transition:** clicking through to a bike page plays a
  full-screen "MADE" wipe
- Bike pages: prev / next paging plus ← / → arrow-key navigation
- Respects `prefers-reduced-motion`
- Responsive down to mobile (hamburger menu under 860px)

## Note

Unofficial, non-commercial fan project / web-design exercise. Builder
names, specs, prices and quotes are editorial and illustrative — not
official announcements from MADE or any manufacturer.
