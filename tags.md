---
layout: page
title: Posts by Tags
permalink: /tags/
---

<ul>
  {% for tags in site.tags %}
  <div id = "{{ tags[0] | slugify }}" class ="pt-5" > </div>
    <li class="pt-5"  >
      <h2 >{{ tags[0] | capitalize }}</h2>
      <hr>
      <ul>
        {% for post in tags[1] %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span>{{ post.date | date: "%B %d, %Y" }}</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
