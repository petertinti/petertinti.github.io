---
layout: default
title: "Photography"
---

{% assign photo_essays = site.pages | where_exp: "page", "page.path contains 'photography/'" | where_exp: "page", "page.name == 'index.md'" | sort: "order" %}

<div class="gallery-grid">
    {% for essay in photo_essays %}
    <div class="gallery-item">
        <a href="{{ essay.url | relative_url }}">
            <img src="{{ essay.url }}{{ essay.featured_image }}" alt="{{ essay.title }}" loading="lazy">
        </a>
        <h3 class="project-title">{{ essay.title }}</h3>
    </div>
    {% endfor %}
</div>