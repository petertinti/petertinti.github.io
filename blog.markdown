---
layout: default
title: "Blog"
---

{% for post in site.posts %}
  <article class="blog-post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="post-meta">
      <time class="post-date">{{ post.date | date: "%B %d, %Y" }}</time>
      {% if post.author %}
        <span class="post-author">by {{ post.author }}</span>
      {% endif %}
    </div>
    
    {% if post.tags and post.tags.size > 0 %}
      <div class="post-tags">
        {% for tag in post.tags %}
          <span class="tag">#{{ tag }}</span>
        {% endfor %}
      </div>
    {% endif %}
    
    {% if post.description %}
      <p class="post-description">{{ post.description }}</p>
    {% elsif post.excerpt %}
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    {% endif %}
  </article>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>No blog posts yet.</p>
{% endif %}