---
layout: about
title: Home
permalink: /
subtitle: Geometry, Robotics, and Dynamical Systems (GRaDS) Lab — Department of Mechanical and Industrial Engineering, New Jersey Institute of Technology.

# Homepage sections from the default al-folio `about` layout are disabled so the
# page shows only the custom hero + carousel + research cards below.
selected_papers: false
social: true # shows the social icons (GitHub, YouTube, …) at the bottom of the homepage

# Latest news is rendered in the page body below (with a capitalized "News" heading),
# so the layout's own lowercase news section is disabled here. limit/scrollable are
# still read by the news include below.
announcements:
  enabled: false
  scrollable: true # adds a scroll bar if there are more than 3 news items
  limit: 5 # number of news items to show on the homepage

latest_posts:
  enabled: false
---

<!-- ===================== HERO ===================== -->
<div class="grads-hero">
  <p class="lead">
    The GRaDS Lab develops the geometric, nonlinear, and hybrid control foundations of
    intelligent robots — with applications to mobile and aerial robotics, drones, and
    safety-critical autonomous systems operating reliably in the real world.
  </p>
</div>

<!-- ===================== IMAGE CAROUSEL ===================== -->
<!-- Placeholder lab/robot photos. Swap the files in assets/img/ (or change the
     paths below) for your own images. -->
<div class="grads-carousel" id="grads-carousel">
  <div class="slide active"><img src="{{ '/assets/img/1.jpg' | relative_url }}" alt="Lab photo 1 (placeholder)"></div>
  <div class="slide"><img src="{{ '/assets/img/7.jpg' | relative_url }}" alt="Lab photo 2 (placeholder)"></div>
  <div class="slide"><img src="{{ '/assets/img/9.jpg' | relative_url }}" alt="Lab photo 3 (placeholder)"></div>
  <div class="dots" aria-hidden="true"></div>
</div>

<!-- ===================== RESEARCH AREAS ===================== -->
<h2>Research</h2>
<div class="research-cards">
  <a class="research-card" href="{{ '/projects/#geometric-control' | relative_url }}">
    <img src="{{ '/assets/img/pics_and_gifs/conv-800.webp' | relative_url }}" alt="Quadrotor following a geometric path" loading="lazy">
    <div class="body">
      <h3>Geometric Path Following &amp; Feedback Linearization</h3>
      <p>Making robots converge to and stay on a geometric path — via transverse feedback
      linearization and singularity-free quadratic-program designs for unicycles, quadrotors, and aircraft.</p>
    </div>
  </a>
  <a class="research-card" href="{{ '/projects/#safe-autonomy' | relative_url }}">
    <img src="{{ '/assets/img/pics_and_gifs/fixed_v_sinusoidal_manifold-800.webp' | relative_url }}" alt="A trajectory staying invariant on a path-following manifold" loading="lazy">
    <div class="body">
      <h3>Safe &amp; Resilient Autonomy</h3>
      <p>Guaranteeing a system never leaves its path once reached — control barrier functions and
      hybrid control for forward path invariance under obstacles, noise, and cyber-attacks.</p>
    </div>
  </a>
  <a class="research-card" href="{{ '/projects/#learning-dynamics' | relative_url }}">
    <img src="{{ '/assets/img/pics_and_gifs/anm1-800.webp' | relative_url }}" alt="Probability density steered on the circle SO(2)" loading="lazy">
    <div class="body">
      <h3>Geometric Stochastic Control &amp; Learning on Lie Groups</h3>
      <p>Coordinate-free density steering (Schrödinger bridges) and learned neural Lyapunov
      certificates directly on rotation groups like SO(2) and SO(3).</p>
    </div>
  </a>
</div>

<!-- ===================== LATEST NEWS ===================== -->
<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">News</a></h2>
{% include news.liquid limit=true %}

<script>
  (function () {
    var root = document.getElementById("grads-carousel");
    if (!root) return;
    var slides = Array.prototype.slice.call(root.querySelectorAll(".slide"));
    var dotbar = root.querySelector(".dots");
    var i = 0;

    slides.forEach(function (_, idx) {
      var b = document.createElement("button");
      b.setAttribute("aria-label", "Show slide " + (idx + 1));
      if (idx === 0) b.classList.add("active");
      b.addEventListener("click", function () { show(idx); });
      dotbar.appendChild(b);
    });
    var dots = Array.prototype.slice.call(dotbar.querySelectorAll("button"));

    function show(n) {
      slides[i].classList.remove("active");
      dots[i].classList.remove("active");
      i = (n + slides.length) % slides.length;
      slides[i].classList.add("active");
      dots[i].classList.add("active");
    }
    setInterval(function () { show(i + 1); }, 4500);
  })();
</script>
