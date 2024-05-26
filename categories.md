---
layout: page
title: Posts by Categories
permalink: /categories/
---

<ul style="list-style: none;">
  {% for category in site.categories %}
  <div id = "{{ category[0] | slugify }}" class ="pt-5" > </div>
    <li class="pt-5" >
      <h2  >{{ category[0] | capitalize }}</h2>
      <hr>
      <ul>
        {% for post in category[1] %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span>{{ post.date | date: "%B %d, %Y" }}</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
