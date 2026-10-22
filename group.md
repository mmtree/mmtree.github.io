---
layout: page
title: Group
permalink: /group/
description: Students advised by Megan Morrison in the Department of Applied Mathematics at Illinois Tech.
---

## Current students

{% for s in site.data.students.current %}
<div class="person">
  <h3>{{ s.name }}</h3>
  <p class="meta">{{ s.level }}, since {{ s.since }}</p>
  <p>{{ s.project }}</p>
</div>
{% endfor %}

{% if site.data.students.alumni.size > 0 %}
## Former students

{% for s in site.data.students.alumni %}
<div class="person">
  <h3>{{ s.name }}</h3>
  <p class="meta">{{ s.level }}, {{ s.when }}</p>
  <p>{{ s.project }}</p>
</div>
{% endfor %}
{% endif %}

## Prospective students

Illinois Tech students interested in dynamical systems, data-driven modeling, or mathematical
neuroscience are welcome to email me. Undergraduates can also apply to the
NSF-funded [SURE summer research program at Illinois Tech](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2548498).
