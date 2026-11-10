# Personal website

Jekyll site for GitHub Pages: About, Research, Publications, Outreach, and CV.

## Installing over your old site

1. In your local copy of the repo, delete everything except the hidden `.git` folder.
   This clears out leftover files from the Cayman theme and the earlier setup.
2. Copy all of these files in, including the hidden `.gitignore`.
3. Add your two files:
   - your banner image as `assets/images/header.jpg`
   - your CV as `assets/cv.pdf`
4. Commit and push:
   ```
   git add -A
   git commit -m "Rebuild site"
   git push
   ```
5. In Settings → Pages, the source should be "Deploy from a branch", `main`, `/ (root)`.

## What to edit

| To change...                          | Edit                          |
|---------------------------------------|-------------------------------|
| Name, links, image path, CV date      | `_config.yml`                 |
| Landing page text                     | `index.md`                    |
| Research page text                    | `research.md`                 |
| Papers                                | `_data/publications.yml`      |
| Outreach entries                      | `_data/outreach.yml`          |
| Tabs in the header                    | `_data/navigation.yml`        |
| Colors, font, spacing                 | top of `assets/css/style.css` |

Changes to `_config.yml` need a restart of the local preview to show up.

## Banner image

- Use a wide image, at least 2000 px across. It's cropped to fit, taller on the landing page.
- If the important part gets cut off, set `header_image_position` in `_config.yml`
  (`top`, `bottom`, or something like `"50% 30%"`).
- To use a different image on one page, add `header_image: /assets/images/other.jpg` to that page's front matter.
  To hide it on one page, add `hero: none`.
- Until the file exists, the site just shows without a banner.

## Local preview

```
bundle install
bundle exec jekyll serve --livereload
```
Then open http://localhost:4000.
