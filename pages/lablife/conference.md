---
layout: page
title: Conferences
permalink: lablife/conference/
hide: true
---

{% assign conferences = site.conference | sort: "date" | reverse %}

{% for conference in conferences %}

  <article class="post">

    <h2>
      <a href="{{ conference.url | relative_url }}">
        {{ conference.title }}
      </a>
    </h2>

    {% if conference.date %}
      <p class="post-meta">
        {{ conference.date | date: "%d %B %Y" }}
      </p>
    {% endif %}

    {% if conference.excerpt %}
      <p>{{ conference.excerpt }}</p>
    {% endif %}

    <a href="{{ conference.url | relative_url }}">
      Read more →
    </a>

  </article>

{% endfor %}