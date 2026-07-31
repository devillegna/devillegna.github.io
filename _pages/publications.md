---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% comment %}
  Sort newest-first, then bucket by year. group_by_exp preserves the incoming
  order, so years come out descending and papers stay ordered within each year.
{% endcomment %}
{% assign publications_by_year = site.publications | sort: 'date' | reverse | group_by_exp: "publication", "publication.date | date: '%Y'" %}

{% for year in publications_by_year %}
  <h2 class="archive__subtitle">{{ year.name }}</h2>
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
