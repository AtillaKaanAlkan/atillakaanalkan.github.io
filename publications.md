---
layout: page
title: Publications
subtitle: Peer-reviewed papers and preprints
permalink: /publications/
---

Each card links to the paper. To add or edit entries, edit
`_data/publications.yml`. Below they are grouped by year, newest first.

<!-- Build a sorted list of unique years, descending -->
{% assign years = site.data.publications | map: "year" | uniq | sort | reverse %}

{% for year in years %}
  <h2 class="pub-year">{{ year }}</h2>
  <div class="card-grid">
    {% for pub in site.data.publications %}
      {% if pub.year == year %}
        {% include card.html
            url=pub.url image=pub.image title=pub.title
            meta=pub.venue badge=pub.badge description=pub.description external=true %}
      {% endif %}
    {% endfor %}
  </div>
{% endfor %}

{% if site.social.scholar != "" %}
<p style="margin-top:2rem">
  See also my <a href="{{ site.social.scholar }}" target="_blank" rel="noopener">Google Scholar profile</a>.
</p>
{% endif %}
