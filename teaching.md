---
layout: page
title: Teaching
permalink: /teaching/
description: Courses taught by Megan Morrison at Illinois Institute of Technology and New York University.
---

{% for school in site.data.teaching %}
## {{ school.institution }}

<table class="courses">
  <tbody>
  {% for c in school.courses %}
    <tr><td class="code">{{ c.code }}</td><td>{{ c.name }}</td><td class="terms">{{ c.terms }}</td></tr>
  {% endfor %}
  </tbody>
</table>
{% endfor %}

## Course development

- **MATH 439/539: Network Modeling and Statistics** (Spring 2026). A new cross-listed
  undergraduate and graduate course.
- **Ordinary Differential Equations and Data-Driven Methods for Dynamical Systems** (in development).
  A redesign of MATH 488/515 that adds numerical methods, model selection, reduced-order modeling,
  DMD and Koopman analysis, control, and machine learning for dynamical systems.
