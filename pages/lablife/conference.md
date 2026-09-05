---
layout: page
title: CONFERENCES & WORKSHOPS
permalink: /lablife/conference/
hide: true
---

<div class="news-timeline">

{% assign conferences = site.conference | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for conference in conferences %}

{% assign conference_year = conference.date | date: "%Y" %}

{% if conference_year != current_year %}
{% assign current_year = conference_year %}
<h2 class="timeline-year">{{ current_year }}</h2>
{% endif %}

<div class="timeline-item">

  <div class="timeline-date">
    {{ conference.date | date: "%d %b" }}
  </div>

  <div class="timeline-content">

    {% if conference.thumbnail %}
    <div class="timeline-thumb">
      <a href="{{ conference.url | relative_url }}">
        <img src="{{ conference.thumbnail | relative_url }}" alt="{{ conference.title }}">
      </a>
    </div>
    {% endif %}

    <div class="timeline-text">

      <h3>
        <a href="{{ conference.url | relative_url }}">
          {{ conference.title }}
        </a>
      </h3>

      <p>
        {{ conference.excerpt | strip_html | truncate: 180 }}
      </p>

      <a href="{{ conference.url | relative_url }}">
        Read More →
      </a>

    </div>

  </div>

</div>

{% endfor %}

</div>