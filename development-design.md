---
title: Development & Design Patterns
description: "Patterns for how to design, build, and deliver products/services in this new paradigm: architecture and processes that support Cloud Native’s fast and responsive delivery dynamic."
layout: default
---

<table>
{% tablerow pattern in site.development-design cols:2 %}
  <a href="{{ pattern.url }}" class="button development-design"></a>
  <a href="{{ pattern.url }}">{{ pattern.title }}</a>
{% endtablerow %}
</table>
