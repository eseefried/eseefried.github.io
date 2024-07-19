---
layout: default
title: Projects
---

<style>
  .card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Creates a three-column grid */
    gap: 20px; /* Adds space between the cards */
    margin: 20px;
  }
  .card {
    background: #f9f9f9;
    border: 1px solid #ddd;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
    transition: box-shadow 0.3s ease-in-out;
  }
  .card:hover {
    box-shadow: 5px 5px 15px rgba(0,0,0,0.2);
  }
  .card img {
    width: 100%; /* Makes the image cover the width of the card */
    height: auto; /* Adjusts the height to maintain aspect ratio */
  }
  .container {
    padding: 15px;
    text-align: center;
  }
</style>

<div class="card-container">
  {% for project in site.projects %}
    <div class="card" onclick="location.href='{{ project.url }}';" style="cursor: pointer;">
      <img src="{{ project.image }}" alt="{{ project.title }}">
      <div class="container">
        <h4><b>{{ project.title }}</b></h4>
        <p>{{ project.description | truncatewords: 20 }}</p>
      </div>
    </div>
  {% endfor %}
</div>

