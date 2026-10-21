# UK Knowledge Graphs Interest Group website

A Jekyll website for the UK Knowledge Graphs Interest Group, relaunching the
[former Alan Turing Institute group](https://www.turing.ac.uk/research/interest-groups/knowledge-graphs)
with support from the Open Data Institute.

## Add a new event (meet-up or symposium)

**Each event is a separate Markdown file and becomes a separate public page.**
You do not need to edit `index.html`, `events/index.html` or the event layout
to add an event.

1. Copy `_templates/meetup-example.md` or `_templates/symposium-example.md`
   to `_events/your-unique-event-name.md` (for example,
   `_events/2027-05-knowledge-graphs-workshop.md`).
2. Replace all `REPLACE:` text with confirmed details. Keep `event_type` as
   `Meet-up` or `Symposium`; you can also use another label if appropriate.
3. Set `order` to the numeric event date in YYYYMMDD form. It controls the
   list order (highest first). Use `event_date` for the human-readable date
   and time, including time zone. YAML strings containing colons need quotes.
4. Under the second `---`, write *this event's own* Markdown description,
   directions, links, accessibility details and any extra headings.
5. Uncomment optional `agenda`, `keynote`, `speakers`, `sponsors` and
   `registration_url` fields **only** when those details are confirmed. Delete
   any sections you do not need. The layout shows only sections provided.
6. Commit and push. The event will appear automatically on `/events/` and at
   `/events/your-unique-event-name/`.

Two example files in `_templates/` show the different kinds of content a
meet-up and a symposium can contain. They are **not published**. No events
are currently announced; `_events/` is intentionally empty.

If a specific event needs content beyond the structured sections, put it
in that event's Markdown body. `_layouts/event.html` defines shared visual
styling only; it does not force empty keynote, speaker or sponsor sections.

## Other common edits

- `index.html`: homepage text and the chairs/contact sections.
- `_data/chairs.yml`: chair names, affiliations and portrait image paths.
- `assets/images/chairs/`: labelled SVG placeholders, **not real photos**.
  Replace with permission-cleared headshots and update `image:` paths in
  `_data/chairs.yml`. Once all portraits are real, update the placeholder
  image alt text and remove the placeholder note in `index.html`.
- `_data/contact.yml`: **single place** to change the LinkedIn group,
  Google group and organiser email; used across the homepage, event listing,
  teaching page and footer.
- `teaching/index.html`: teaching material landing page. Review links and
  reuse permissions before listing resources.
- `assets/css/site.css`: styling and responsive layouts.
- `_layouts/default.html`: shared header/footer.
- `_layouts/event.html`: shared event design and optional fields.
- `meetups/` and `symposiums/`: old index URLs redirect to `/events/`;
  do not add events there.

## Preview locally

1. Install Ruby and Bundler, then run `bundle install`.
2. Run `bundle exec jekyll serve`.
3. Open `http://127.0.0.1:4000/`.

Jekyll processes the source `index.html` and its Liquid tags. Opening the
source file directly in a browser will not show the finished site.

## Publish at https://uk-knowledge-graphs.github.io/

Create a repository called `uk-knowledge-graphs.github.io` under the
`uk-knowledge-graphs` GitHub account/organisation, push these files to
`main`, and select **GitHub Actions** as the Pages build/deployment source.
The included workflow builds and publishes on pushes to `main`.
`_config.yml` is configured for the root domain; adjust `url` and `baseurl`
if deploying to a project repository instead.

Before launch: confirm the group/ODI wording and contact details, obtain
chair photographs and consent, and review any contributed teaching links.
No keynotes, sponsors, or forthcoming event dates are asserted.
