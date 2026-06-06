# site-template

A generic website template for quickly spinning up sites hosted on GitHub
Pages. It vendors the [**Millennial**](https://github.com/LenPaul/Millennial)
Jekyll theme by Paul Le (MIT-licensed) — a minimalist, card-grid blog/publication
theme — with all layouts, includes, and styles living in this repo so it's easy
to customize.

## Quick start for a new site

1. Create a new repo from this template (or copy the files in).
2. Edit `_config.yml` — set `title`, `description`, `author`, `email`, and
   `url`/`baseurl`.
3. Edit `_data/settings.yml` — the header/footer menu links and social icons
   (Font Awesome icon names), plus optional Disqus / Google Analytics.
4. Replace the sample content:
   - Pages live in `pages/` (`about.md`, `contact.md`, etc.).
   - Blog posts live in `_posts/` (filename `YYYY-MM-DD-title.md`). Each post's
     front matter takes an `image:` (a file in `assets/img/`) used as the
     home-page card background.
5. Swap the images in `assets/img/` and `favicon.ico`.

The sample posts/pages in `_posts/` and `pages/` are the theme's demo content —
delete or rewrite them.

## Run locally

```sh
bundle install
bundle exec jekyll serve
```

Then open the local URL Jekyll prints (with the configured `baseurl`).

## Deploy to GitHub Pages

Push to GitHub, then in **Settings → Pages** set the source to your branch
(e.g. `main`). GitHub builds the site automatically with the `github-pages` gem.

- `baseurl` is currently `"/site-template"` because the site is served under a
  subpath. If you move it to a domain root (or a `<user>.github.io` repo), set
  `baseurl: ""`.
- The theme prefixes links/assets with `site.baseurl` (changed from the
  upstream `site.github.url`) so paths are deterministic under the subpath.

## Structure

```
_config.yml          Site + build configuration
_data/settings.yml   Menu, social icons, Disqus, analytics, UI text
_layouts/            Templates (default, home, page, post, category)
_includes/           Partials (head, header, footer, featured-post, ...)
_sass/               SCSS partials (imported via assets/css/main.scss)
assets/css/          main.scss (theme) + syntax.css (code highlighting)
assets/img/          Post card / featured images
pages/               Standalone pages (about, contact, ...)
_posts/              Blog posts
index.html           Home (paginated card grid)
404.md               Not-found page
rss-feed.xml         Optional RSS 2.0 feed
```

## Credits

Theme: [Millennial](https://github.com/LenPaul/Millennial) by Paul Le, MIT License.
