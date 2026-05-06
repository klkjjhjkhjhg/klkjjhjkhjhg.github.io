# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal academic homepage (Lianghao Zhang) deployed to GitHub Pages. It is a static HTML site with no build system.

## Architecture

- **Single-page site**: All content is in [index.html](index.html) (525 lines)
- **CSS framework**: Bootstrap 4 via CDN ([css/](css/))
- **JavaScript**: jQuery 3.5.1 + Bootstrap JS + Popper ([js/](js/))
- **Assets**: Images in [imgs/](imgs/), fonts in [fonts/](fonts/)

## Development

This is a static site with no development server, build steps, or tests. To view locally, open `index.html` in a browser or serve with any static file server:

```bash
python3 -m http.server 8000
# or
npx serve .
```

## Deployment

The site deploys automatically to `https://klkjjhjkhjhg.github.io/` via GitHub Pages when changes are pushed to the `main` branch.
