# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static portfolio site for Harry Gomes — 3D Artist & Animator. Single-file HTML with all CSS and JavaScript inline. Hosted on GitHub Pages at https://sanches3d.github.io/portfolio/.

## Deploying changes

After any modification, push to GitHub to update the live site (takes 1–2 minutes to propagate):

```bash
git add -A && git commit -m "Mise a jour portfolio" && git push
```

No build step, no dependencies, no package manager.

## Architecture

Everything lives in `index.html` — styles, layout, and scripts are all inline. Media files are served from:
- `images/` — PNG product renders
- `videos/` — MP4 cinematic animations (autoplay on hover, lightbox on click)

Key sections in `index.html` (by anchor/id):
- `#travaux` — gallery grid (12-column, alternating 7/5 span layout)
- `#tarifs` — 3 pricing cards (Essentiel €45 / Pro Animation €120 / Full Cinéma €250)
- `#processus` — 4-step process
- `#contact` — Formspree form (`action="https://formspree.io/f/mbdqnjbr"`) + social links

## Adding media

New images go in `images/`, videos in `videos/`. Reference them with relative paths (`images/filename.png`, `videos/filename.mp4`). Never use absolute local paths (`C:/`, `D:/`, `file:///`).

## Contact form

Connected to Formspree (ID: `mbdqnjbr`). Messages are delivered to harry.gomessanches@gmail.com. Form fields have `name` attributes — add `name="..."` to any new inputs.
