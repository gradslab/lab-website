---
layout: page
title: Learning Neural Lyapunov Functions on SO(n)
description: A physics-informed neural framework that learns maximal Lyapunov functions — and estimates regions of attraction — for dynamical systems evolving on the rotation group SO(n).
img: assets/img/pics_and_gifs/learned_lyapunov_roa.jpg
importance: 3
category: learning-dynamics
github: https://github.com/mBarreau/LyapunovSO
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2606.19669">arXiv:2606.19669</a>
  <a class="btn-link" href="https://github.com/mBarreau/LyapunovSO">Code</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication (L-CSS)</a>
</div>

Proving stability for systems on **Lie groups** is hard: the classical Lyapunov machinery built for
Euclidean space does not transfer to curved geometries. This project learns **maximal Lyapunov functions**
for systems evolving on the special orthogonal group **SO(n)** — certificates that both prove stability and
estimate the largest possible **region of attraction**.

We introduce a **neural Lyapunov architecture based on the logarithmic map**, with proven approximation
capabilities, and cast learning as a **Zubov-type** characterization of the maximal region of attraction. A
central technical contribution is an explicit, numerically tractable formula for the **derivative of the
logarithmic map**, which enables a two-phase training algorithm that trades off computational cost against
accuracy.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/learned_lyapunov_roa.jpg' | relative_url }}" alt="A learned Lyapunov function with its estimated region of attraction and spiraling trajectories" loading="lazy">
  <p class="media-caption">A learned Lyapunov function <em>V(α, ω)</em>: the black contour is the estimated region of attraction; white curves are trajectories spiraling into the stable equilibrium.</p>
</div>

**Contributions**

- A neural Lyapunov architecture on SO(n) built from the **logarithmic map**, with approximation guarantees.
- Explicit, tractable formulas for the **derivative of the log map** that make training feasible.
- A **two-phase learning algorithm** validated on an interpretable low-dimensional nonlinear system, recovering a large region of attraction.

*Learning Neural Maximal Lyapunov Functions on SO(n)* — Adeel Akhtar, Matthieu Barreau (IEEE Control Systems Letters).
