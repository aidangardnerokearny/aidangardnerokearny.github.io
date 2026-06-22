# Physics PhD — academic website

A clean, self-contained [Jekyll](https://jekyllrb.com) template built for
GitHub Pages. There's no  external theme to fight with; the layout, styles, and a
detector-cross-section signature graphic are all in this repo, and can be edited
freely. Content lives in YAML and config; you rarely touch HTML.

```
.
├── _config.yml            ← ALL your personal info + links (start here)
├── _data/
│   ├── publications.yml   ← your papers (auto-grouped by year, name auto-bolded)
│   ├── news.yml           ← short dated updates for the home page
│   └── cv.yml             ← education / experience / teaching / skills
├── index.html             ← home: hero, about, research, selected work, news
├── portfolio.md           ← /portfolio/  (full list)
├── cv.md                  ← /cv/            (condensed CV + PDF link)
├── _layouts/  _includes/  ← the theme (nav, footer, detector graphic, etc.)
└── assets/
    ├── css/style.css      ← design tokens + all styling
    ├── img/favicon.svg
    └── cv.pdf             ← ADD THIS: your full CV
```

## Make it yours (5 minutes)

1. **`_config.yml`** — name, role, tagline, university, and every link
   (email, GitHub, Google Scholar, ORCID, INSPIRE, arXiv, LinkedIn). Leave any
   value as `""` and that link disappears automatically.
2. **`_data/portoflio.yml`** — replace the example papers. Set `selected: true`
   to feature one on the home page. Set `author_key` to your surname and your
   name gets bolded wherever it appears in an author list.
3. **`_data/news.yml`** and **`_data/cv.yml`** — your updates and CV entries.
4. Edit the **About** paragraph and the three **Research** blurbs in `index.html`.
5. Drop your CV at **`assets/cv.pdf`**.

The colors and fonts are CSS variables at the top of `assets/css/style.css` —
change `--accent` and the three `--font-*` values to re-skin the whole site.

## Run it locally

Requires Ruby (3.x). Then:

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://localhost:4000
```

## Deploy to GitHub Pages

**For a user site** (`username.github.io`):
- Name the repo `username.github.io`.
- In `_config.yml`: `url: "https://username.github.io"` and `baseurl: ""`.

**For a project site** (`username.github.io/repo`):
- In `_config.yml`: `baseurl: "/repo"`.

Then either:
- **Classic** — Settings → Pages → Source: *Deploy from a branch* → `main` / root. Done.
- **Actions** — Settings → Pages → Source: *GitHub Actions* (uses the included
  `.github/workflows/pages.yml`). Otherwise you can delete that file.

Push to `main` and the site builds automatically.

## Notes

- Built only on GitHub-Pages-whitelisted plugins (`jekyll-seo-tag`,
  `jekyll-sitemap`), so it deploys with zero extra configuration.
- Responsive, keyboard-accessible, and honors `prefers-reduced-motion`
  (the detector animation stops for visitors who ask it to).
- The detector graphic is plain SVG in `_includes/detector.html` — the rings are
  detector subsystems and the highlighted one is the solenoid. Swap the geometry
  or delete the include to use your own hero.
