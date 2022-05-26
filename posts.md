---
title: Posts
---
{% for post in site.posts %}
  <article>
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    {{ post.content }}
  </article>
{% endfor %}

{%- assign default_paths = site.pages | map: "path" -%}
{%- assign page_paths = site.header_pages | default: default_paths -%}

### Debug
{% for page in page_paths %}
  {{ page }}
{% endfor %}
