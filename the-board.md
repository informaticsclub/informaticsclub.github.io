---
layout: page
title: Executive Board
subtitle: Meet Our Executive Board
---

<style>
  .team-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  
  .member-container {
    width: 23%; /* Adjusting for margins and spacing */
    text-align: center;
    margin-bottom: 1em;
  }

  .member-container img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover; /* Ensure the image is properly cropped within the circle */
  }

  @media (max-width: 768px) {
    .member-container {
      width: 48%; /* For smaller screens, show 2 per row */
    }
  }

  @media (max-width: 480px) {
    .member-container {
      width: 100%; /* For very small screens, show 1 per row */
    }
  }
</style>

<div class="team-container">
  {% for member in site.data.team %}
    <div class="member-container">
      <img src="{{ member.image }}" alt="{{ member.name }}">
      <div>
        <strong>{{ member.name }}</strong>
        {{ member.role }}
      </div>
      <br>
      <br>
    </div>
  {% endfor %}
</div>
