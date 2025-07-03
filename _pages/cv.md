---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<section id="education">
  <h2>Education</h2>
  <dl>
    <dt><strong>KAIST</strong> &nbsp; <span stype="float:right;">2025-2029 (expected)</span></dt>
    <dd> Undergraduate, Dept. of Semiconductor System Engineering</dd>
  <dl>
    <dt><strong>Chungbuk Science High School</strong> &nbsp; <span style="float:right;">2023 – 2025</span></dt>
  </dl>
</section>

<section id="publications">
  <h2>Publications</h2>
  <ul>
    {% for post in site.publications reversed %}
      {% include archive-single-cv.html %}
    {% endfor %}
  </ul>
</section>

<section id="achievements">
  <h2>Awards & Honors</h2>
  <ul>
    <li><strong>Regeneron ISEF 2024 Finalist</strong> – Physics & Astronomy Category (Los Angeles, USA)</li>
    <li><strong>Qualified to Genius Olympiad 2025</strong> – Artificial Intelligence Category</li>
    <li><strong>2025 Talent Award of Korea</strong></li>
  </ul>
</section>

<section id="skills">
  <h2>Skills</h2>
  <ul>
    <li><strong>Programming:</strong> Python, C++, Java</li>
    <li><strong>Tools & Libraries:</strong> PyTorch, CUDA</li>
    <li><strong>Languages:</strong> Korean (native), English (fluent)</li>
  </ul>
</section>

<section id="projects">
  <h2>Selected Projects</h2>
  <ul>
    <li><strong>Astrophysics Simulation Toolkit</strong> – Developed a real-time orbital mechanics simulator using RK4 and Python.</li>
    <li><strong>Battery SOH Estimation using EIS</strong> – Designed a PCB system to measure SOH using frequency response; finalist in national science fair.</li>
  </ul>
</section>
