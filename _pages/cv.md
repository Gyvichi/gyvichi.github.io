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
    <dt><strong>Chungbuk Science High School</strong> &nbsp; <span style="float:right;">2023 – 2025</span></dt>
    <dd>Specialized curriculum in mathematics and physical sciences. Ranked top 5% of class.</dd>
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
    <li><strong>Genius Olympiad 2024 Qualifier</strong> – Artificial Intelligence Track</li>
    <li><strong>Talent Award of Korea</strong> – National recognition for scientific potential (2025)</li>
  </ul>
</section>

<section id="skills">
  <h2>Skills</h2>
  <ul>
    <li><strong>Programming:</strong> Python, C++, JavaScript, HTML/CSS</li>
    <li><strong>Tools & Libraries:</strong> PyTorch, TensorFlow, Scikit-learn, OpenCV</li>
    <li><strong>Languages:</strong> Korean (native), English (fluent), Japanese (intermediate)</li>
  </ul>
</section>

<section id="projects">
  <h2>Selected Projects</h2>
  <ul>
    <li><strong>Astrophysics Simulation Toolkit</strong> – Developed a real-time orbital mechanics simulator using RK4 and Python.</li>
    <li><strong>Battery SOH Estimation using EIS</strong> – Designed a PCB system to measure SOH using frequency response; finalist in national science fair.</li>
  </ul>
</section>

<section id="extracurricular">
  <h2>Extracurricular Activities</h2>
  <ul>
    <li><strong>Student Research Society</strong> – President; organized national-level AI research workshops.</li>
    <li><strong>Debate Club</strong> – Captain; won regional championship 2024.</li>
  </ul>
</section>
