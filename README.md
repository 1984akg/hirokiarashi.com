# hirokiarashi.com

Personal academic website of Hiroki Arashi, built with the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template (Jekyll) and hosted on GitHub Pages.

Live site: <https://1984akg.github.io/hirokiarashi.com/>

## Editing content

- `_config.yml` — name, bio, sidebar links, site-wide settings
- `_pages/about.md` — home page
- `_pages/cv.md` — CV page
- `_publications/` — one Markdown file per publication
- `_talks/` — one Markdown file per talk / presentation
- `_portfolio/` — one Markdown file per project
- `_data/navigation.yml` — top navigation menu

Pushing to `main` triggers the GitHub Pages build automatically.

## Local preview

With Docker installed:

```bash
docker compose up
# open http://localhost:4000/hirokiarashi.com/
```
