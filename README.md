# proof.hendrick.net Static Site

Static proof assets for Michael Hendrick.

## Current Pages

- `/` - proof landing page with About summary and links to evidence.
- `testimonials/` - selected colleague testimonials grouped by theme.
- `certificates/` - SAFe certificates and Scrum Alliance profile context.

## Published Certificate Assets

- `certificates/assets/safe-agilist.pdf`
- `certificates/assets/certified-safe-5-scrum-master.pdf`
- `certificates/assets/certified-safe-4-devops-practitioner.pdf`

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

## Squarespace DNS

For a Squarespace-managed `hendrick.net` domain, add this custom DNS record:

| Type | Host | Value |
| --- | --- | --- |
| `CNAME` | `proof` | `CtrlAltMike.github.io` |

After DNS resolves, return to GitHub repo settings and enforce HTTPS for the Pages site.

For Cloudflare Pages, use:

- Build command: none
- Output directory: `proof-site` if deploying from the parent repo, or `/` if this folder is the repo root.
