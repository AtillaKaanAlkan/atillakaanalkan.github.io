---
layout: page
title: Blog
subtitle: Making AI & NLP accessible — popular science and paper explainers
permalink: /blog/
---

I write here to popularize ideas in AI and NLP for a general audience — including
plain-language explanations of my own papers. To add a post, drop a Markdown file
in `_posts/` (see `_posts/2026-06-05-welcome.md` for the template).

{% if site.posts.size > 0 %}
<div class="card-grid">
  {% for post in site.posts %}
    {% assign post_date = post.date | date: "%B %-d, %Y" %}
    {% include card.html
        url=post.url
        image=post.image
        title=post.title
        meta=post_date
        badge=post.badge
        description=post.description %}
  {% endfor %}
</div>
{% else %}
<p>No posts yet — check back soon.</p>
{% endif %}
