---
layout: page
title: About
subtitle: Learn more about the history of the Informatics Club.
permalink: /about/
---

## Mission

The Informatics Club was founded to foster a community for UAB students and trainees
who are interest in informatics (including bioinformatics and health/clinical informatics)
through professional development, social activites, and community service.

## History

In the fall of 2019, the Informatics Club was founded by a group of UAB students including former president, Dr. Tarun
Mamidi. The club has since grown to include a diverse group of students and trainees from various disciplines
including computer science, biomedical sciences, dentistry, health informatics, and medicine.

Over the last few years, our club has organized a virtual hackathon ([Hackin' Omics in 2022](https://hackathon.ubrite.org/hackathon-2022/)) with over 100 participants and received the Campus Impact Award from UAB's Student Involvement and Leadership Office in April 2023.

![award-photograph](/assets/img/campus-impact.jpg)

We have also co-sponsored and supported programming workshops. In fact, after the height of the pandemic, the Informatics Club was one of the first student organizations to host an in-person workshop at UAB with the help of Dr. Blake Joyce and UAB's Research Computing.

![Informatics Club workshop with Dr. Blake Joyce](/assets/img/blake-python.png)

## Previous Presidents

- Dr. Tarun Mamidi (2019-2021)
- Ari Ginsparg (2021-2023)
- Samuel Bharti (2023-2025)
- Dev Raj Bhattarai (2025-Present)

{% if site.data.alumni.size > 0 %}

## Previous Executive Board Members

<ul>
{% for member in site.data.alumni %}
  <li>
    <strong>{{ member.name }}</strong> &mdash; {{ member.role }} ({{ member.years }})
    {% if member.current_position %}<br><em>{{ member.current_position }}</em>{% endif %}
    {% if member.github %}
      <a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener"><i class="fab fa-github"></i></a>
    {% endif %}
    {% if member.linkedin %}
      <a href="https://linkedin.com/in/{{ member.linkedin }}" target="_blank" rel="noopener"><i class="fab fa-linkedin"></i></a>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}
