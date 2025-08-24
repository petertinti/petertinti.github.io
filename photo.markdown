---
layout: default
title: "Photo"
---

<div class="content-container">
    <div class="gallery-grid">
        {% for project in site.projects %}
        <div class="gallery-item">
            <a href="{{ project.url | relative_url }}">
                {% if project.featured_image %}
                <img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}" loading="lazy">
                {% else %}
                <img src="/assets/images/placeholder.jpg" alt="{{ project.title }}" loading="lazy">
                {% endif %}
            </a>
            <h3 class="project-title">{{ project.title }}</h3>
        </div>
        {% endfor %}
    </div>
</div>