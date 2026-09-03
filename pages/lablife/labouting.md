---
layout: page
title: LAB OUTING
permalink: /lablife/labouting/
hide: true
---

<div class="news-timeline">

{% assign outings = site.labouting | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for outing in outings %}

{% assign outing_year = outing.date | date: "%Y" %}

{% if outing_year != current_year %}
{% assign current_year = outing_year %}
<h2 class="timeline-year">{{ current_year }}</h2>
{% endif %}

<div class="timeline-item">

  <div class="timeline-date">
    {{ outing.date | date: "%d %b" }}
  </div>

  <div class="timeline-content">

    {% if outing.thumbnail %}
    <div class="timeline-thumb">
      <a href="{{ outing.url | relative_url }}">
        <img src="{{ outing.thumbnail | relative_url }}" alt="{{ outing.title }}">
      </a>
    </div>
    {% endif %}

    <div class="timeline-text">

      <h3>
        <a href="{{ outing.url | relative_url }}">
          {{ outing.title }}
        </a>
      </h3>

      <p>
        {{ outing.excerpt | strip_html | truncate: 180 }}
      </p>

      <a href="{{ outing.url | relative_url }}">
        Read More →
      </a>

    </div>

  </div>

</div>

{% endfor %}

</div>