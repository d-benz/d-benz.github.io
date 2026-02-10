---
layout: page
title: "Newsletter Archive"
permalink: /newsletter/
css: index
---

<div class="archive-grid">
{% assign sorted = site.newsletter | sort: "newsletter_date" | reverse %}

{% for item in sorted %}
  <div class="archive-item">
    <h3 class="archive-date">
      <a href="{{ item.url }}">
        {{ item.newsletter_date | date: "%B %d, %Y" }}
      </a>
    </h3>

    {% assign raw = item.content %}
    {% assign summary = raw | split: '<!-- summary:' | last | split: '-->' | first | strip %}

    {% if summary != raw %}
      <p class="archive-summary">{{ summary }}</p>
    {% endif %}
  </div>
{% endfor %}
</div>



