---
layout: about
title: about
permalink: /
subtitle: University of Illinois Urbana-Champaign

# profile:
#   align: right
#   image: prof_pic.jpg
#   image_circular: false # crops the image to make it circular
#   address: >
#     <p>555 your office number</p>
#     <p>123 your address street</p>
#     <p>Your City, State 12345</p>

news: false  # includes a list of news items
latest_posts: false  # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page


horizontal: true

---

Modern real-time scheduling theory was started by Professor David Liu at UIUC with his seminal paper [Scheduling Algorithms for Multiprogramming in a Hard Real-Time Environment](http://www.newslab.csie.ntu.edu.tw/course/rts2011/papers/Scheduling%20Algorithms%20for%20Multiprogramming%20in%20%20a%20Hard-Real-Time%20Environment%20.pdf).
Built upon this pioneering work, Professor Lui Sha and his collaborators created the modern real-time scheduling theory that transformed the real-time computing standards and impacted [many national high technology projects](http://publish.illinois.edu/cpsintegrationlab/files/2012/02/Space.pdf).


## selected projects
---

<!-- pages/projects.md -->
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% if project.selected -%}
        {% include projects_horizontal.html %}
      {%- endif -%}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% if project.selected -%}
        {% include projects.html %}
      {%- endif -%}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>

