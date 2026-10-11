# Wenchao Yue — personal academic homepage

Static site (one `index.html` + `stylesheet.css`), built on the layout of
[Jon Barron's website](https://github.com/jonbarron/jonbarron_website).

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | the whole page: bio, research statement, news, publications, miscellanea |
| `stylesheet.css` | template styles (fonts, colours). The hover-reveal rules for publication rows (`.one` / `.two`, `tr.pub:hover .two`) are inlined in the `<head>` of `index.html`; bump the `?v=` on the stylesheet link whenever you edit this file so GitHub Pages' 10-minute cache is bypassed |
| `images/wenchao.jpg` | profile photo |
| `images/<paper>.jpg` / `.png` | 320×320 publication thumbnails (`.png` files are placeholder venue cards — replace with real figures when ready) |
| `images/<paper>.mp4` | short hover videos shown when the mouse is over a publication row |
| `images/favicon/` | favicon set |
| `data/` | put `Wenchao_Yue_CV.pdf` here and un-comment the CV link in `index.html` |

## Editing

* Add a publication: copy any `<tr class="pub"> … </tr>` block in `index.html`, change the thumbnail, title, authors, venue, links and one-line description. Add `bgcolor="#ffffd0"` to highlight it.
* Hover video: wrap the thumbnail in `<div class="one"><div class="two"><video …></div><img …></div>` (see the pouch-motor / balloon-sensor rows).
* Thumbnails are 320×320 (2× of the 160 px slot). Pad non-square figures with white rather than cropping them.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
