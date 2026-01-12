# ghpages-test

A minimal GitHub Pages / Jekyll test site for content and posts.

Quick start

- Install Jekyll locally and preview the site:

```bash
gem install bundler jekyll
bundle exec jekyll serve --livereload
# or
jekyll serve --livereload
```

- Content lives in the repo root and `_posts/`.

Files to know

- `about.md` — a root page using `layout: page`.
- `_posts/` — blog posts. Filenames must be `YYYY-MM-DD-title` and the `date:` front matter should match the filename.
- `_layouts/` — contains `default.html`, `page.html`, and `post.html` used for rendering.
- `_config.yml` — minimal config for Jekyll builds.
- `.github/workflows/gh-pages.yml` — workflow to build and deploy the site to GitHub Pages.

Adding a post

1. Create `_posts/YYYY-MM-DD-your-title.md`.
2. Add front matter: `layout: post`, `title:`, `date:`, `categories:`.

Deployment

- A GitHub Actions workflow is included to build and deploy `_site` to GitHub Pages. Set `url:` and `baseurl:` in `_config.yml` before publishing to a custom domain or subpath.

If you want, I can add a sample `.gitignore`, expand the layouts with CSS, or configure a GitHub Pages publishing branch.
