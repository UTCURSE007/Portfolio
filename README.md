# Utkarsh — Portfolio

A single self-contained page. No build step, no dependencies: every image, style and script is inlined into `index.html`, so the site works even if you delete `assets/`.

```
index.html              the whole site, self-contained
assets/photos/          original photographs
assets/paintings/       original paintings
assets/certificates/    certificate scans
assets/cv/              CV as PDF
.nojekyll               makes GitHub serve files as-is
```

`assets/` is kept as the source archive — originals at full resolution, named readably — so the images are versioned alongside the page rather than only living inside it.

## Publish on GitHub Pages

1. Push the contents of this folder to the default branch:
   ```
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```
2. Repository → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. The site appears at `https://<user>.github.io/<repo>/`.

## Local preview

Open `index.html` in any browser, or run `python3 -m http.server` in this folder.
