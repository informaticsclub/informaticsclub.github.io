---
layout: page
title: Events
---

Food is always served at our Code, Chat, & Collab events.

The following Zoom link can be accessed for all our events: [https://uab.zoom.us/my/informaticsclub](https://uab.zoom.us/my/informaticsclub)

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Name</th>
      <th>Date</th>
      <th>Time</th>
      <th>Mode</th>
      <th>Location</th>
      <th>Flyer</th>
      <th>Resources</th>
<!--       <th>Zoom</th>
      <th>Calendar Link</th> -->
    </tr>
  </thead>
  <tbody>
    {% for event in site.data.events %}
    <tr>
      <td>{{ event.name }}</td>
      <td>{{ event.title }}</td>
      <td>{{ event.date }}</td>
      <td>{{ event.time }}</td>
      <td>{{ event.mode }}</td>
      <td>{{ event.location }}</td>
      <td><a href="{{ event.flyer }}">Link</a></td>
      <td>
        {% if event.resources %}
          <a href="{{ event.resources }}"><i class="fab fa-github fa-stack-1x fa-inverse"></i></a>
        {% else %}
          N/A
        {% endif %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>
