# Personal website

An academic personal site built with [Jekyll](https://jekyllrb.com) and hosted on
GitHub Pages. Sections: **Home/bio**, **Research**, **Publications**, **Blog**
(science popularization), and **Outreach** (book, talks). Every external link is
shown as a **clickable image card**.

## Quick start — what to edit

| You want to…                  | Edit                                             |
|-------------------------------|--------------------------------------------------|
| Set your name, URL, socials   | `_config.yml`                                    |
| Write your bio                | `index.html` (hero section, `TODO` markers)      |
| Describe your research        | `research.md`                                    |
| Add a paper                   | `_data/publications.yml`                         |
| Add a book / talk             | `_data/outreach.yml`                             |
| Write a blog post             | add a file in `_posts/` (copy the example)       |
| Swap images                   | `assets/images/` (see its README)                |
| Restyle (colours, etc.)       | `assets/css/style.css` (variables at the top)    |

> After editing `_config.yml`, search the whole project for **`TODO`** and
> **`USERNAME`** to make sure nothing is left as a placeholder.

## Add a blog post

Create `_posts/YYYY-MM-DD-some-slug.md` with front matter:

```yaml
---
layout: post
title: "My post title"
date: 2026-06-10
badge: "Explainer"
tags: [nlp, transformers]
description: "One line shown on the card and in previews."
image: "/assets/images/my-post.png"
reading_time: "5 min read"
---

Your text in Markdown...
```

See `_posts/2026-06-05-welcome.md` for a full template, including how to drop a
clickable image card inside a post with an `include card.html` tag.

## Deploy to GitHub Pages

1. Create a repo on GitHub.
   - **User site** (recommended, URL = `https://USERNAME.github.io`):
     name the repo exactly `USERNAME.github.io`, and in `_config.yml` keep
     `baseurl: ""`.
   - **Project site** (URL = `https://USERNAME.github.io/REPONAME`):
     name it anything, and set `baseurl: "/REPONAME"` in `_config.yml`.
2. Push this folder to that repo (see commands below).
3. On GitHub: **Settings → Pages → Build and deployment → Source =
   "Deploy from a branch"**, branch `main`, folder `/ (root)`. Save.
4. Wait ~1 minute; your site appears at the URL above. It rebuilds on every push.

```bash
git remote add origin https://github.com/USERNAME/REPO.git
git branch -M main
git push -u origin main
```

## Optional: preview locally

Requires Ruby. Then:

```bash
gem install bundler
bundle install
bundle exec jekyll serve   # open http://localhost:4000
```

(You don't need this to publish — GitHub builds the site for you.)
