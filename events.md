---
layout: page
title: Events
---

#### Zoom link for Informatics Club: [https://uab.zoom.us/my/informaticsclub](https://uab.zoom.us/my/informaticsclub)

<table>
  <thead>
    <tr>
      <th>Event Name</th>
      <th>Date</th>
      <th>Time</th>
      <th>Mode</th>
      <th>Location</th>
      <th>Flyer</th>
      <th>Zoom</th>
      <th>Calendar Link</th>
    </tr>
  </thead>
  <tbody>
    {% for event in site.data.events %}
    <tr>
      <td>{{ event.name }}</td>
      <td>{{ event.date }}</td>
      <td>{{ event.time }}</td>
      <td>{{ event.mode }}</td>
      <td>{{ event.location }}</td>
      <td><a href="{{ event.flyer }}">Link</a></td>
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
