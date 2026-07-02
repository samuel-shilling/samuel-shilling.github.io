---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

---

Below are links to some examples of my research.

---
<!-- {% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid"%}
{% endfor %} -->


<div class="grid__wrapper">
{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>