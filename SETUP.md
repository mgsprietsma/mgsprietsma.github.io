# Setup notes

Drop these files into the root of your repository (keeping the folder structure):

```
_config.yml            ← you already have this (see note below)
_layouts/default.html  ← page shell: header, nav, footer
_data/publications.yml ← your papers live here
assets/css/style.css   ← all styling; change the accent color at the top
assets/cv.pdf          ← replace with your real CV (keep the name)
assets/portrait.jpg    ← optional headshot (see index.md)
index.md               ← About / landing page
research.md            ← Research page (reads _data/publications.yml)
cv.md                  ← CV page (embeds assets/cv.pdf)
```

## Customize

- **Your info:** edit `index.md` (bio, links) and the placeholders throughout.
- **Papers:** edit `_data/publications.yml` only — add a block per paper. The
  Research page builds the cards automatically.
- **CV:** replace `assets/cv.pdf` with your own file, same name and location.
- **Colors/fonts:** edit the `:root` block at the top of `assets/css/style.css`.
  Changing `--accent` recolors the whole site.

## _config.yml

The pages use `layout: default`, which resolves to the local `_layouts/default.html`
here — so it works with or without a theme. Two things worth setting so the header
and page titles fill in correctly:

```yaml
title: Your Name
description: Researcher in [your field].
```

If your config sets a `theme:` or `remote_theme:`, you can leave it — the local
layout takes precedence. If you hit conflicts, removing the theme line is safe.

## Preview locally (optional)

You don't need this to publish — GitHub builds the site for you. But to preview:

```bash
bundle install
bundle exec jekyll serve
```

with the included `Gemfile`, then open http://localhost:4000.

## Publish

Commit and push to your `main` branch. In the repo's **Settings → Pages**, set the
source to **Deploy from a branch → main → / (root)**. Your site appears at
`https://<username>.github.io/<repo>/` within a minute or two.
