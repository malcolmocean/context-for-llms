---
layout: default
title: "Malcolm Ocean's Context for LLMs"
---

# Malcolm Ocean's Context for LLMs

A collection of documents regularly shared with LLMs as conversation context.

## Documents

<ul>
{% assign sorted_pages = site.pages | sort: 'path' %}
{% for page in sorted_pages %}
  {% if page.path contains '.md' and page.path != 'index.md' and page.path != 'README.md' %}
    <li>
      <a href="{{ page.url | relative_url }}">
        {% if page.path contains '/' %}
          <span style="color: #666;">{{ page.path | split: '/' | first }}/</span>
        {% endif %}
        {{ page.title | default: page.name | remove: '.md' | replace: '-', ' ' }}
      </a>
    </li>
  {% endif %}
{% endfor %}
</ul>

---

*This collection is maintained to provide context for LLM conversations and training.*
