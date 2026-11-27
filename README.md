# zoe-site

Source for **[www.zoefriedman.com](https://www.zoefriedman.com)**, served by GitHub Pages from `main`.

## Files
| File | What it is |
|---|---|
| `index.html` | The whole site (one page): hero, About, Experience, Athletics, Contact. |
| `styles.css` | All styling. Colors and fonts are set at the top in `:root`. |
| `images/web/` | Resized, web-ready photos used by the site (keep new photos under ~300 KB). |
| `images/web/og-image.jpg` | The preview card shown when the link is shared (LinkedIn, iMessage, etc.). |
| `projects.html` | Games, kept off the main nav and hidden from Google (`noindex`). |
| `404.html` | “Page not found” page. |
| `sitemap.xml`, `robots.txt` | For search engines. Update `<lastmod>` in the sitemap after big edits. |

## Common edits (all in `index.html`, editable right on GitHub)
- **Add a role:** copy one `<li class="xp">…</li>` block in the Experience section and change the text.
- **Add a resume:** upload `Zoe-Friedman-Resume.pdf` to the repo root, then uncomment the “Resume (PDF)” button in the hero.
- **Change the headline or bio:** edit the hero `lede` and the About paragraphs. If the one-line summary changes, also update the `<meta name="description">`, the `og:` tags, and the JSON-LD `description` at the top so Google shows the same thing.
- **Swap a photo:** resize it to ~1400px wide (or 640×640 for the headshot) and replace the matching file in `images/web/`.
