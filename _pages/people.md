---
layout: page
permalink: /people/
title: people
description: 
nav: true
nav_order: 5
---

<style>
.people-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.person {
  width: calc(33.33% - 20px); /* Adjust the width as needed for the desired number of entries per row */
  margin-bottom: 20px;
  text-align: center;
}

.person-photo {
  width: auto;
  height: 150px;
  border-radius: 50%;
  margin-bottom: 10px;
}

.person-name {
  font-weight: bold;
  font-size: 1.2em; /* Adjust the font size as needed */
}

.person-designation {
  color: #666;
}

.person-note {
  font-size: 0.8em;
  color: #999;
}

</style>


{% assign people_by_designation = site.data.people | group_by: "designation" %}

{% for group in people_by_designation %}
<h2>{{ group.name }}</h2>
<div class="people-grid">
  {% for person in group.items %}
  <div class="person">
    <img src="{{ person.photo }}" alt="{{ person.name }}" class="person-photo">
    <div class="person-info">
      {% if person.url %}
        <h2 class="person-name"><a href="{{ person.url }}">{{ person.name }}</a></h2>
      {% else %}
        <h2 class="person-name">{{ person.name }}</h2>
      {% endif %}
      {% if person.note %}
        <p class="person-note">{{ person.note }}</p>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>
{% endfor %}


