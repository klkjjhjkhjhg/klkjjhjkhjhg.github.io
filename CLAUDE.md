# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal academic homepage for Lianghao Zhang (Researcher at Xiaomi, Ph.D. from Tianjin University). The site showcases research publications in computer graphics and computer vision, focusing on material acquisition, appearance modeling, and 3D reconstruction.

## Architecture

- **Single-page site**: All content is in [index.html](index.html) (~310 lines)
- **CSS framework**: Bootstrap 4 via CDN ([css/](css/))
- **JavaScript**: jQuery 3.5.1 + Bootstrap JS + Popper ([js/](js/))
- **Assets**: Images in [imgs/](imgs/), fonts in [fonts/](fonts/)
- **Visitor analytics**: ClustrMaps widget for visitor location tracking

## Page Sections

- **Profile**: Name, affiliation (Xiaomi | Researcher), research area (Computer Graphics & Computer Vision), contact links (Email, GitHub)
- **About**: Introduction with research interests
- **Publications**: 9 papers with thumbnails, ACM official PDF links, project pages, author/venue info
- **Contact**: Email and GitHub links

## Development

This is a static site with no build steps or tests. To view locally:

```bash
python3 -m http.server 8000
# or
npx serve .
```

Then visit `http://localhost:8000`

## Deployment

The site deploys automatically to `https://klkjjhjkhjhg.github.io/` via GitHub Pages when changes are pushed to the `main` branch.

## Adding Publications

Each publication entry follows this structure:

```html
<div class="pub-item">
    <div class="row">
        <div class="col-md-2 text-center">
            <img class="pub-thumb" src="imgs/xxx.png" style="...">
        </div>
        <div class="col-md-10">
            <p class="pub-title">Paper Title</p>
            <p class="pub-meta">
                <a href="ACM_PDF_URL" class="pub-link">[PDF]</a>
                <a href="Project_URL" class="pub-link">[Project]</a>
            </p>
            <p class="pub-authors">Authors with <span class="author-self">Lianghao Zhang</span></p>
            <p class="pub-venue">Conference info</p>
        </div>
    </div>
</div>
```

## Adding Visitor Map

ClustrMaps tracking code is embedded before `</body>`:

```html
<script type="text/javascript" id="mapmyvisitors" src="https://mapmyvisitors.com/map.js?cl=080808&w=300&t=n&d=YOUR_DOMAIN_ID&co=ffffff&ct=808080&cmo=3acc3a&cmn=ff5353"></script>
```

Style parameters: `w=` (width), `cl=` (background color), `co=` (text color), etc.
