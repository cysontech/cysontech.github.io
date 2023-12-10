---
title: "html"
layout: archive
permalink: /html
author_profile: true
---

{% assign posts = site.categories.html %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout%} {% endfor %}
