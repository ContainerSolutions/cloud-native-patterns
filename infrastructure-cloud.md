---
title: Infrastructure & Cloud Patterns
description: Patterns that help in discovering and choosing the right infrastructure, while avoiding common pitfalls like vendor lock-in and building unnecessary custom solutions.
layout: default
---

<table>
{% tablerow pattern in site.infrastructure-cloud cols:2 %}
  <a href="{{ site.baseurl }}{{ pattern.url }}" class="button infrastructure-cloud"></a>
  <a href="{{ site.baseurl }}{{ pattern.url }}">{{ pattern.title }}</a>
{% endtablerow %}
</table>
