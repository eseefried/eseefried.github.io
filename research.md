---
layout: default
title: Research
---

<style>
  .card-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); /* Responsive columns */
    gap: 20px;
    margin: 20px;
  }
  .card {
    display: flex;
    flex-direction: column;
    background: #f9f9f9;
    border: 1px solid #ddd;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
    transition: box-shadow 0.3s ease-in-out;
    min-height: 300px; /* Ensures all cards are at least 300px tall */
  }
  .card:hover {
    box-shadow: 5px 5px 15px rgba(0,0,0,0.2);
  }
  .card img {
    width: 100%;
    height: 60%; /* Fixed height for all images */
    object-fit: cover;
  }
  .container {
    padding: 15px;
    text-align: center;
    flex-grow: 1; /* Ensures content container fills available space */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  @media (max-width: 600px) {
    .card-container {
      grid-template-columns: 1fr; /* One column on small screens */
    }
    .card img {
      height: 100px; /* Smaller images on small screens */
    }
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

