---
layout: page
title: Singularity-Free Tracking of Unicycle Robots
description: A relaxed quadratic-program reformulation of dynamic feedback linearization that stays well-defined even at zero velocity — enabling stop-and-reverse maneuvers.
img: assets/img/pics_and_gifs/dfl_qp_tracking.gif
importance: 2
category: geometric-control
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2606.23355">arXiv:2606.23355</a>
  <a class="btn-link" href="https://gradslab.github.io/DFL_QP_Unicycle/">Code &amp; project page</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication (CCTA 2026)</a>
</div>

**Dynamic feedback linearization (DFL)** is a classical way to make a unicycle-type robot track a
trajectory — but the standard DFL controller becomes **singular when the linear velocity vanishes**. That
makes it unusable for exactly the maneuvers robots need most: stopping, reversing, and tight turns.

We reformulate the DFL constraints as an **equality-constrained quadratic program (QP)** with a slack
variable. The QP is feasible for *all* states and references — including where the robot's velocity is
zero — and we prove the resulting feedback law is **locally Lipschitz continuous**. Tunable parameters let
the controller steer around the singular configuration for a large class of reference trajectories.

<div class="media-duo">
  <figure>
    <img src="{{ '/assets/img/pics_and_gifs/standard_dfl_tracking-800.webp' | relative_url }}" alt="Standard DFL controller stalling near zero velocity" loading="lazy">
    <figcaption class="media-caption">Standard DFL — the control law degrades near the zero-velocity singularity.</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/img/pics_and_gifs/dfl_qp_tracking-800.webp' | relative_url }}" alt="Proposed QP-based controller tracking smoothly through stop-and-reverse" loading="lazy">
    <figcaption class="media-caption">Proposed QP framework — smooth, singularity-free tracking on a TurtleBot3 Waffle.</figcaption>
  </figure>
</div>

**Highlights**

- Guarantees feasibility and local Lipschitz continuity of the feedback everywhere, including at zero velocity.
- Enables **stop-and-reverse** maneuvers that classical DFL cannot handle.
- Validated in **ROS 2 / Gazebo** on a TurtleBot3 Waffle robot.

*A Relaxed Quadratic-Program-based Framework for Trajectory Tracking of Unicycle Robots with Singularity Avoidance* — Hamza Tariq, Usman Ali, Adeel Akhtar (IEEE CCTA 2026).
