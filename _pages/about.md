---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
lang: en
name: about
redirect_from: 
  - /about/
  - /about.html
  - /_pages/about/
---
My name is Philippe Laporte. I am a Ph.D. student at the University of Montréal (Canada).<br>
I currently do research in Nuclear Medicine, 
where I try to improve segmentation techniques for dynamical PET images in a preclinical context.<br><br>
Starting to work with polyglot v.37<br><br>

{% for lang in site.languages %}
    {% if lang == site.default_lang %}
[{{lang}} (Default)]({{lang}}{{page.url}})
    {% else %}
[{{lang}}](/{{site.website_name}}/{{lang}}{{page.url}})
    {% endif %}
{% endfor %}