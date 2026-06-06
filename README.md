# site-template

A generic [Jekyll](https://jekyllrb.com/) website template for quickly spinning
up sites hosted on GitHub Pages. It uses no external theme gem — all layouts and
styles live in this repo, so it's easy to customize.

## Quick start for a new site

1. Create a new repo from this template (or copy the files in).
2. Edit `_config.yml` — set `title`, `tagline`, `description`, `author`,
   `email`, `url`/`baseurl`, and the `social` handles.
3. Replace the content in `index.html`, `about.md`, and `contact.md`.
4. Add blog posts to `_posts/` (filename format: `YYYY-MM-DD-title.md`).
5. Swap `assets/favicon.svg` and tweak colors in `assets/css/style.css`
   (custom properties at the top).

## Run locally

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Use `--livereload` to auto-refresh on save.

## Deploy to GitHub Pages

Push to GitHub, then in **Settings → Pages** set the source to your branch
(e.g. `main`). GitHub builds the site automatically using the `github-pages`
gem, so the local and deployed builds match.

- **User/org site** (`<user>.github.io`): leave `baseurl: ""`.
- **Project site** (`<user>.github.io/<repo>`): set `baseurl: "/<repo>"`.
- **Custom domain**: add a `CNAME` file with the domain and leave `baseurl: ""`.

## Structure

```
_config.yml          Site configuration
_layouts/            Page templates (default, post)
_includes/           Reusable partials (header, footer)
_posts/              Blog posts
assets/              CSS and favicon
index.html           Home page
about.md             About page
contact.md           Contact page
blog.html            Post listing
404.html             Not-found page
```
