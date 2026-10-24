# Uncover Math Genius

Static website for **[uncovermathgenius.com](https://uncovermathgenius.com)**, hosted on GitHub Pages.

## Structure

```
docs/                 ← the website (GitHub Pages serves this folder)
├── index.html        ← home page
├── about-us/         ← each folder = one page URL (/about-us/)
├── blog/
├── ...
├── wp-content/       ← images, videos, themes, plugin assets
├── wp-includes/      ← core scripts and styles
└── CNAME             ← custom domain
```

Folder names inside `docs/` are the page URLs, so renaming or moving them changes the site's links.

## Updating the site

Edit files inside `docs/` and push to `main`. GitHub Pages redeploys automatically within a minute or two.

## Notes

- Exported from WordPress as a static site. Forms, cart and checkout don't work on a static site.
- Large videos are hosted on Wistia, not in this repo.
- DNS is managed at Hostinger. Email, `book.` and `webinar.` subdomains run on Zoho.
