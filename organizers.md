---
layout: default
title: Organizers
nav_order: 6
---

# Organizers
<br>

<div class="people-container">
  {% for person in site.data.organizers %}
    <div class="people-card">
      <img class="person-image" src="{{ person.image | relative_url }}">
      <div class="person-high">{{ person.name }}</div>
      <div>{{ person.email }}</div>
      <div>{{ person.website }}</div>
      <div>{{ person.position }}</div>
      <div>{{ person.institution }}</div>
      <div class="person-high">Bio</div>
      <div class="person-card-bio">{{ person.bio }}</div>
    </div>
  {% endfor %}
</div>