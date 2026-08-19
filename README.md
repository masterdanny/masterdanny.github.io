# Daniele De Gregorio — Portfolio

Portfolio and Markdown blog for Daniele De Gregorio, Systems Engineer at KLA and Physicist specializing in electron-beam metrology and nanophotonics.

**Live:** [https://masterdanny.github.io](https://masterdanny.github.io)

## Design

- Tailwind CSS via CDN (no JS build step; GitHub Pages builds the blog with Jekyll)
- Dark-first scientific aesthetic (deep navy + teal/cyan accents)
- Fully responsive, accessible, SEO-optimized
- Subtle micro-interactions and scroll reveals (vanilla JS only)
- All content preserved from previous version with enhanced scannability for recruiters

## Local development

Jekyll expands the shared layout and Markdown posts. A static file server will not.

Needs Ruby 3.x (macOS system Ruby 2.6 is too old). On Homebrew:

```bash
brew install ruby@3.3
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000

Alternatively, from this repo with Docker:

```bash
docker run --rm -v "$PWD":/srv/jekyll -w /srv/jekyll -p 4000:4000 ruby:3.3 \
  bash -lc "bundle config set path vendor/bundle && bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

## Writing a post

Add a file under `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: Your title
description: One-line summary shown on the listing.
date: 2026-08-19
tags:
  - notes
---

Markdown body.
```

It is published at `/blog/slug/` on the next build.

## Deployment (GitHub Pages)

1. (Optional for now) Generate a professional 1–2 page CV and export as `Daniele_De_Gregorio_CV.pdf` (place in repo root).  
   **Note:** The Download CV buttons have been temporarily removed from the live site. You can still prepare the file — it will be easy to re-enable later.
2. (Strongly recommended) Create a custom 1200×630 social preview image and update the `og:image` tag.
3. (Optional) Replace `images/profile.jpg` with an updated headshot.
4. Commit & push to `main`.
4. In GitHub → Settings → Pages: Source = **Deploy from a branch** → `main` / `(root)`.
5. Visit https://masterdanny.github.io (allow ~60s for CDN).

See the `<!-- DEPLOYMENT INSTRUCTIONS -->` comment block in `_includes/head.html` for the complete checklist (including how to re-add the CV buttons later).

## Tech stack

- Jekyll via the `github-pages` gem (branch deploy from `main` / root)
- Homepage in `index.html`; shared chrome in `_includes/`
- Posts in `_posts/` (Markdown), listing at `/blog/`, RSS at `/feed.xml`
- Tailwind 3.x (CDN)
- Vanilla JS (mobile menu, copy-to-clipboard, scrollspy, theme)
- Font Awesome 6 (CDN icons)
- All PDFs and images remain in `theses/` and `images/`

## New Features Added

- **Dark / Light mode toggle** (persisted in localStorage + respects system preference)
- **Privacy-friendly analytics ready** (Plausible recommended — just uncomment the script)
- **Improved SEO** (better meta + JSON-LD structured data)
- **Proper favicon** + refined KLA logo treatment
- **Custom OG image guidance** (highly recommended for sharing)

## Future improvements (optional)

- Homepage teaser of the latest post
- Real contact form (Formspree / Web3Forms)
- Re-enable Download CV buttons + add real CV.pdf + print-optimized view
- Custom high-quality social preview image (1200×630)
- Subtle canvas background (optional)

---

Built with precision. Open to senior roles in semiconductor metrology, photonics hardware, and deep-tech systems engineering.
