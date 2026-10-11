# Wenchao Yue — personal academic homepage

Static site (one `index.html` + `stylesheet.css`), built on the layout of
[Jon Barron's website](https://github.com/jonbarron/jonbarron_website).

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | the whole page: bio, research statement, news, publications, miscellanea |
| `stylesheet.css` | template styles (fonts, colours). The hover-reveal rules for publication rows (`.one` / `.two`, `tr.pub:hover .two`) are inlined in the `<head>` of `index.html`; bump the `?v=` on the stylesheet link whenever you edit this file so GitHub Pages' 10-minute cache is bypassed |
| `images/wenchao.jpg`, `images/wenchao_back.jpg` | profile photo (front) and the photo revealed by the hover flip (back) |
| `images/<paper>.jpg` / `.png` / `.mp4` | publication thumbnails and hover videos — currently **not used** (the list is text-only); kept so the thumbnail layout can be restored, see git history (`bae886d`) for the markup |
| `images/favicon/` | favicon set |

## Interactive bits

* **Journey map** (after the intro): inline SVG; land outline generated from a simplified Natural Earth country file (equirectangular, cropped to lon −14…132 / lat −12…61, viewBox 800×400). Stops, roles and label offsets live in the `STOPS` array in the first `<script>`; arcs animate once when scrolled into view (skipped under `prefers-reduced-motion`).
* **Tactile canvas** (Research Philosophy, right column): 16×16 pressure grid driven by the pointer, Gaussian press + exponential decay, three renderers (`array`, `gel`, `oct`). All in the second `<script>`; no dependencies.

## Editing

* Add a publication: copy any `<tr class="pub"> … </tr>` block in `index.html`, change the title, authors, venue, links and one-line description. Add `bgcolor="#ffffd0"` to highlight it.
* Numbering is chronological (oldest = 1), so a new paper gets the next number: set `id="p<N>"`, put `<span class="pubnum"><N></span>` before the title, and place the row at the top of the list.
* Topics: set `data-tags` on the row to any of `ml`, `tactile`, `robotics` (space-separated). The tab buttons in `#pubtabs` filter on these and show counts automatically. To reference the paper from the Research overview, link to `#p<N>`.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
