---
layout: page
title: Research & Publications
permalink: /research/
description: Research and publications by Megan Morrison on data-driven dynamical systems, Koopman eigenfunctions, C. elegans neural dynamics, and signed networks.
lede: >-
  I build and analyze dynamical systems models, often from data, to understand how networks of
  interacting parts produce collective behavior.

# Each theme lists the papers in _data/publications.yml whose "theme" matches its key.
themes:
  - key: neural
    title: Neural dynamics and behavior
    intro: >-
      The nematode *C.&nbsp;elegans* has a fully mapped connectome and can be imaged neuron by neuron,
      which makes it a test bed for connecting network structure to behavior. I build models,
      constrained by the connectome and fit to whole-brain imaging, of how neural activity switches
      the worm between behavioral states such as forward and reverse locomotion. Current work uses
      community detection and dimensionality reduction to find low-dimensional descriptions of
      these dynamics, and calibrated matching methods to identify neurons in whole-brain recordings.
      Earlier work studied memory retrieval in damaged Hopfield networks.
  - key: koopman
    title: Koopman eigenfunctions and exact solutions of nonlinear ODEs
    intro: >-
      Koopman eigenfunctions turn a nonlinear system into a linear one in new coordinates. When
      those eigenfunctions can be found exactly, so can the solution of the ODE. I construct
      eigenfunctions from invariant manifolds, and in collaboration with Sonja Petrović, I study
      which polynomial ODEs have rational eigenfunctions and hence closed-form solutions.
  - key: datadriven
    title: Data-driven modeling, model selection, and control
    intro: >-
      Methods such as SINDy discover governing equations from data, but in biology data are often
      scarce while the library of candidate models is large. My group studies when the correct model
      can be identified in this regime, and how to choose sampling strategies that give the most
      information for model selection. Earlier work used discovered models to design control signals.
  - key: networks
    title: Signed networks, cooperation, and conflict
    intro: >-
      In signed networks, ties can be friendly or hostile. With Michael Gabbay and Nathan Kutz I
      studied structural balance dynamics on these networks: when communities can be detected, which
      factions emerge, and how a network of states can tip abruptly from peace into systemic war.
---

<p class="note">Papers are grouped by topic below. For a full list, see <a href="{{ site.links.scholar }}">Google Scholar</a> or my <a href="{{ site.links.cv | relative_url }}">CV</a>. Code for most papers is on <a href="{{ site.links.github }}">GitHub</a>.</p>

<nav class="theme-index" aria-label="Research themes">
  {% for theme in page.themes %}<a href="#{{ theme.key }}">{{ theme.title }}</a>{% endfor %}
</nav>

{% for theme in page.themes %}
<section class="theme" id="{{ theme.key }}">
  <h2>{{ theme.title }}</h2>
  <div class="theme-intro">{{ theme.intro | markdownify }}</div>
  {% assign papers = site.data.publications | where: "theme", theme.key %}
  {% for pub in papers %}{% include publication.html pub=pub %}{% endfor %}
</section>
{% endfor %}

<h2>Funding</h2>
<ul>
  <li>NSF REU Site: Summer Undergraduate Research Experience (SURE) at Illinois Tech, Award #2548498, 2026–2029 (Co-PI; PI Yuhan Ding)</li>
  <li>NSF Mathematical Sciences Postdoctoral Research Fellowship, Award #2103239, 2021–2025</li>
</ul>
