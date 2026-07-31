# devillegna.github.io

Source for my personal academic website: <https://devillegna.github.io>

It lists my publications and software projects in post-quantum cryptography.
Built with [Jekyll](https://jekyllrb.com/) and served by GitHub Pages, which
rebuilds the site automatically on every push to `master`.

## Layout

| Path | Contents |
| --- | --- |
| `_pages/` | Standalone pages (about, publications, projects, sitemap, 404) |
| `_publications/` | One markdown file per paper |
| `_projects/` | One markdown file per software project |
| `files/` | PDFs and other downloads, served from `/files/` |
| `images/` | Avatar and favicons |
| `_includes/`, `_layouts/`, `_sass/`, `assets/` | Theme internals |
| `markdown_generator/` | Optional scripts to bulk-generate `_publications/` entries from BibTeX or TSV |

## Adding content

Add a markdown file to `_publications/` or `_projects/` with front matter
matching the existing entries. Both collections are rendered newest-first, so
the `date:` field controls ordering.

## Running locally

Requires Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

The site is then at <http://localhost:4000>. Pass `--config _config.yml,_config.dev.yml`
to use the local overrides (localhost URLs, expanded CSS, no analytics).

The `Gemfile` deliberately depends only on the `github-pages` gem, which pins
Jekyll and every plugin to the exact versions GitHub Pages runs. Do not add a
standalone `gem "jekyll"` line — it conflicts with that pin.

## Credits and licence

The theme is [academicpages](https://github.com/academicpages/academicpages.github.io),
forked by [Stuart Geiger](https://github.com/staeiou) from the
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme,
© 2016 Michael Rose. The theme code is MIT licensed — see [LICENSE](LICENSE).

The site content — publication entries, project descriptions, images and the
documents under `files/` — is © Ming-Shing Chen and is not covered by that
licence.
