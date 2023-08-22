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

news: true  # includes a list of news items
latest_posts: false  # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page


horizontal: true

---


### History
CPS Integration Laboratory was formerly known as Real-Time and Embedded System Laboratory established by Professors David C. L. Liu and Jane W. S. Liu. Professor Jane Liu is the pioneer of Imprecise (approximate) Real-TIme Computing Algorithms. This method is increasingly influential in soft real-time applications such as those used in the transmission of video over wireless networks.


Modern real-time scheduling theory was started by Professor David Liu at UIUC with his seminal paper [Scheduling Algorithms for Multiprogramming in a Hard Real-Time Environment](http://www.newslab.csie.ntu.edu.tw/course/rts2011/papers/Scheduling%20Algorithms%20for%20Multiprogramming%20in%20%20a%20Hard-Real-Time%20Environment%20.pdf).
Built upon this pioneering work, Professor Lui Sha and his collaborators created the modern real-time scheduling theory that transformed real-time computing standards and impacted [many national high-technology projects](http://publish.illinois.edu/cpsintegrationlab/files/2012/02/Space.pdf).

Profess David Liu is the pioneer of real-time system schedulability analysis. His paper on real-time scheduling, Scheduling Algorithms for Multiprogramming in A Hard Real-Time Environment, has over 10000 citations. He also led the transformation from ad hoc EDA to algorithmic EDA.  He was an early advocate for more rigorous design automation, arguing that powerful, formal algorithmic techniques were essential to the effective solution of complex design automation problems.  His technical contributions are at the foundation of a multitude of current EDA tools within several disciplines, including behavioral synthesis, logic synthesis, and physical design.  He received the Phil Kaufman Award in 2011. After Professors David Liu’s and Jane Liu’s retirement, Professor Lui Sha became the Director of the Laboratory in 1998.

### Research Impact

* Global Positioning Satellite:
“The navigation payload software for the next block of Global Positioning System upgrades recently completed testing. … This design would have been difficult or impossible prior to the development of rate monotonic theory”, L.  Doyle, and J. Elzey “Successful Use of Rate Monotonic Theory on A Formidable Real-Time System, technical report, p.1, ITT, Aerospace Communication Division, 1993.
International Space Station: “Through the development of Rate Monotonic Scheduling, we now have a system that will allow [Space Station] Freedom’s computers to budget their time, to choose between a variety of tasks, and decide not only which one to do first but how much time to spend in the process”, Aaron Cohen, Deputy Administrator of NASA, October 1992 (p. 3), Charting The Future: Challenges and Promises Ahead of Space Exploration.

* International Space Station:
“Dear Dr. Sha, I hope this finds you doing well. I frequently recall your efforts on everyone’s behalf in convincing IBM on RMS principles for the Space Station Software…It has been a very exciting 5 years since the reconstruction of the Station from Freedom to its present configuration [International Space Station].” ISS C&DH Architecture and Software Manager, David Pruett, NASA Johnson Space Center, January 19, 2001.

* Mars Pathfinder:
(Rescuing Mars Pathfinder when its software repeatedly crashed on Mars due to real-time computing problems) “When was the last time you saw a room of people cheer a group of computer science theorists for their significant practical contribution to advancing human knowledge? 🙂  It was quite a moment.  … For the record, the paper was L. Sha, R. Rajkumar, and J. P. Lehoczky. Priority Inheritance Protocols: An Approach to Real-Time Synchronization. In IEEE Transactions on Computers, vol. 39, pp. 1175-1185, Sep. 1990.” [reported by Dr. Michael Jones of Microsoft Research.](http://catless.ncl.ac.uk/Risks/19.49.html)

* Digital Avionics:
National Academy of Science’s Committee on Certifiably Dependable Systems wrote, “One key to achieving dependability at a reasonable cost is a serious and sustained commitment to simplicity, including simplicity of critical functions and simplicity in system interactions. This commitment is often the mark of true expertise.  There is no alternative to simplicity. Advances in technology or development methods will not make simplicity redundant; on the contrary, they will give it greater leverage”. A notable invention of our team in this area is the Physically Asynchronous Logically Synchronous (PALS) architecture. Rockwell Collins Inc has shown in their lab that using PALS, the verification time using model checking time for a dual redundant flight control system has reduced from 35 hours to less than 30 seconds, winning the 2009 David Lubkowski Memorial Award for the Advancement of Digital Avionics from American Institute of Aeronautics and Astronautics (AIAA). Running on top of PALS middleware, engineers can design, verify and run a networked (single-core) real-time control system as if it were a single computer at the fastest possible speed permitted by the platform.



## Selected Projects
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

