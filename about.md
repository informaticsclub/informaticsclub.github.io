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

![Campus Impact Award ceremony](/assets/img/campus-impact.jpg){:.about-photo}

We have also co-sponsored and supported programming workshops. In fact, after the height of the pandemic, the Informatics Club was one of the first student organizations to host an in-person workshop at UAB with the help of Dr. Blake Joyce and UAB's Research Computing.

<div class="columns is-centered is-vcentered is-variable is-4 about-photo-row">
  <div class="column is-half">
    <img src="/assets/img/hackathon.png" alt="Hackin' Omics hackathon participants" class="about-photo" loading="lazy">
  </div>
  <div class="column is-half">
    <img src="/assets/img/blake-python.png" alt="Informatics Club workshop with Dr. Blake Joyce" class="about-photo" loading="lazy">
  </div>
</div>

<style>
.content .about-photo {
  display: block;
  width: 100%;
  max-width: 100%;
  height: auto;
  margin: 1.25rem auto;
  border-radius: var(--radius-sm, 8px);
}
.content .about-photo-row {
  margin: 1.25rem 0;
  align-items: stretch;
}
.content .about-photo-row .column {
  display: flex;
}
.content .about-photo-row .about-photo {
  margin: 0;
  width: 100%;
  height: clamp(220px, 32vw, 360px);
  object-fit: cover;
  object-position: center;
}
@media screen and (max-width: 768px) {
  .content .about-photo-row .column + .column {
    margin-top: 1rem;
  }
}
</style>

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
