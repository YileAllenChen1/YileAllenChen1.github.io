---
permalink: /
title: "About Me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Howdy! I am a senior computer engineering student at Texas A&M University, advised by Dr. [Xia (Ben) Hu](https://cs.rice.edu/~xh37/). In Fall 2021, I interned at Nvidia on the Drive IX team working on synthetic data generation and vehicle user authentication pipeline. I also interned at Arm in Summer 2021 working on a front end web app. My interest lies in computer vision, autonomous driving and robotics.

My hobbies include running, working out, playing the guitar, and photography.


<h1> Publications </h1>

{% include base_path %}

{% assign cur_year = "9999" %}
{% for post in site.publications reversed %}
  {% assign dates = post.date | split: "-" %}
  {% assign year = dates.first %}
  {% if year != cur_year %}
    {% assign cur_year = year %}
<h2> {{ year }} </h2>
  {% endif %}
  {% include archive-single.html %}
{% endfor %}

<b> * Equal contribution </b>
