---
layout: default
title: Projects
---

<div class="card-container">
  {% for project in site.projects %}
    <div class="card" onclick="location.href='{{ project.url }}';" style="cursor: pointer;">
      <img src="{{ project.image }}" alt="{{ project.title }}" style="width:20%">
      <div class="container">
        <h4><b>{{ project.title }}</b></h4>
        <p>{{ project.description | truncatewords: 20 }}</p>
      </div>
    </div>
  {% endfor %}
</div>
