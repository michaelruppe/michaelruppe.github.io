---
layout: page
title: Machine Learning
---
Here you'll find creative projects, mostly generative art and interactive demos.

<ul>
  {% for item in site.MachineLearning %}
    <li>
      <a href="{{ item.url }}">{{ item.title }}</a>
      - {{ item.tagline }}
    </li>
  {% endfor %}
</ul>