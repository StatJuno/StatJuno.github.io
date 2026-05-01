# Convert This Site to jemdoc

This repo currently contains a hand-written `index.html`.

The new source file is `index.jemdoc`. Edit that file, then regenerate `index.html`.

## 1) Install jemdoc (one-time)

Option A (recommended on macOS/Linux):

```bash
python3 -m pip install --user git+https://github.com/wsshin/jemdoc_mathjax.git
```

If `jemdoc` command is still not found, add your user bin path to shell PATH.

## 2) Generate HTML

```bash
python3 -m jemdoc index.jemdoc
```

This writes/overwrites `index.html` in the same directory.

## 3) Publish

```bash
git add index.jemdoc MENU index.html README_JEMDOC.md
git commit -m "Migrate homepage source to jemdoc"
git push
```

Since this is a `username.github.io` repo, GitHub Pages will redeploy automatically.

## Notes

- Keep `image.jpg`, `favicon.png` if you still want to use them.
- If you want a classic academic layout with sidebar/photo/publications, we can add extra pages (`publications.jemdoc`, `teaching.jemdoc`, `projects.jemdoc`) and a richer menu next.
