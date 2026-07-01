---
layout: page
title: Path Following for Quadrotors
description: Quasi-static transverse feedback linearization (QSTFL) that makes a quadrotor follow a geometric path with no extra controller states.
img: assets/img/pics_and_gifs/conv.gif
importance: 1
category: geometric-control
github: https://gitlab.com/a5akhtar/quasistatic-tfl-uav/
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2606.23218">arXiv:2606.23218</a>
  <a class="btn-link" href="https://gitlab.com/a5akhtar/quasistatic-tfl-uav/">Code &amp; animations</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication</a>
</div>

For a vehicle moving along a prescribed curve, a time-parameterized reference is the wrong tool: if the
quadrotor slows down or stops, the reference keeps evolving and an artificial tracking error appears.
**Path following** removes time from the reference and instead asks the vehicle to converge to, and stay on,
a geometric path — regulating its speed *along* the curve independently.

We propose a **quasi-static transverse feedback linearization (QSTFL)** controller for a quadrotor. Unlike
dynamic-feedback designs, it introduces **no additional controller states**: the thrust is computed
algebraically from the current state, so there is no need to measure thrust derivatives or numerically
integrate an extended system.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/conv-800.webp' | relative_url }}" alt="Quadrotor converging to and following a circular path" loading="lazy">
  <p class="media-caption">A quadrotor converging to a circular path and remaining on it — the path-following manifold is rendered invariant.</p>
</div>

**What the design guarantees**

- The path-following manifold is made **invariant**: trajectories that start on the path stay on it for all future time.
- **Local exponential stability** of the manifold is proved via a diffeomorphic coordinate transformation, while tangential velocity and yaw are regulated simultaneously.
- Closed-form thrust and torque inputs; the decoupling matrix to invert is only **3×3 instead of 4×4**, giving a simpler, cheaper control law than dynamic-feedback constructions.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/traj_3d_circle-800.webp' | relative_url }}" alt="Several quadrotors following circular paths in 3D" loading="lazy">
  <p class="media-caption">Multiple quadrotors following 3D circular paths under the QSTFL controller.</p>
</div>

*Path-following Control of a Quadrotor using Quasi-Static Transverse Feedback Linearization* — Mohamed Al Lawati, Adeel Akhtar.
