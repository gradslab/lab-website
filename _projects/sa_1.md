---
layout: page
title: Safe Hybrid Control with Barrier Functions
description: A hybrid framework for car-like robots that combines global convergence with guaranteed path invariance and obstacle avoidance, using control barrier functions.
img: assets/img/pics_and_gifs/fixed_v_sinusoidal_manifold.gif
importance: 1
category: safe-autonomy
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2502.07136">arXiv:2502.07136</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication</a>
</div>

For a car-like robot moving through an environment with obstacles, we interpret **safety as path
invariance**: once the robot converges to a feasible, obstacle-free path, it must **never leave it**.
Trajectory-tracking controllers cannot guarantee this — a fundamental performance limitation means the
robot may drift off the path and into obstacles.

We solve the problem in two stages. First, within a "tight" obstacle-free neighborhood of the path, a
**local controller** ensures both convergence and path invariance, with a **control barrier function (CBF)**
steering the system away from the singular configurations where the local law is undefined. Second, a
**hybrid control framework** stitches this local path-invariant controller together with *any* off-the-shelf
global tracking controller — inheriting global convergence from the latter and path-invariance + robustness
from the former.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/fixed_v_sinusoidal_manifold-800.webp' | relative_url }}" alt="A trajectory converging to and remaining on a curved path-following manifold" loading="lazy">
  <p class="media-caption">Once the state reaches the path-following manifold it remains invariant — the geometric essence of "safety as path invariance."</p>
</div>

**Guarantees**

- Global convergence from *any* initial position to the desired path.
- Forward **path invariance** — the robot provably never leaves the path after reaching it.
- **Robustness to sensor noise**, with the CBF avoiding singular configurations along the way.

*A Safe Hybrid Control Framework for Car-like Robot with Guaranteed Global Path-Invariance using a Control Barrier Function* — Nan Wang, Adeel Akhtar, Ricardo G. Sanfelice.
