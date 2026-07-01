---
layout: page
title: Path Invariance under Cyber-Attacks
description: A transverse-feedback-linearization controller that keeps a quadrotor on its path with provable forward invariance, even when an adversary hijacks a rotor.
img: assets/img/pics_and_gifs/quadrotor_cyber_path.jpg
importance: 2
category: safe-autonomy
video: https://youtu.be/orp1g-pIFrM
---

<div class="project-meta">
  <a class="btn-link" href="https://youtu.be/orp1g-pIFrM">Video</a>
  <a class="btn-link" href="{{ '/publications/' | relative_url }}">Publication (ACC 2025)</a>
</div>

What happens to a quadrotor's mission when an attacker takes over one of its rotors? This project designs
a **path-following controller that guarantees safe maneuvers — in the sense of forward path invariance —
in the presence of cyber-physical attacks.**

We model an adversary that can drive any single rotor through a **false-data-injection (FDI)** attack. Using
**transverse feedback linearization**, we build a controller with a **closed-form analytical expression**
that is cheap to compute, mitigates the bounded malicious signal, and provably keeps the quadrotor on a
class of smooth curves — ensuring mission success despite the attack.

<div class="project-media">
  <img src="{{ '/assets/img/pics_and_gifs/quadrotor_cyber_path.jpg' | relative_url }}" alt="Quadrotor following the desired path despite an adversarial rotor attack" loading="lazy">
  <p class="media-caption">The quadrotor (drone snapshots) tracks the desired path (green) via the traversed trajectory (red) even while one rotor is under attack.</p>
</div>

**Contributions**

- Provable **forward path invariance** under bounded FDI attacks, with realistic assumptions.
- A **computationally efficient, closed-form** controller — no online optimization required.
- The controller also enforces a desired **speed profile** along the path during the attack.

*Path Invariance of a Quadrotor System under Cyber Attacks with Theoretical Guarantees* — Hamza Mahmood, Usman Ali, Adeel Akhtar (American Control Conference 2025).
