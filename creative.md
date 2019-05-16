---
layout: page
title: Creative Projects
---
Here you'll find creative projects, mostly Generative art and interactive demos.

<!-- <ul>
   {% for item in site.data.creative-projects.docs %}
      <li><a href="{{ item.url }}">{{ item.title }}</a></li>
   {% endfor %}
</ul> -->
Before

{% for cat in site.docs %}
<h2>{{ cat.name | capitalize }}</h2>
    <ul>
        <li><a href="{{ item.url }}">{{ item.title }}</a></li>
    </ul>
{% endfor %}

after
