# Daniele De Gregorio — Portfolio

Modern, self-contained single-file portfolio for Daniele De Gregorio, Systems Engineer at KLA and Physicist specializing in electron-beam metrology and nanophotonics.

**Live:** [https://masterdanny.github.io](https://masterdanny.github.io)

## Design

- Tailwind CSS via CDN (zero build step, GitHub Pages friendly)
- Dark-first scientific aesthetic (deep navy + teal/cyan accents)
- Fully responsive, accessible, SEO-optimized
- Subtle micro-interactions and scroll reveals (vanilla JS only)
- All content preserved from previous version with enhanced scannability for recruiters

## Local development

```bash
# Serve locally
python3 -m http.server 8080
# or
npx serve .
```

Open http://localhost:8080

## Deployment (GitHub Pages)

1. (Optional for now) Generate a professional 1–2 page CV and export as `Daniele_De_Gregorio_CV.pdf` (place in repo root).  
   **Note:** The Download CV buttons have been temporarily removed from the live site. You can still prepare the file — it will be easy to re-enable later.
2. (Strongly recommended) Create a custom 1200×630 social preview image and update the `og:image` tag.
3. (Optional) Replace `images/profile.jpg` with an updated headshot.
4. Commit & push to `main`.
4. In GitHub → Settings → Pages: Source = **Deploy from a branch** → `main` / `(root)`.
5. Visit https://masterdanny.github.io (allow ~60s for CDN).

See the `<!-- DEPLOYMENT INSTRUCTIONS -->` comment block at the top of `index.html` for the complete checklist (including how to re-add the CV buttons later).

## Tech stack

- Single `index.html` (≈ 850 lines)
- Tailwind 3.x (CDN)
- Vanilla JS (mobile menu, copy-to-clipboard, scrollspy, reveals)
- Font Awesome 6 (CDN icons)
- All PDFs and images remain in `theses/` and `images/`

## New Features Added

- **Dark / Light mode toggle** (persisted in localStorage + respects system preference)
- **Privacy-friendly analytics ready** (Plausible recommended — just uncomment the script)
- **Improved SEO** (better meta + JSON-LD structured data)
- **Proper favicon** + refined KLA logo treatment
- **Custom OG image guidance** (highly recommended for sharing)

## Future improvements (optional)

- Real contact form (Formspree / Web3Forms)
- Re-enable Download CV buttons + add real CV.pdf + print-optimized view
- Custom high-quality social preview image (1200×630)
- Subtle canvas background (optional)

---

Built with precision. Open to senior roles in semiconductor metrology, photonics hardware, and deep-tech systems engineering.
