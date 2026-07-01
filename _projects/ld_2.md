---
layout: page
title: Schrödinger Bridges over Compact Lie Groups
description: Generalizing coordinate-free density steering from SO(2) to any compact connected Lie group, with numerical examples on SO(2) and SO(3).
img: assets/img/pics_and_gifs/sbp_lie_density.jpg
importance: 2
category: learning-dynamics
github: https://github.com/gradslab/SbpLieGroups
---

<div class="project-meta">
  <a class="btn-link" href="https://arxiv.org/abs/2603.14049">arXiv:2603.14049</a>
  <a class="btn-link" href="https://github.com/gradslab/SbpLieGroups">Code &amp; animations</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication (L-CSS)</a>
</div>

This work lifts our SO(2) result to its natural level of generality: the **Schrödinger bridge problem on
any compact connected Lie group**. The goal is the same — steer a controlled diffusion between given initial
and terminal densities supported on the group while minimizing control effort — but the formulation is fully
**coordinate-free**, respecting the group's geometry and avoiding local parameterizations or Euclidean
embeddings.

Working in the Banach space of continuous functions on the group and using **Hilbert's projective metric**,
we prove existence and uniqueness of the solution to the corresponding Schrödinger system, and the result is
**constructive**: it yields the geometric controller that optimally interpolates the densities. This
geometric perspective matters for groups like **SO(3)**, which appear throughout attitude control, DNA
statistical mechanics, flexible-needle steering, and mobile robotics.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/sbp_lie_density.jpg' | relative_url }}" alt="Optimal probability densities interpolated over a Lie group" loading="lazy">
  <p class="media-caption">Optimally interpolated densities steered over the group — illustrated on the rotation groups SO(2) and SO(3).</p>
</div>

**Contributions**

- A coordinate-free formulation of the SBP for **any compact connected Lie group**.
- Existence–uniqueness of the Schrödinger system solution via a contraction in Hilbert's projective metric.
- A constructive **geometric controller**, with numerical examples on **SO(2)** and **SO(3)**.

*Schrödinger Bridge Over a Compact Connected Lie Group* — Hamza Mahmood, Abhishek Halder, Adeel Akhtar (IEEE Control Systems Letters).
