# circo.io/bio - how to edit

Two pages, built automatically by GitHub Pages from one text file:

- English: https://circo.io/bio/
- German: https://circo.io/bio/de/

## Change any text

1. On GitHub, open [`_data/bio.yml`](_data/bio.yml) and click the pencil icon.
2. Edit the text between the double quotes. English (`en:`) and German (`de:`) sit next to each other.
3. Commit. The pages update within 1-2 minutes (progress shows under the repo's **Actions** tab).

Rules:
- Keep the double quotes around each text, and keep the indentation (spaces) as it is.
- To add a list item (e.g. another Focus detail or Bio paragraph), copy an existing `- "..."` line in the same list.
- The browser-tab title and Google snippet are under `meta:` at the top.

If a commit breaks the file (e.g. a missing quote), the build fails, the live site keeps the previous version, and GitHub emails you. Fix the line and commit again.

## Swap the photo

Upload a new file to `bio/portrait.jpg` (same name, replace the old one).

- Portrait orientation, about 900 x 1200 px, JPG, under 250 KB.
- The page crops it to fit and keeps the face near the top, so similar framing works best.

The share images shown on LinkedIn, Slack, WhatsApp (`bio/og-en.jpg`, `bio/og-de.jpg`, 1200 x 630) are separate files. They don't update automatically when the photo or text changes.

## Change the layout

The page design lives in [`_layouts/bio.html`](_layouts/bio.html). It's only needed for design changes, not for text.

## Preview before publishing

Edit on a new branch instead of `main` ("Create a new branch" when committing), open a pull request, check the text, then merge. GitHub Pages only publishes `main`.

## Fonts

Geist and Geist Mono (SIL Open Font License, `assets/fonts/OFL.txt`), self-hosted in `assets/fonts/`, subset to Latin and German characters.
