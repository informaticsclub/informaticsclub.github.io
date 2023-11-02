---
layout: page
title: Executive Board
subtitle: Meet Our Executive Board
---

{% for member in site.data.team %}
<div class="member-container">
  <img src="{{ member.image }}" alt="{{ member.name }}" style="width:150px;height:auto;">
  <div>
    <strong style="margin-bottom: 0.5em;">{{ member.name }}</strong>
    <p style="margin-top: 0.5em;">{{ member.role }}</p>
  </div>
</div>
{% endfor %}
