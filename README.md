# proof.hendrick.net Static Site

Static proof assets for Michael Hendrick.

## Current Pages

- `testimonials/` - selected colleague testimonials grouped by theme.

## Local Preview

Open `testimonials/index.html` directly in a browser, or run a local static server from this directory:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/testimonials/`.

## Deploy Notes

This folder can deploy as a static site root to Cloudflare Pages, GitHub Pages, Netlify, or any static host.

Suggested production route:

- Domain: `proof.hendrick.net`
- Page path: `/testimonials/`
- Static root: `proof-site`
- CNAME file: included for GitHub Pages-style hosting

For Cloudflare Pages, use:

- Build command: none
- Output directory: `proof-site` if deploying from the parent repo, or `/` if this folder is the repo root.
