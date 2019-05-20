---
layout: page
title: Machine Learning
---
Here you'll find creative projects, mostly generative art and interactive demos.

<!-- Simple unorderd list -->
<!-- <ul>
  {% for item in site.MachineLearning %}
    <li>
      <a href="{{ item.url }}">{{ item.title }}</a>
      - {{ item.tagline }}
    </li>
  {% endfor %}
</ul> -->


<!-- Tiled with thumbnails - hover mouse to show title + description-->
<div class="row">
    {% assign projects = site.MachineLearning %}
    {% for project in projects %}
      <div class="col-lg-4 col-md-4 col-sm-6">
          <a href="{{ project.url | relative_url }}">
              <div class="img__wrap">
              {%if project.thumbnail %}
                <img class="img__img" width="200" src="{{site.baseurl}}/{{ project.url | replace: "/", " " | truncatewords: 2, "" | replace: " ", "/" }}/{{ project.thumbnail }}">
              {% else %}
                <img class="img__img" width="200" src="{{ "assets/default_thumbnail.png" | relative_url }}">
              {% endif %}
                <div class="img__description_layer">
                    <p class="img__description">{{ project.title }}<br>{{ project.tagline }}</p>
                </div>
            </div>
          </a>
    </div>

    {% endfor %}
</div>
