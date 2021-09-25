---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph,D Candidate in Computer Science, The University of Queensland, Australia, 2019 - current.
* Master of Information Technology, The University of Queensland, Australia, 2017 - 2018.
* Bachelor of Electrical Engineering, China, Chongqing University of Science and Technology University, 2012 - 2016.
  

Publications
======

{%- assign publications = site.publications | sort:"year" | reverse | group_by:"year" -%}
{% for year in publications %}
  {%- for post in year.items -%}
    {% include archive-single.html %}
  {%- endfor -%}
{% endfor %}

<!--   <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->
  
<!-- 
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
-->

Awards
======
* [ICTIR 2021](https://ictir2021.org/awards/)[ Best Student Paper Award {% <i class="fa fa-trophy" aria-hidden="true"></i> %}]
* [2021 DIGIX GLOBAL AI CHALLENGE](https://developer.huawei.com/consumer/en/activity/digixActivity/digixdetail/201621219634131423): 
Search rankings in multimodal and multilingual contexts. [Champion {% <span role="image" aria-label="🥇" style="font-family:&quot;Apple Color Emoji&quot;,&quot;Segoe UI Emoji&quot;,NotoColorEmoji,&quot;Noto Color Emoji&quot;,&quot;Segoe UI Symbol&quot;,&quot;Android Emoji&quot;,EmojiSymbols;line-height:1em;font-size:1em">🥇</span> %}]

Teaching
======
<!-- 
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
-->
* The University of Queensland
  * Tutor
  * Tutoring of the INFS7410 (Information Retrieval and Web Search) course. Preparing and delivering course materials, assignments and exams marking.
  * Aug 2018 - Current


Work experience
======
* Casual Research Assistant
  * The University of Queensland
  * Assist with the research and development of methods of information retrieval and evaluation based on online learning to rank.
  * Apr 2019 - July 2019

  
Service
======
* PC member: SIGIR2021, ADCS20201
* Publicity Chair of [CIKM2021](http://www.cikm2021.org/committee)
