# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll blog using the [Lanyon](http://lanyon.getpoole.com) theme (built on [Poole](https://github.com/poole)). It is deployed via GitHub Pages on the `gh-pages` branch to treymoore.me.

## Build & Serve

```bash
jekyll serve          # Local dev server at http://localhost:4000
jekyll build          # Build static site to _site/
```

## Architecture

- **Layouts** (`_layouts/`): Three-tier layout hierarchy — `post` and `page` both extend `default`
- **Includes** (`_includes/`): `head.html` (meta/CSS) and `sidebar.html` (toggleable nav, auto-generates links for all pages with `layout: page`)
- **Styling** (`public/css/`): `poole.css` (base), `lanyon.css` (theme/sidebar), `syntax.css` (code highlighting)
- **Content pages**: Use `layout: page` in front matter to auto-appear in sidebar nav
- **Blog posts**: Add to `_posts/` directory with `layout: post` front matter (paginated on index, 1 per page)

## Key Config (`_config.yml`)

- `baseurl`: `""` (templates use `{{ site.baseurl }}/...`); `url`: `https://treymoore.me`
- `paginate: 1` — one post per page on the index
- `permalink: pretty` — clean URLs
