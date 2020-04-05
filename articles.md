---
layout: page
title: articles
---

{% for category in site.tags %}
  <h3><a name="{{ category[0] }}" class="anchors">{{ category[0] }} </a></h3>
  <ul>
    {% for post in category[1] %}
      <li>
        <h3>
          <a href="{{ post.url }}">{{ post.title }}
            <small>{{ post.date | date_to_string }}</small>
          </a>
        </h3>
      </li>
    {% endfor %}
  </ul>
{% endfor %}