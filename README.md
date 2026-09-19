# utkarsh — portfolio site

Static site. No build step, no dependencies.

```
index.html      the site (renders from content.json)
content.json    ALL editable content — text, image paths, which tabs are visible
admin.html      the editor (open it in a browser, edit, export)
styles.css      design tokens + component classes
assets/         every image and the CV pdf
```

## Publishing

Copy the contents of this folder to the repository root and push. GitHub Pages serves it as is.

## Editing

Open `admin.html` **over http** — either the published URL (`…/admin.html`) or locally:

```
cd <this folder>
python -m http.server 8000
# then open http://localhost:8000/admin.html
```

Edit anything in the left-hand sections. Changes autosave to the browser's local
storage, so closing the tab does not lose work.

- **Add images…** on a gallery adds one entry per file you pick.
- **Preview** opens the real site with your unsaved edits.
- **Export files to push** downloads `portfolio-update.zip` — `content.json` plus
  any images you added. Unzip it into the repository root, overwrite, commit, push.
- **content.json only** downloads just the JSON if you added no new images.
- **Discard draft** throws away local edits and reloads the published content.

Opening `admin.html` straight off the disk (`file://`) blocks the fetch of
`content.json` — use **Load JSON…** to open the file manually in that case.

## Notes

- The Curriculum Vitae tab is hidden (`tabs.cv: false` in `content.json`). Its
  content is still there; flip the switch under **Visible tabs** to bring it back.
- Poems keep their line breaks exactly as typed. Set **Script** to `devanagari`
  for Hindi pieces so they set in Tiro Devanagari Hindi.
- Figure **Fit**: `natural` (full image), `cover`, `contain`, or `rotated`
  (the quarter-turn shadowgraph treatment).
