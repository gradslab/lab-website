---
layout: page
title: Research
permalink: /projects/
description: The GRaDS Lab research landscape — geometric control, safe autonomy, and stochastic control & learning on Lie groups.
nav: true
nav_order: 1
horizontal: false
---

<!-- _pages/projects.md — projects grouped by the lab's three research thrusts.
     Each section has an `id` so the homepage cards can deep-link to it
     (e.g. /projects/#geometric-control). Projects live in _projects/ and are
     filtered by their `category` (geometric-control | safe-autonomy | learning-dynamics). -->

<p class="research-lede">
The GRaDS Lab studies how the <strong>geometry</strong> of a dynamical system can be turned into
better control. A rotating body, a wheeled robot, a quadrotor — each lives on a curved state space,
and respecting that structure yields controllers that are simpler, provably correct, and robust.
Our work spans three connected thrusts, from deterministic path following to safety guarantees to
stochastic control and learning on Lie groups.
</p>

<div class="projects">

<!-- ===================== Geometric Path Following & Feedback Linearization ===================== -->
<h2 id="geometric-control" class="research-section-title">Geometric Path Following &amp; Feedback Linearization</h2>
<p class="research-section-intro">
Make a robot converge to — and stay on — a geometric <em>path</em>, rather than chase a clock.
We exploit the geometry of a system's motion through <strong>transverse feedback linearization</strong>
and <strong>quadratic-program</strong> reformulations that eliminate the singularities of classical
designs, with demonstrations on unicycle robots, quadrotors, and aircraft.
</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign gc = site.projects | where: "category", "geometric-control" | sort: "importance" %}
  {% for project in gc %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Safe & Resilient Autonomy ===================== -->
<h2 id="safe-autonomy" class="research-section-title">Safe &amp; Resilient Autonomy</h2>
<p class="research-section-intro">
Convergence is not enough: a safe system must <em>never leave</em> its path once it reaches it — even
amid obstacles, sensor noise, or adversarial cyber-attacks. We build <strong>control-barrier-function</strong>
and <strong>hybrid</strong> controllers that certify forward <strong>path invariance</strong> and robustness
for car-like robots and quadrotors.
</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign sa = site.projects | where: "category", "safe-autonomy" | sort: "importance" %}
  {% for project in sa %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- ===================== Geometric Stochastic Control & Learning on Lie Groups ===================== -->
<h2 id="learning-dynamics" class="research-section-title">Geometric Stochastic Control &amp; Learning on Lie Groups</h2>
<p class="research-section-intro">
Real robots evolve on curved state spaces — rotation groups like <em>SO(2)</em> and <em>SO(3)</em> — where
Euclidean tools break down. We develop coordinate-free methods to steer probability densities
(<strong>Schrödinger bridges</strong>) and to learn certificates of stability (<strong>neural Lyapunov
functions</strong>) directly on Lie groups.
</p>
<div class="row row-cols-1 row-cols-md-3">
  {% assign ld = site.projects | where: "category", "learning-dynamics" | sort: "importance" %}
  {% for project in ld %}
    {% include projects.liquid %}
  {% endfor %}
</div>

</div>
