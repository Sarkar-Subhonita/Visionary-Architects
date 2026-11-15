# Visionary Architects

A responsive, single-page website for a fictional architecture firm. It's a front-end only project written in plain HTML, CSS and JavaScript, with a few small libraries for smooth scrolling and scroll animations. No framework, no build step, no backend.

The look is clean and editorial: a big headline, large photography, generous spacing and a custom heading font.

## What's on the page

Everything lives in one page, `index.html`:

1. **Navigation.** Logo, links (Home, Studio, Services, Contact, FAQ) and a "Let's talk" button. On small screens it collapses into a hamburger menu that slides in from the right.
2. **Intro.** The main headline, a short pitch, two featured project images and a "View Projects" button.
3. **About.** A short write-up of the studio.
4. **Stats.** Three animated counters (Odometer) that count up the first time they scroll into view, followed by a row of image cards.
5. **Portfolio.** A grid of featured design images.
6. **Brands.** A logo strip of eight partner brands.
7. **Footer.** Social links, an email field and a copyright line.

## Features

- **Smooth scrolling.** Lenis gives the page an eased, inertial scroll. It pauses while the mobile menu is open so the page behind doesn't move.
- **Scroll reveal animations.** WOW.js triggers Animate.css effects (fade up, fade left, fade right) as sections come into view.
- **Count-up stats.** The numbers start at 0 and roll up to their values once, the first time the stats section is visible.
- **Responsive layout.** Bootstrap's grid handles the structure, and custom media queries adapt the design at 1080px, 992px, 800px, 768px, 576px and 420px.
- **Custom fonts.** Cabinet Grotesk for headings and Nunito for body text, both loaded locally from the repo, so there's no Google Fonts dependency.

## Tech stack

- HTML5, CSS3, vanilla JavaScript
- Bootstrap grid (`bootstrap-grid.css` only, not the full framework)
- [Lenis](https://github.com/darkroomengineering/lenis) for smooth scroll
- [WOW.js](https://github.com/matthieua/WOW) and [Animate.css](https://animate.style/) for scroll animations
- [Odometer](https://github.hubspot.com/odometer/docs/welcome/) for the counters

## Getting started

Nothing to install. Every dependency is included in the folder.

```bash
cd Visionary-Architects-main

# Option A: open the file
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option B: serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

VS Code's Live Server extension also works well.

## Project structure

```
.
├── index.html          # The whole page, plus a small inline script
├── style.css           # All custom styles (~700 lines)
├── bootstrap-grid.css  # Bootstrap's grid utilities
├── animate.css         # Animate.css
├── odometer.css / odometer.js
├── wow.js
├── lenis.js
├── CabinetGrotesk.ttf  # Heading font
├── Nunito.ttf          # Body font
└── images/             # Project photos, brand logos, icons
```

The JavaScript that ties things together sits in a `<script>` block at the bottom of `index.html`. It starts WOW.js and Lenis, triggers the counters when the stats section is visible, and handles the mobile menu toggle.

## Customising it

- **Text and images.** Edit `index.html` directly. Images are in `images/`, so replace them with files of the same name or update the `src` attributes.
- **Colours, fonts and spacing.** Everything is in `style.css`.
- **Stats.** Change the `data-value` attribute on each `.odometer` element. The labels next to them ("Happy Sellers", "Shipments Daily", "App Rating") are leftovers from another template and don't suit an architecture firm, so they need rewording.
- **Contact details.** The "Let's talk" and "Submit" buttons use `mailto:` links and the footer social links point to the original author's accounts. Replace these before publishing it as your own site.

## Known gaps

- **The newsletter field doesn't do anything.** The footer's email input isn't connected to anything. "Submit" just opens a `mailto:` link, ignoring what was typed.
- **Most links are placeholders.** The Studio, Services, Contact and FAQ links, and the "View Projects" and "View More" buttons, point to `#`, so the site is effectively one page for now.
- **Accessibility.** Images have empty `alt` text and the nav has no skip link, so a pass for alt text and keyboard navigation would help.
- **Typo.** The nav says "FAQ`s" with a stray backtick.
- **No meta tags.** There's no description, Open Graph or viewport-based SEO setup beyond the basics.

## Credits

This project was created by **Ashutosh Kumar** ([codeaashu](https://github.com/codeaashu)), and the original repository is [codeaashu/Visionary-Architects](https://github.com/codeaashu/Visionary-Architects). The design was based on Figma and Pinterest references. All credit for the original design and code goes to him.

If you fork it or build on it, keep this credit in place and describe your own changes in the section below.

### My changes

<!-- Fill this in honestly with what you added or modified, for example:
- Fixed the nav typo and replaced placeholder stats
- Added a working contact form
- Deployed to Vercel
-->

## Licence

The original repository doesn't include a licence file, so by default all rights remain with the author. Check with the author before reusing it commercially. The bundled libraries (Lenis, WOW.js, Animate.css, Odometer, Bootstrap) keep their own licences. Photos in `images/` should be treated as placeholders.