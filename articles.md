---
layout: page
title: articles
---

{% for category in site.tags %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li>
        <h3>
          <a href="{{ post.url }}">{{ post.title }}
            <small>{{ post.date | date_to_string }}</small>
          </a>
          <div class="message">
            {{ post.excerpt }}
          </div>
        </h3>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
  