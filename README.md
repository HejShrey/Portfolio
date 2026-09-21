# Shreyas Gowda Marigowda — Portfolio

**Live:** https://hejshrey.github.io/Portfolio/

The whole website is a single file: `index.html`. All styling and interaction is inside it —
no folders, no build step, nothing that can go missing during an upload.

## Files in this repo

```
index.html    the entire website
*.pdf         CV, transcript, certificates (linked from the page)
profile.png   portrait shown in the hero panel (optional)
.nojekyll     tells GitHub Pages to serve the files as-is
```

Everything sits at the top level on purpose. There are no subfolders to lose.

## PDFs — use these exact names

| Save as | Source file |
|---|---|
| `Shreyas-Gowda-Marigowda-CV.pdf` | Resume_Shreyas GM.pdf |
| `transcript.pdf` | Transcript.pdf |
| `universal-robots.pdf` | Universal Robots Certificates.pdf |
| `bosch-rexroth-iat.pdf` | IAT_Bosch.pdf |
| `siemens-nx.pdf` | SIEMENS.pdf |
| `plc-scada.pdf` | PLC  SCADA Certificate.pdf |
| `plc-fundamentals-l1.pdf` | PLC Fundamentals Level 1.pdf |
| `ptc-creo.pdf` | PTC Creo.pdf |
| `python.pdf` | Python.pdf |
| `yuken.pdf` | Yuken.pdf |

**Deliberately NOT in this repo:** the Wiksfors *Anställningsbetyg* and *Tjänstgöringsintyg*.
They contain a referee's direct contact details, so the page offers a
"Request the letters" button instead — it opens the visitor's email client with a
pre-filled message asking for them.

A missing PDF only breaks its own link — the rest of the page is unaffected.
Same for the portrait: the page tries `profile.png`, then `.jpg`, `.jpeg` and `.webp`,
and falls back to an "SG" monogram if none is there.

## Updating the site

Edit `index.html` and re-upload it to GitHub (drag it onto the repo page and commit).
GitHub replaces the old version and the live site updates within a minute.

## How it's built

- **Colour system:** industrial HMI signal colours, used as data rather than decoration.
  Each discipline owns a hue — simulation `#22D3EE`, PLC `#FFB020`, robotics `#FF5DA2`,
  software `#57E08A`, academic `#A78BFA` — and project cards, filters and skill panels
  all take their colour rail from the same set.
- **Type:** Familjen Grotesk (display) + IBM Plex Sans (body) + IBM Plex Mono (data),
  loaded from Google Fonts.
- **Projects:** each `<article class="p">` carries `data-cat` (its colour),
  `data-tags` (which filter buttons show it) and `data-video` (a YouTube video ID).
  The `<div class="detail">` block inside is what the pop-up displays.
- Respects `prefers-reduced-motion`, works down to 390px wide, and has a print stylesheet.
