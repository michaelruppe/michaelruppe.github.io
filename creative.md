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

<ul>
    {% for doc in site.docs %}
        <li><a href="{{ doc.url }}">{{ doc.title }}</a></li>
    {% endfor %}
</ul>

after
