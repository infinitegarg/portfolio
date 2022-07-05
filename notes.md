---
layout: page
title: reflections
permalink: /reflections/
---

  <!-- NOTES LIST -->

    {%- if site.notes.size > 0 -%}
    <ul class="note-list">
      {%- for post in site.notes -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <h3>
          <a class="note-link" href="{{ post.url | relative_url }}">
           {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>
  {%- endif -%}