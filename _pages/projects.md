---
layout: page
title: Projects
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
<h2 id="geometric-control" class="research-section-title">Geometric &amp; Nonlinear Control</h2>
<p class="research-section-intro">Controllers built on the geometry of motion — feedback linearization, transverse feedback linearization, and control on Lie groups and manifolds.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign gc = site.projects | where: "category", "geometric-control" | sort: "importance" %}
  {% for project in gc %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Safe & Reliable Autonomy ===================== -->
<h2 id="safe-autonomy" class="research-section-title">Safe &amp; Path-Invariant Autonomy</h2>
<p class="research-section-intro">Safety-critical and path-invariant control — control barrier functions, hybrid control, and robustness to disturbances and cyber attacks.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign sa = site.projects | where: "category", "safe-autonomy" | sort: "importance" %}
  {% for project in sa %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Learning & Dynamical Systems ===================== -->
<h2 id="learning-dynamics" class="research-section-title">Stochastic &amp; Learning-Based Control</h2>
<p class="research-section-intro">Stochastic optimal control and learning for control — Schrödinger bridges on Lie groups and learning Lyapunov certificates for stability.</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign ld = site.projects | where: "category", "learning-dynamics" | sort: "importance" %}
  {% for project in ld %}
    {% include projects.liquid %}
  {% endfor %}
</div>

</div>
