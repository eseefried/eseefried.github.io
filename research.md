---
layout: default
title: Research
---

<style>
  .card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Creates a three-column grid */
    gap: 20px; /* Adds space between the cards */
    margin: 20px;
  }
  .card {
    display: flex;
    flex-direction: column;
    justify-content: space-between; /* Ensures the footer stays at the bottom */
    background: #f9f9f9;
    border: 1px solid #ddd;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
    transition: box-shadow 0.3s ease-in-out;
    height: 100%; /* Makes all cards the same height */
  }
  .card:hover {
    box-shadow: 5px 5px 15px rgba(0,0,0,0.2);
  }
  .card img {
    width: 100%; /* Makes the image cover the width of the card */
    height: 60%; /* Adjusts the height automatically */
    object-fit: cover; /* Ensures the image covers the area, might crop */
  }
  .container {
    padding: 15px;
    text-align: center;
    flex-grow: 1; /* Allows the container to fill the available space */
  }
</style>

<div class="card-container">
  {% for research in site.research %}
    <div class="card" onclick="location.href='{{ research.url }}';" style="cursor: pointer;">
      <img src="{{ research.image }}" alt="{{ research.title }}">
      <div class="container">
        <h4><b>{{ research.title }}</b></h4>
        <p>{{ research.description | truncatewords: 20 }}</p>
      </div>
    </div>
  {% endfor %}
</div>

