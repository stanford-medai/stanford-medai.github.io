---
layout: default
title: Previous Talks
nav_order: 4
---

# Previous Talks

<div class="talks-list">
  {% for talk in site.data.talks reversed %}
    {% if talk.type == 'previous' %}
      <!-- <br> -->
      <hr>
      <div class="talk-container">
        <h3 class="talk-presenter">({{ talk.date }}) Speaker: {{ talk.speaker }}</h3>
        <h4>{{ talk.institution }}</h4>
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
            <div><a href="{{ talk.livestream }}">Livestream Link</a></div>
          {% elsif talk.abstract %}
            <div class="talk-subtitle">Video</div>
            <div>Session not recorded on request</div>
          {% endif %} 
          {% if talk.abstract %}
            <div class="talk-subtitle">Questions for the Speaker</div>
            <div>Please add your questions to the speaker either to this <a href="https://forms.gle/229GT2yi35NHqHje8" target="_blank">google form</a> or directly under the <a href="https://www.youtube.com/channel/UCOkkljs06NPPkjNysCdQV4w" target="_blank">YouTube video</a></div>
          {% endif %}
      </div>
    {% endif %}
  {% endfor %}
</div>
