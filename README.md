# UK Knowledge Graphs Interest Group website

A responsive, Jekyll-based website scaffold for the UK Knowledge Graphs Interest Group,
relaunching the [former Alan Turing Institute group](https://www.turing.ac.uk/research/interest-groups/knowledge-graphs)
with support from the Open Data Institute.

## Preview locally

1. Install Ruby and Bundler, then run `bundle install`.
2. Run `bundle exec jekyll serve`.
3. Open `http://127.0.0.1:4000/`.

The source homepage is `index.html`. Jekyll processes its Liquid tags and layouts:
opening this source file directly in a browser will not show the finished page.

## Publish at https://uk-knowledge-graphs.github.io/

Create a GitHub repository named `uk-knowledge-graphs.github.io` in the
`uk-knowledge-graphs` account/organisation, commit all files, and push to `main`.
In repository Settings → Pages, set the build/deployment source to **GitHub Actions**.
The included workflow builds the site and deploys it on pushes to `main`.
The `url` and `baseurl` in `_config.yml` are already set for the root domain.
If using a project repository instead, update both values.

## Edit the site

- `index.html`: homepage and chair listing.
- `_data/chairs.yml`: chair names, affiliations and local image paths.
- `assets/images/chairs/`: local SVG **placeholders**, not real chair photos.
  Replace each with a licensed/permission-cleared headshot, then update its
  `image:` path in `_data/chairs.yml` (e.g. `/assets/images/chairs/jeff-pan.jpg`).
  Keep descriptive `alt` text in the homepage image markup. No photographs
  could be downloaded or their reuse rights checked in this environment.
- `_meetups/` and `_symposiums/`: one Markdown file per event. Each becomes a
  dedicated page with its own agenda, speakers, keynote and sponsor fields.
  Current "coming soon" pages are **planning placeholders**, not event announcements.
- `_templates/`: starter Markdown files to copy into the appropriate collection.
  Use a unique filename and replace all bracketed values. Use date values in
  YYYY-MM-DD format to avoid ambiguity.
- `teaching/index.html`: teaching-material landing page. Add verified links
  and permissions before publishing contributed course material.
- `assets/css/site.css`: styling and responsive layouts.
- `_layouts/`: shared page and event templates.

**Before launch:** obtain chair photographs and consent, confirm wording about
ODI support and the new group, replace planning pages when real event details
are known, and curate teaching links. The supplied user contact email appears
in the footer for contributions; replace it if a shared inbox is preferred.

No actual events, keynotes, sponsor commitments, or teaching links are asserted.
