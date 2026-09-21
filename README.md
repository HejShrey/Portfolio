# Shreyas Gowda Marigowda — Portfolio

Personal portfolio website: an extended, interactive version of my CV covering experience,
projects, skills, education and certifications.

**Live site:** https://hejshrey.github.io/Portfolio/

---

## What's in here

```
index.html                 the whole site (single scrolling page)
assets/
  css/style.css            dark technical theme
  js/main.js               nav, scroll reveal, counters, project filters, modal
  img/profile.jpg          ← add your portrait here (optional, falls back to a monogram)
  docs/                    ← PDFs linked from the site (see list below)
.nojekyll                  tells GitHub Pages to serve the files as-is
```

No build step, no dependencies, no framework. Plain HTML/CSS/JS — edit and push.

---

## Files you need to add

### 1. Portrait photo (optional)

Drop a square-ish photo at `assets/img/profile.jpg`.
If the file is missing the hero card shows an "SG" monogram instead, so the site never breaks.

### 2. PDFs

Copy your PDFs into `assets/docs/` using **exactly** these names:

| Save as                             | Source file                              |
|-------------------------------------|------------------------------------------|
| `Shreyas-Gowda-Marigowda-CV.pdf`    | Resume_Shreyas GM.pdf                    |
| `transcript.pdf`                    | Transcript.pdf                           |
| `universal-robots.pdf`              | Universal Robots Certificates.pdf        |
| `bosch-rexroth-iat.pdf`             | IAT_Bosch.pdf                            |
| `siemens-nx.pdf`                    | SIEMENS.pdf                              |
| `plc-scada.pdf`                     | PLC  SCADA Certificate.pdf               |
| `plc-fundamentals-l1.pdf`           | PLC Fundamentals Level 1.pdf             |
| `ptc-creo.pdf`                      | PTC Creo.pdf                             |
| `python.pdf`                        | Python.pdf                               |
| `anstallningsbetyg-wiksfors.pdf`    | Annställningsbetyg - Shreyas Gowda.pdf   |
| `tjanstgoringsintyg-wiksfors.pdf`   | Tjänstgöringsintyg - Shreyas Gowda.pdf   |
| `yuken.pdf`                         | Yuken.pdf                                |

Plain ASCII names (no spaces, no å/ä/ö) keep the URLs clean and avoid encoding problems on GitHub Pages.

---

## Publishing

```bash
git add .
git commit -m "Add portfolio site"
git push
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch →
Branch: `main` / `(root)` → Save.** The site goes live at
`https://hejshrey.github.io/Portfolio/` within a minute or two.

> Want the shorter URL `https://hejshrey.github.io/`? Create a second repository named
> exactly `HejShrey.github.io` and push these same files there.

---

## Editing content

Everything is written directly in `index.html`, in labelled sections:

| Section          | Where                                        |
|------------------|----------------------------------------------|
| Hero / intro     | `<section class="hero">`                     |
| About            | `id="about"`                                 |
| Experience       | `id="experience"` — each job is an `<li class="tl-item">` |
| Projects         | `id="projects"` — each is an `<article class="proj">`     |
| Skills           | `id="skills"`                                |
| Education        | `id="education"`                             |
| Certifications   | `id="certifications"`                        |
| Contact          | `id="contact"`                               |

### Adding a project

Copy any existing `<article class="proj">` block and change:

- `data-tags` — any of `simulation plc robotics software academic` (space separated; drives the filter buttons)
- `data-video` — a YouTube video **ID** only (e.g. `OggnjA84u7k`), or leave empty for no video
- the visible summary, and the `<div class="proj-detail" hidden>` block, which is what
  the pop-up shows

### Changing the colours

All colours are CSS variables at the top of `assets/css/style.css` (`--accent`, `--bg`,
`--surface`, …). Change `--accent` and the whole site follows.

---

## Local preview

Double-click `index.html`, or serve it properly:

```bash
python -m http.server 8000
# then open http://localhost:8000
```
