# Wenchao Yue — personal academic homepage

Static site (one `index.html` + `stylesheet.css`), built on the layout of
[Jon Barron's website](https://github.com/jonbarron/jonbarron_website).

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | the whole page: bio, research statement, publications, miscellanea |
| `stylesheet.css` | template styles |
| `images/wenchao.jpg` | profile photo |
| `images/<paper>.jpg` / `.png` / `.mp4` | publication thumbnails and hover videos — currently **not used** (the list is text-only); kept so the thumbnail layout can be restored, see git history (`8fc40da`) for the markup |
| `images/favicon/` | favicon set |
| `data/` | put `Wenchao_Yue_CV.pdf` here and un-comment the CV link in `index.html` |

## Editing

* Add a publication: copy any `<tr class="pub"> … </tr>` block in `index.html`, change the title, authors, venue, links and one-line description. Add `bgcolor="#ffffd0"` to highlight it.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
