---
layout: page
title: Events
subtitle: Attend our upcoming events and access resources from previous events.
---
Food (either lunch or light snacks) is always served at our Code, Chat, & Collab events!

## Upcoming Events
  
<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Name</th>
      <th>Date</th>
      <th>Time</th>
      <th>Mode</th>
      <th>Location</th>
      <th>Zoom</th>
      
    </tr>
  </thead>
  <tbody>
    {% for event in site.data.upcoming-events %}
    <tr>
      <td>{{ event.name }}</td>
      <td>{{ event.title }}</td>
      <td>{{ event.date }}</td>
      <td>{{ event.time }}</td>
      <td>{{ event.mode }}</td>
      <td>{{ event.location }}</td>
      <td><a href="{{ event.zoom }}">Zoom Link</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

## Previous Events

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Name</th>
      <th>Date</th>
      <th>Time</th>
      <th>Mode</th>
      <th>Location</th>
      <th>Slides</th>
      <th>Recording</th>
    </tr>
  </thead>
  <tbody>
    {% for event in site.data.previous-events %}
    <tr>
      <td>{{ event.name }}</td>
      <td>{{ event.title }}</td>
      <td>{{ event.date }}</td>
      <td>{{ event.time }}</td>
      <td>{{ event.mode }}</td>
      <td>{{ event.location }}</td>
      <td style="text-align: center;">
        {% if event.slides %}
          <a href="{{ event.slides }}" download><i class="fas fa-download fa-lg"></i></a>
        {% else %}
          N/A
        {% endif %}
      </td>
      <td>
        {% if event.recording %}
          <a href="{{ event.recording }}"><i class="fab fa-video fa-stack-1x fa-inverse"></i></a>
        {% else %}
          N/A
        {% endif %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>
