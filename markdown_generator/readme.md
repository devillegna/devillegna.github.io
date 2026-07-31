# Publication markdown generator

Optional helpers for bulk-generating the per-paper markdown files in
`_publications/`. Not needed for day-to-day edits — the existing entries are
hand-written, and adding one more by hand is usually faster.

Run these from inside this directory; both write into `../_publications/`.

| File | Input | Notes |
| --- | --- | --- |
| `pubsFromBib.py` | BibTeX (`pubs.bib`, `proceedings.bib`) | Requires `pybtex`. Edit the file list near the top of the script. |
| `publications.py` | `publications.tsv` | Columns: `pub_date`, `title`, `venue`, `excerpt`, `citation`, `url_slug`, `paper_url`. You need to supply this TSV — the template's sample data was removed. |

The `.ipynb` files are Jupyter versions of the same two scripts with inline
documentation.

Generated files overwrite anything with a matching slug, so review the output
before committing.
