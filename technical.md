---
title: Technical Patterns
description: "Patterns that focus on how to manage and operate Cloud Native services whilst ensuring their reliability and security."
layout: default
---

<table>
{% tablerow pattern in site.technical cols:2 %}
  <a href="{{ site.baseurl }}{{ pattern.url }}" class="button technical"></a>
  <a href="{{ site.baseurl }}{{ pattern.url }}">{{ pattern.title }}</a>
{% endtablerow %}
</table>
