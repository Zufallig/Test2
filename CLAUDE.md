# CLAUDE.md

## Project Overview

This is a **static landing page** built on the "Namari" template (v1.1.0) by ShapingRain. It is a single-page website with HTML, CSS, and JavaScript — no build tools, no frameworks, no package manager.

## Repository Structure

```
.
├── index.html              # Single-page HTML (all sections inline)
├── style.css               # Core layout, grid system, responsive styles
├── namari-color.css        # Theme colors, typography, and button styling
├── font-awesome.css        # Font Awesome icon library (v4)
├── logo.png                # Site logo displayed in the banner
├── images/                 # Referenced but not committed (banner, user, company images)
└── js/                     # Referenced but not committed (jQuery, plugins, site.js)
```

### Key Files

- **`index.html`** — Contains all page sections: banner/header, about, services, testimonials, clients, pricing, and footer. Navigation uses anchor links (`#about`, `#services`, etc.).
- **`namari-color.css`** — The primary theming file. The accent color is `#d2b356` (gold). Edit this file to change colors, fonts, or typography.
- **`style.css`** — Core structural styles: grid system (`.col-1` through `.col-3`), responsive breakpoints, layout helpers (`.clearfix`, `.row`), and component styles.
- **`font-awesome.css`** — Font Awesome 4.x icon definitions. Do not edit manually.

## Page Sections (in order)

1. **Header/Banner** (`#banner`) — Logo, social icons, main nav, hero text with CTA button
2. **About** (`#about`) — Feature icons grid (HTML5, Easy to Use, Responsive, Parallax)
3. **Services** (`#services`) — Testimonial quote, content block, video CTA, dancer image
4. **Testimonials** (`#testimonials`) — Three customer quote cards
5. **Clients** (`#clients`) — Company logo grid (9 logos)
6. **Footer** (`#landing-footer`) — Copyright and social icons

## Conventions

- **No build step** — Open `index.html` directly in a browser or serve with any static file server.
- **Commit messages** — Historically written in French (e.g., "Ajout de nouveau style"). Follow the existing language convention or use English for new commits.
- **CSS organization** — Layout/structure in `style.css`, theming/colors in `namari-color.css`. Keep this separation.
- **Font** — Open Sans (loaded externally or via system fallback). Referenced throughout `namari-color.css`.
- **Accent color** — `#d2b356` (gold). Used for links, icons, borders, buttons hover, and active nav states. Change it in `namari-color.css` for a full theme swap.
- **JavaScript** — jQuery 1.8.3 with plugins (WOW.js, Featherlight, Enllax, ScrollUp, Easing, StickyNavbar, Waypoints). Scripts are referenced from a `js/` directory.

## Development Notes

- **Missing assets** — The `images/` and `js/` directories are referenced in the HTML/CSS but are not committed to the repository. The page will have broken images and no JS interactivity without them.
- **No linter, formatter, or test suite** — This is a plain static site with no tooling.
- **Responsive** — The CSS includes media queries in `style.css` for mobile/tablet breakpoints.

## Gotchas

- There is an HTML nesting issue near line 372 of `index.html`: a stray closing `</div>` and `</section>` for a pricing section that was removed but whose closing tags remain.
- `font-awesome.css` is a vendored file — do not modify it directly.
