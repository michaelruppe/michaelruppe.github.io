---
layout: page
title: Misc. Projects
---
Here you'll find miscellaneous coding projects. Stuff that doesn't really fit in with any other category on the site.

<ul>
  {% for item in site.MiscProjects %}
    <li>
      <a href="{{ item.url }}">{{ item.title }}</a>
      - {{ item.tagline }}
    </li>
  {% endfor %}
</ul>
