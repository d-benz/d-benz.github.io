---
layout: post
title: "Newsletter Archive"
permalink: /newsletter/
---

{% assign sorted = site.newsletter | sort: "newsletter_date" | reverse %}

{% for item in sorted %}
  <h3><a href="{{ item.url }}">{{ item.title }}</a></h3>
  <p>{{ item.newsletter_date | date: "%B %d, %Y" }}</p>
{% endfor %}
