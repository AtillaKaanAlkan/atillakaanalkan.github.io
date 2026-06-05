---
layout: post
title: "Welcome — and what this blog is for"
date: 2026-06-05
badge: "Note"
tags: [meta, nlp, ai]
# `description` shows on the card and in search/social previews:
description: "Why I'm writing plain-language explainers about AI and NLP, and what to expect."
# `image` is the card thumbnail AND the hero at the top of the post.
# Use /assets/images/...  or a full https URL. Remove the line for no image.
image: "/assets/images/post-placeholder.svg"
reading_time: "3 min read"
---

This is an example post — copy this file to start a new one. The file name
encodes the date and slug: `YYYY-MM-DD-my-title.md`.

## Why this blog exists

A lot of fascinating work in AI and NLP never reaches the people it affects,
because it's locked behind jargon and paywalls. Here I'll write **accessible
explainers** — including plain-language walkthroughs of my own papers.

## Formatting cheatsheet

You write posts in Markdown. A few things you'll use often:

- **Bold** and _italics_, and `inline code`.
- Links: [like this](https://example.com).
- Images: `![alt text](/assets/images/diagram.png)`

> Block quotes are handy for highlighting a key idea or a quote from a paper.

```python
# Code blocks get syntax highlighting:
def attention(q, k, v):
    return softmax(q @ k.T) @ v
```

### Linking to a paper with a clickable image card

Inside a post you can reuse the same card component as the rest of the site:

{% include card.html
    url="https://arxiv.org/abs/1706.03762"
    image="/assets/images/post-placeholder.svg"
    title="Attention Is All You Need"
    meta="Vaswani et al., 2017"
    badge="Paper"
    description="The paper that introduced the Transformer — explained in my next post."
    external=true %}

That's it. Delete this post once you've written your first real one.
