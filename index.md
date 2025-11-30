---
layout: default
title: LargeLanguageMind
---
# LargeLanguageMind
A personal research journal documenting my evolving understanding 
of human cognition, machine learning, and the foundations of intelligence.

---

## Notes

{% assign notes = site.pages 
   | where_exp: "page", "page.path contains 'notes/'" 
   | sort: "path" %}

<ul>
{% for note in notes %}
  <li>
    <a href="{{ note.url | relative_url }}">
      {{ note.title | default: note.path }}
    </a>
  </li>
{% endfor %}
</ul>
