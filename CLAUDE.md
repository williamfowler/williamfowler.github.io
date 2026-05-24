# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal website hosted on GitHub Pages. No build tools, no frameworks, no dependencies — pure HTML, CSS, and static assets served directly.

## Development

Open any `.html` file in a browser directly (file://) or use a local HTTP server:

```bash
python3 -m http.server 8000
```

No build, lint, or test steps exist.

## Architecture

Single CSS file ([css/style.css](css/style.css)) shared across all pages. Each HTML page hardcodes the nav bar — there is no templating or shared includes.

**Pages:**
- [index.html](index.html) — About/bio with profile photo
- [research.html](research.html) — Publications (PDF links) and projects (GitHub links)
- [resume.html](resume.html) — Embeds `resume.pdf` at project root (not yet added)

**Layout:** All pages use a centered `.container` (max-width 720px). One mobile breakpoint at 560px.

## Design

Minimalist black-and-white, inspired by ai-2027.com. Font is Georgia serif (18px, line-height 1.7). No color except black and white. The design spec is in [website_design_specifications.txt](website_design_specifications.txt).

**Content patterns in research.html:**
- Publications: `<li>` with linked title, italic author line, gray venue/year
- Projects: `.project-entry` div with `<h3>` linked title and description paragraph

## Deployment

Push to GitHub — the repo is set up for GitHub Pages (no build step needed, serves from root).
