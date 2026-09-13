# Utkarsh — Portfolio

```
index.html      the site
uploads/        photographs, paintings, certificates, CV (referenced by the gallery tabs)
.nojekyll       makes GitHub serve files as-is
```

`uploads/` must sit next to `index.html` — the Photographs and Paintings tabs load their images from it at runtime.

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
