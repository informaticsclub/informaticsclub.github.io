---
layout: page
title: Events
subtitle: Attend our upcoming events and access resources from previous events.
permalink: /events/
---

We host regular workshops, seminars, and social events throughout the academic year.

**A light lunch is always served at Code, Chat, & Collab.**

## Upcoming Events

{% include event-table.html events=site.data.upcoming-events type="upcoming" %}

## Previous Events

{% assign reversed_events = site.data.previous-events | reverse %}
{% include event-table.html events=reversed_events type="previous" %}

{% for event in site.data.upcoming-events %}
{% if event.start_datetime %}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Event",
  "name": {{ event.title | jsonify }},
  "startDate": "{{ event.start_datetime }}",
  {% if event.end_datetime %}"endDate": "{{ event.end_datetime }}",{% endif %}
  "location": {
    "@type": "Place",
    "name": {{ event.location | jsonify }}
  },
  "organizer": {
    "@type": "Organization",
    "name": {{ site.title | jsonify }}
  },
  "eventAttendanceMode": "{% if event.mode == 'Hybrid' %}https://schema.org/MixedEventAttendanceMode{% elsif event.mode == 'Virtual' %}https://schema.org/OnlineEventAttendanceMode{% else %}https://schema.org/OfflineEventAttendanceMode{% endif %}"
}
</script>
{% endif %}
{% endfor %}
