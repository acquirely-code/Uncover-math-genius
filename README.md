# Uncover Math Genius

Static website for **[uncovermathgenius.com](https://uncovermathgenius.com)**, hosted on Cloudflare Workers (static assets).

## Structure

```
docs/                 ← the website (Cloudflare serves this folder)
├── index.html        ← home page
├── about-us/         ← each folder = one page URL (/about-us/)
├── blog/
├── ...
├── wp-content/       ← images, videos, themes, plugin assets
├── wp-includes/      ← core scripts and styles
├── 404.html         ← shown for unknown URLs
└── CNAME            ← GitHub Pages only; not uploaded to Cloudflare
```

Folder names inside `docs/` are the page URLs, so renaming or moving them changes the site's links.

## Updating the site

Edit files inside `docs/`. With the repo connected in Cloudflare (Workers Builds), pushing to `main` redeploys automatically.

Manual deploy (Node 22.12+):

```
npm ci
npm run dev       # local preview
npm run deploy    # publish
```

Settings are in `wrangler.jsonc`. Limits: 25 MiB per file, 20,000 files (free plan). Don't put files in `docs/cdn-cgi/`; Cloudflare reserves that path.

## Notes

- Exported from WordPress as a static site. Forms, cart and checkout don't work on a static site.
- Large videos are hosted on Wistia, not in this repo.
- DNS is managed at Hostinger. Email, `book.` and `webinar.` subdomains run on Zoho.
