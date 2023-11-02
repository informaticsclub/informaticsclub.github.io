---
layout: page
title: Events
---

<table>
  <thead>
    <tr>
      <th>Event Name</th>
      <th>Location</th>
      <th>Time</th>
      <th>Zoom</th>
      <th>Calendar Link</th>
    </tr>
  </thead>
  <tbody>
    {% for event in site.data.events %}
    <tr>
      <td>{{ event.name }}</td>
      <td>{{ event.location }}</td>
      <td>{{ event.time }}</td>
      <td>
        {% if event.zoom %}
          <a href="{{ event.zoom }}">Link</a>
        {% else %}
          N/A
        {% endif %}
      </td>
      <td><a href="{{ event.calendar }}">.ics file</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>