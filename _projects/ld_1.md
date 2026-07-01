---
layout: page
title: Schrödinger Bridges on SO(2)
description: A coordinate-free solution to the Schrödinger bridge problem on the circle — steering probability densities on SO(2) with minimum control effort.
img: assets/img/pics_and_gifs/anm1.gif
importance: 1
category: learning-dynamics
github: https://gitlab.com/a5akhtar/sbp
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2606.22690">arXiv:2606.22690</a>
  <a class="btn-link" href="https://gitlab.com/a5akhtar/sbp">Code &amp; animations</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication</a>
</div>

The **Schrödinger bridge problem (SBP)** asks for the controller that drives the entire *probability density*
of a stochastic system from a prescribed initial distribution to a prescribed terminal distribution over a
fixed time horizon, while spending the least control effort. It is *density* control: we steer the whole
population of states, not a single trajectory — with applications from robotic swarms to traffic densities.

Most existing SBP theory lives in Euclidean space. But most robots — drones, wheeled vehicles — have a
**Lie group** as their state space. Here we solve the isotropic SBP for the kinematic equation on
**SO(2)**, taking angular velocity as the control input.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/anm1-800.webp' | relative_url }}" alt="A probability density steered around the circle SO(2) over time" loading="lazy">
  <p class="media-caption">The optimal density evolving on SO(2): the initial distribution is transported to the target on the circle with minimum effort.</p>
</div>

**Key results**

- Existence and uniqueness of a solution to the **Schrödinger system on SO(2)**, proved by showing a fixed-point recursion is contractive in **Hilbert's projective metric**.
- A **geometric, coordinate-free** controller that uses the intrinsic structure of SO(2) — never embedding it in the Euclidean plane.
- Numerical simulations confirm the theoretical construction of the bridge.

*A Geometric Solution of the Schrödinger Bridge Problem on SO(2) via Stochastic Optimal Control* — Hamza Mahmood, Adeel Akhtar.
