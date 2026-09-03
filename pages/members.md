---
layout: page
title: MEMBERS
permalink: /members/
position: 2
feature-img: "assets/img/header/members.jpg"
hide: false
---

{% for member in site.data.members %}

<div class="member-card {% if member.profile %}clickable{% endif %}"
     {% if member.profile %}
     onclick="window.location='{{ member.profile | relative_url }}';"
     {% endif %}>

  <div class="member-photo-container">
    <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
  </div>

  <div class="member-info">

    <h3>{{ member.name }}</h3>

    <p class="member-position">{{ member.position }}</p>

{% if member.email %}
  <p class="member-email">
    <a href="mailto:{{ member.email }}">{{ member.email }}</a>
  </p>
{% endif %}

    <p>{{ member.description }}</p>

  </div>

</div>

{% endfor %}

# Masters/Internship students

{% for intern in site.data.interns %}

<div class="member-card {% if intern.profile %}clickable{% endif %}"
     {% if intern.profile %}
     onclick="window.location='{{ intern.profile | relative_url }}';"
     {% endif %}>

  <div class="member-photo-container">
    <img src="{{ intern.image | relative_url }}" alt="{{ intern.name }}">
  </div>

  <div class="member-info">

    <h3>{{ intern.name }}</h3>

    <p class="member-position">{{ intern.position }}</p>

    <p>{{ intern.description }}</p>

  </div>

</div>

{% endfor %}

# Laboratory staff

{% for labstaff in site.data.labstaff %}

<div class="member-card {% if labstaff.profile %}clickable{% endif %}"
     {% if intern.profile %}
     onclick="window.location='{{ labstaff.profile | relative_url }}';"
     {% endif %}>

  <div class="member-photo-container">
    <img src="{{ labstaff.image | relative_url }}" alt="{{ labstaff.name }}">
  </div>

  <div class="member-info">

    <h3>{{ labstaff.name }}</h3>

    <p class="member-position">{{ labstaff.position }}</p>

{% if labstaff.email %}
  <p class="member-email">
    <a href="mailto:{{ labstaff.email }}">{{ labstaff.email }}</a>
  </p>
{% endif %}

    <p>{{ labstaff.description }}</p>

  </div>

</div>

{% endfor %}


# Collaborators

<div class="collaborators-list">

<h2>National</h2>

{% for collaborator in site.data.collaborators %}
{% if collaborator.type == "national" %}

<div class="collaborator-entry">

  <div class="collaborator-name">{{ collaborator.name }}</div>

  <div class="collaborator-affiliation">{{ collaborator.affiliation }}</div>

{% if collaborator.project %} <div class="collaborator-project">Project: {{ collaborator.project }}</div>
{% endif %}

{% if collaborator.duration %} <div class="collaborator-duration">{{ collaborator.duration }}</div>
{% endif %}

</div>

{% endif %}
{% endfor %}

<h2>International</h2>

{% for collaborator in site.data.collaborators %}
{% if collaborator.type == "international" %}

<div class="collaborator-entry">

  <div class="collaborator-name">{{ collaborator.name }}</div>

  <div class="collaborator-affiliation">{{ collaborator.affiliation }}</div>

{% if collaborator.project %} <div class="collaborator-project">Project: {{ collaborator.project }}</div>
{% endif %}

{% if collaborator.duration %} <div class="collaborator-duration">{{ collaborator.duration }}</div>
{% endif %}

</div>

{% endif %}
{% endfor %}

</div>


# Alumni

{% for alum in site.data.alumni %}

<div class="alumni-entry">

  <strong>{{ alum.name }}</strong><br>

  {{ alum.position }}

  {% if alum.duration %}
    <br><em>{{ alum.duration }}</em>
  {% endif %}

  {% if alum.current-position %}
    <br>Current position: {{ alum.current-position }}
  {% endif %}

</div>

{% endfor %}
