# /powpal

PowPal landing page, served at https://circo.io/powpal/ by GitHub Pages (published from `main`, like the rest of circo.io). Plain HTML with inline CSS; no build step.

## Files

| File | What |
|---|---|
| `index.html` | The page. All copy lives here as plain HTML. |
| `hero-{800,1200,1600}.{avif,webp,jpg}` | Hero photo sizes. |
| `og.jpg` | Share preview (1200 x 630). |
| `favicon.svg` | Tab icon. |
| `llms.txt` | Short summary for AI assistants. |

Fonts come from the site's own `/assets/fonts/` (self-hosted Geist). No remote fonts, analytics or cookies. The only third-party script is Tally's embed (`tally.so/widgets/embed.js`).

## Change things

- **Copy:** edit the text in `index.html`. The Questions section also exists as `FAQPage` JSON-LD in `<head>`: keep both identical.
- **Form ID (`TALLY_FORM_ID` = `NqlE6O`):** appears in the iframe `data-tally-src`, the `<noscript>` link and the "Open it here" link in `index.html`, and in `llms.txt`.
- **URL (`SITE_URL` = `https://circo.io/powpal/`):** canonical, `og:url`, `og:image`, JSON-LD in `index.html`; `llms.txt`; `/sitemap.xml`.
- **Images:** regenerate with `tools/powpal.py <photo> circo-io-repo/powpal` from the project folder (needs Pillow).

## Deploy

Branch, pull request, merge into `main`. Pages publishes within 1-2 minutes.
