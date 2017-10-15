---
layout: default
---

<section class="articles">
{% for post in site.posts %}
  {% if post.link %}
    {% include linked.html post_content = post %}
  {% else %}
    {% if post.tags contains 'snippet' %}
      {% include snippet.html post_content = post %}
    {% else %}
      {% include post.html post_content = post %}
    {% endif %}
  {% endif %}
{% endfor %}
</section>