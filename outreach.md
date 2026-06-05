---
layout: page
title: Outreach
subtitle: Books, talks, and science communication
permalink: /outreach/
---

Beyond research papers, I work to bring AI and NLP to a wider public. To add or
edit items, edit `_data/outreach.yml`.

## My book

<div class="card-grid covers">
  {% for item in site.data.outreach %}
    {% if item.cover %}
      {% include card.html
          url=item.url image=item.image title=item.title
          meta=item.kind badge=item.badge description=item.description external=true %}
    {% endif %}
  {% endfor %}
</div>

## Talks, interviews & articles

<div class="card-grid">
  {% for item in site.data.outreach %}
    {% unless item.cover %}
      {% include card.html
          url=item.url image=item.image title=item.title
          meta=item.kind badge=item.badge description=item.description external=true %}
    {% endunless %}
  {% endfor %}
</div>
