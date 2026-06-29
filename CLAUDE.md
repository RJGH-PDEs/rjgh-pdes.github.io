# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static academic portfolio website for Rodrigo Gonzalez, deployed via GitHub Pages at `git@github.com:RJGH-PDEs/rjgh-pdes.github.io.git`. No build step, no dependencies — plain HTML/CSS/JS served directly by GitHub Pages.

## Deployment

Push to `main` to deploy. GitHub Pages serves `index.html` from the repo root automatically.

## Structure

- `index.html` — single-page site with anchor-linked sections: About, Research, Publications, Notes, CV
- `css/style.css` — all styles; uses CSS custom properties defined in `:root` for colors, typography, and layout
- `js/main.js` — footer year injection and mobile hamburger nav toggle
- `assets/` — PDFs (CV, papers, notes) and profile photo; files here are linked directly from `index.html`

## Content conventions

- **Publications**: add `<li class="pub-item">` entries inside `.pub-list` in `index.html`; each item contains `.pub-title`, `.pub-authors`, `.pub-venue`, and `.pub-links` spans
- **Notes**: add `<li class="note-item">` entries inside `.notes-list`; each has a `.note-main` div and a `.note-pdf` link
- **Assets**: drop PDFs into `assets/` and link with a relative path (e.g., `href="assets/filename.pdf"`)
- Alternating section backgrounds use the `.alt-bg` class (applies `--bg-alt`)

## Responsive design

The hamburger nav and single-column stacking kick in at `max-width: 640px` via a single media query at the bottom of `style.css`.
