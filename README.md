# Portfolio

My CV as a website.

**→ [hejshrey.github.io/Portfolio](https://hejshrey.github.io/Portfolio/)**

A printed CV has to fit on two pages. This doesn't — so it carries the full picture:
the projects behind each role, the hardware and software involved, demo videos, and
the certificates themselves.

## Why a static site

Hosting is free on GitHub Pages, there's nothing to maintain, and nothing can break
between me and a recruiter opening the link. Editing the page is editing one file.

## How it's built

- **One file.** `index.html` holds the markup, the CSS and the JavaScript. No framework,
  no build step, no dependencies to install.
- **Plain HTML, CSS and vanilla JS** — a sticky nav with scroll progress, filterable
  project cards, pop-up case studies with embedded video, and scroll-triggered reveals.
- **Colour carries meaning.** The palette is borrowed from industrial HMI signal colours,
  with one hue per discipline — simulation, PLC and controls, robotics, software, academic —
  so the colour rail on a project card tells you what kind of work it was before you read it.
- **Type:** Familjen Grotesk, IBM Plex Sans and IBM Plex Mono, served from Google Fonts.
- Responsive down to phone width, respects `prefers-reduced-motion`, and prints cleanly.

## Structure

```
index.html    the site
*.pdf         CV and certificates, linked from the page
profile.png   portrait
.nojekyll     serve the files as-is, no Jekyll processing
```
