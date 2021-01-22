---
title: Operations
description: "Patterns that focus on the technical and architectural aspects of how to build and operate Cloud Native services whilst ensuring their reliability and security."
layout: default
---

<table>
{% tablerow pattern in site.operations cols:2 %}
  <a href="{{ site.baseurl }}{{ pattern.url }}" class="button technical"></a>
  <a href="{{ site.baseurl }}{{ pattern.url }}">{{ pattern.title }}</a>
{% endtablerow %}
</table>
