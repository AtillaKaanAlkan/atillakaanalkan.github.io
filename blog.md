---
layout: page
title: Blog
subtitle: "Popular science and paper explainers on natural language processing and machine learning"
permalink: /blog/
---

I write here to make ideas in natural language processing and machine learning
accessible to a general audience, including plain-language explanations of my own
work. Each card below opens the full article.

{% if site.data.blog_external.size > 0 or site.posts.size > 0 %}
<div class="card-grid">
  {% for post in site.data.blog_external %}
    {% include card.html
        url=post.url
        image=post.image
        title=post.title
        meta=post.date
        badge=post.badge
        description=post.description
        contain=post.contain
        external=true %}
  {% endfor %}
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
<p>No posts yet, check back soon.</p>
{% endif %}
