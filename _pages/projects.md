---
layout: page
title: projects
permalink: /projects/
description: Projects organized by research area.
nav: true
nav_order: 1
horizontal: false
---

<!-- _pages/projects.md — projects grouped by the lab's three research areas.
     Each section has an `id` so the homepage cards can deep-link to it
     (e.g. /projects/#geometric-control). Projects live in _projects/ and are
     filtered by their `category` (geometric-control | safe-autonomy | learning-dynamics). -->

<div class="projects">

<!-- ===================== Geometric Control & Estimation ===================== -->
<h2 id="geometric-control" class="research-section-title">Geometric &amp; Hybrid Control</h2>
<p class="research-section-intro">Geometric and hybrid controllers for robots and drones on manifolds and Lie groups.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign gc = site.projects | where: "category", "geometric-control" | sort: "importance" %}
  {% for project in gc %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Safe & Reliable Autonomy ===================== -->
<h2 id="safe-autonomy" class="research-section-title">Safe &amp; Reliable Autonomy</h2>
<p class="research-section-intro">Control barrier functions, feedback linearization, and decentralized coordination for dependable autonomy.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign sa = site.projects | where: "category", "safe-autonomy" | sort: "importance" %}
  {% for project in sa %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Learning & Dynamical Systems ===================== -->
<h2 id="learning-dynamics" class="research-section-title">Stochastic &amp; Learning Dynamics</h2>
<p class="research-section-intro">Geometric control of stochastic dynamical systems and learning-based methods for control.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign ld = site.projects | where: "category", "learning-dynamics" | sort: "importance" %}
  {% for project in ld %}
    {% include projects.liquid %}
  {% endfor %}
</div>

</div>
