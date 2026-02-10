---
layout: post
title: "Newsletter Archive"
permalink: /newsletter/
---

{% for item in site.newsletter %}
  <h3><a href="{{ item.url }}">{{ item.title }}</a></h3>
  <p>{{ item.newsletter_date | date: "%B %d, %Y" }}</p>
{% endfor %}