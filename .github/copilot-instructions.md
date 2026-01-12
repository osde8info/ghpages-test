---
description: Copilot instructions for ghpages-test
---

Purpose
- This is a very small GitHub Pages / Jekyll site. The repo contains mostly Markdown content; AI agents should focus on content, front-matter, and simple static-site conventions.

Quick orientation
- Content files: `about.md` (root pages) and posts under `_posts/`.
- No `_config.yml` or build scripts are present in the repo — the site is minimal and static.

What to edit and examples
- Root pages: edit `about.md`. Example front matter from this repo:

```yaml
---
layout: page
title: About
permalink: /about/
---
```

- Blog posts: place files in `_posts/` with a filename of the form `YYYY-MM-DD-title` and YAML front matter like:

```yaml
---
layout: post
title: "My First Blog Post"
date: 2026-01-12
categories: blog
---
```

Conventions to preserve
- Filenames: keep the leading date in `_posts/` filenames in sync with the `date:` value in front matter.
- Layout names: pages use `layout: page`, posts use `layout: post`. Look for `_layouts/` if it gets added later.
- Categories: use simple words (e.g., `blog`) as seen in existing posts.


Local preview (developer workflow)
- This repo supports local preview with Jekyll. To preview locally, run:

```bash
gem install bundler jekyll           # if ruby/jekyll not installed
bundle exec jekyll serve --livereload
# or
jekyll serve --livereload
```

- The repository now contains a basic `_config.yml` and simple layouts under `_layouts/` that Jekyll will use during site build.

Deployment notes
- A GitHub Actions workflow has been added at `.github/workflows/gh-pages.yml` that builds the site and deploys `_site` to GitHub Pages using `peaceiris/actions-gh-pages` on pushes to `main`/`master`.
- Before using the workflow, set `url:` and `baseurl:` in `_config.yml` if hosting on a custom domain or a subpath.

Agent guidance (concise)
- Make only content/front-matter edits unless asked to add a layout or build tool. Changes that introduce Ruby gems or Node tooling should be proposed first.
- Preserve front matter keys and date formats used in existing files. When creating a new post, match the `YYYY-MM-DD-title` filename convention.
- When adding templates or assets, place them under conventional Jekyll folders (`_layouts/`, `_includes/`, `assets/`) and note the change in your commit message.

Where to look
- Root: `about.md`, `README.md`
- Posts: `_posts/`

If anything here is unclear or you'd like me to expand examples (layouts, assets, or CI), tell me which area and I'll update this file.
