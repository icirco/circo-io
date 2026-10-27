# circo.io/expert - how to edit

Expert profile for implementing firms, donors, evaluation units and NCPs, in two languages:

- English: https://circo.io/expert/
- German: https://circo.io/expert/de/

## Linking rules (important)

/expert is **orphaned on purpose**: people reach it only from outreach emails (later perhaps LinkedIn). This keeps /bio a pure mentoring page.

- **Never** add a link to /expert from the homepage, /bio, /bio/de, any navigation or footer, or `sitemap.xml`.
- /expert links only to: its own EN/DE versions, the homepage (← circo.io), email, LinkedIn, the CV PDF, and one link at the bottom to the mentoring profile (/bio, matched by language).
- No `noindex`: the pages may be found by search once linked from LinkedIn. That's accepted.
- The page files carry `sitemap: false` in case a sitemap plugin is ever added.

## Change any text

1. On GitHub, open [`_data/expert.yml`](_data/expert.yml) and click the pencil icon.
2. Edit the text between the double quotes (English `en:` and German `de:` next to each other).
3. Commit. The pages update within 1-2 minutes.

Keep the quotes and the indentation (spaces) exactly as they are.

### Field record and ventures

Both are lists, newest first. To add an entry, copy a whole block (from `- years:` / `- name:` down to the last line before the next `-`), paste it in the right position, and edit it. Fields:

- Field record: `years`, `org`, `full` (optional full organisation name), `role` (optional), `what`.
- Ventures: `name`, `url` (optional, makes the name a link), `years`, `role`, `desc`.

Write years as `2011-2014`; the page shows them with a proper dash.

## The CV download

The **CV** link in the header stays hidden until the PDF exists:

1. Upload the English PDF as `expert/Julian-Circo-CV-EU.pdf` and the German one as `expert/de/Julian-Circo-CV-EU.pdf` (Add file › Upload files, in those folders). If there's only one version, upload the same file to both places.
2. In `_data/expert.yml`, change `available: false` to `available: true` under `cv:`.

## Photo

The page reuses the /bio portrait (`bio/portrait.jpg`). Replacing that file changes both pages.

## Share images

`expert/og-en.jpg` and `expert/og-de.jpg` (1200 x 630) are the previews shown on LinkedIn, Slack and in email clients. They contain the text as an image, so they don't update when the text changes. The script that makes them is in the project folder (`tools/og_expert.py`).

## Layout

The design lives in [`_layouts/expert.html`](_layouts/expert.html). It shares colours, fonts and the header style with `_layouts/bio.html`; if you change a colour in one, change it in the other.

## Preview before publishing

Edit on a new branch ("Create a new branch" when committing), open a pull request, then merge. GitHub Pages only publishes `main`.
