---
title: Technical Patterns
description: "Yadayada."
layout: default
---

<table>
{% tablerow pattern in site.technical cols:2 %}
  <a href="{{ site.baseurl }}{{ pattern.url }}" class="button technical"></a>
  <a href="{{ site.baseurl }}{{ pattern.url }}">{{ pattern.title }}</a>
{% endtablerow %}
</table>
