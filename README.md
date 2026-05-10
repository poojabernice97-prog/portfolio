# Pooja Bernice — Portfolio

A single-page personal portfolio website for **Pooja Bernice Janarathinam**, a Project Manager based in Seattle, WA. Built as a self-contained HTML file with embedded CSS and JavaScript — no build step, no dependencies.


## Features

- **Single-file deployment** — one `.html` file, no bundler, no `node_modules`
- **Custom cursor** with hover-state animations
- **Sticky navigation** that changes appearance on scroll
- **Reveal-on-scroll animations** powered by `IntersectionObserver`
- **Testimonial carousel** with prev/next arrows, dot navigation, autoplay, and viewport-aware scroll clamping (no ghost cards)
- **Filterable portfolio grid**
- **Mouse-parallax orbs** in the hero section
- **Animated skill bars**
- **Direct mailto + resume download** in the contact section
- **Responsive layout** for desktop and mobile

## Tech stack

| Layer | Tools |
|---|---|
| Markup | HTML5 |
| Styling | Vanilla CSS (custom properties, flexbox, grid) |
| Behavior | Vanilla JavaScript (no frameworks) |
| Fonts | Google Fonts — DM Sans, Syne, DM Serif Display |
| Assets | Inline SVG noise texture, emoji icons |

## File structure

```
.
├── Pooja_Bernice_Portfolio.html   # The entire site
├── Pooja Bernice.pdf              # Resume served by the "Download Resume" button
└── README.md
```

The resume PDF must live in the same directory as the HTML file (or you'll need to update the `href` on the Download Resume button).

## Running locally

No install required. Either:

```bash
# 1. Open directly
start Pooja_Bernice_Portfolio.html       # Windows
open  Pooja_Bernice_Portfolio.html       # macOS
xdg-open Pooja_Bernice_Portfolio.html    # Linux
```

Or serve it over HTTP for the most accurate behavior (the `download` attribute and some browser features prefer this):

```bash
# Python 3
python -m http.server 8000

# Node (npx)
npx serve .
```

Then visit `http://localhost:8000`.

## Customization

All sections live inside `Pooja_Bernice_Portfolio.html`. Common edits:

| What to change | Where |
|---|---|
| Color theme | `:root { --bg, --p1, --c1, … }` block in `<style>` |
| Email address | `mailto:` link in the `#contact` section |
| Resume file | `href` on the "Download Resume" `<a>` tag |
| Testimonials | `<div class="testi-card">` blocks inside `#testimonials` |
| Nav links | `<ul>` inside `<nav>` |
| Hidden sections | Currently `#events` and `#blog` are wrapped in HTML comments |

## Browser support

Tested on the latest versions of Chrome, Edge, Firefox, and Safari. Uses modern CSS (custom properties, `:has()`, `backdrop-filter`) — IE is not supported.

## License

Personal portfolio. All content and copy © Pooja Bernice Janarathinam.
