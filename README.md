# lucianmarin.github.io

Personal blog and log of Lucian Marin, built with [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages at [lucianmarin.github.io](https://lucianmarin.github.io/).

- Subreply: [@lucian](https://subreply.com/lucian)
- Portfolio: [lucianmarin.com](https://lucianmarin.com/)

## Structure

- `_config.yml` — Jekyll configuration (`permalink: /:year/:title.html`, `incremental: true`).
- `_posts/` — Markdown blog posts organized by year (`2012`–`2025`).
- `_layouts/` — HTML templates (`default.html`, `post.html`).
- `static/` & `images/` — Stylesheets and post media assets.
- `index.html` — Chronological post index.
- `feed.rss` — RSS 2.0 syndication feed.

## Running Locally

```bash
jekyll serve --incremental
```

Then open `http://localhost:4000`.
