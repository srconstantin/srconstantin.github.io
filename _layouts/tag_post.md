---
layout: post
---

<h1>{{ page.title }}</h1>

{% if page.tags != empty %}
<ul class="tags">
  {% for tag in page.tags %}
  <li>
    <a href="/tag/{{ tag }}.html">{{ site.data.tags[tag].name }}</a>
  </li>{% endfor %}
</ul><br>
{% endif %}

<article>
  {{ content }}
</article>

