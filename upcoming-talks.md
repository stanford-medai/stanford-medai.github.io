---
layout: default
title: Upcoming Talks
nav_order: 3
---

# Upcoming Talks

<div class="talks-list">
  {% for talk in site.data.talks %}
    {% if talk.type == 'upcoming' %}
      <!-- <br> -->
      <hr>
      <div class="talk-container">
        <h3 class="talk-presenter">({{ talk.date }}) Speaker: {{ talk.speaker }}</h3>
        {% if talk.title %}
          <div class="talk-subtitle">Title</div>
          <div>{{ talk.title }}</div>
        {% endif %}
          {% if talk.abstract %}
            <div class="talk-subtitle">Abstract</div>
            <div> {{ talk.abstract}}</div>
          {% endif %}
          {% if talk.bio %}
            <div class="talk-subtitle">Bio</div>
            <div> {{ talk.bio}}</div>
          {% endif %}  
          {% if talk.recording %}
            <div class="talk-subtitle">Video</div>
            <div><a href="{{ talk.recording }}">Video Recording</a></div>
          {% elsif talk.livestream %}
            <div class="talk-subtitle">Video</div>
            <div><a href="{{ talk.livesteam }}">Livestream Link</a></div>
          {% endif %}        
      </div>
    {% endif %}
  {% endfor %}
</div>