---
layout: cards
title: Projects
---

<div class="card-container">
  {% for project in site.projects %}
    <div class="card">
      <a href="{{ project.url }}">
        <img src="{{ project.image }}" alt="{{ project.title }}" class="card-image">
        <div class="card-content">
          <h4>{{ project.title }}</h4>
          <p>{{ project.description | truncatewords: 20 }}</p>
        </div>
      </a>
    </div>
  {% endfor %}
</div>
