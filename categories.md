---
layout: categories
---

<h1>{{ page.title }}</h1>

<ul>
  {% for category in site.categories %}
    <li>
      <h2>{{ category[0] }}</h2>
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
