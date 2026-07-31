---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a postdoc in [Institute of Information Science, Academia Sinica](https://www.iis.sinica.edu.tw/).  
Until September 2021, I was a postdoc in [Chair of Security Engineering, Ruhr University Bochum](https://informatik.rub.de/en/security-engineering/).  
Until September 2019, I was a postdoc in [Research Center for Information Technology Innovation, Academia Sinica](https://www.citi.sinica.edu.tw/).  
Before that, I was a research assistant in [Institute of Information Science, Academia Sinica](https://www.iis.sinica.edu.tw/) and a PhD student in [Graduate Institute of Electrical Engineering, National Taiwan University](https://graduate.ee.ntu.edu.tw/).  

## Education

* Ph.D in Electrical Engineering, National Taiwan University, 2018
  * Thesis: Multiplication in Binary Fields on Modern Computers and its Applications. [[pdf]](https://devillegna.github.io/files/thesis.pdf)
  * Advisor: [Dr. Chen-Mou Cheng](https://scholar.google.com/citations?user=WKmNG2sAAAAJ&hl=en).
* M.S. in Computer Science and Information Engineering, National Taiwan University, 2003
* B.S. in Physics, National Taiwan University, 2001


## Publications

{% assign publications_by_year = site.publications | sort: 'date' | reverse | group_by_exp: "publication", "publication.date | date: '%Y'" %}
{% for year in publications_by_year %}
  <h3 class="archive__subtitle">{{ year.name }}</h3>
  <ul>{% for post in year.items %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endfor %}


## Software Projects

  <ul>{% for post in site.projects reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

