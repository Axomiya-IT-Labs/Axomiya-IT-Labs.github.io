---
layout: default
title: Our Team
permalink: /team/
---

<div class="hero-section">
  <span class="hero-badge">Meet the Builders</span>
  <h1 class="hero-title">Meet the Builders & Problem Solvers</h1>
  <p class="hero-subtitle">The people who design, code, research, and organize behind Axomiya IT Labs.</p>
</div>

<section class="team-page-content container">
  {% if site.data.team.leadership.size > 0 %}
  <div class="text-center">
    <h2 class="section-title">Leadership</h2>
  </div>
  {% include sections/team-grid.html team=site.data.team.leadership %}
  {% endif %}

  {% if site.data.team.developers.size > 0 %}
  <div class="text-center" style="margin-top: 3rem;">
    <h2 class="section-title">Developers</h2>
  </div>
  {% include sections/team-grid.html team=site.data.team.developers %}
  {% endif %}

  {% if site.data.team.designers.size > 0 %}
  <div class="text-center" style="margin-top: 3rem;">
    <h2 class="section-title">Designers</h2>
  </div>
  {% include sections/team-grid.html team=site.data.team.designers %}
  {% endif %}

  {% if site.data.team.advisors.size > 0 %}
  <div class="text-center" style="margin-top: 3rem;">
    <h2 class="section-title">Advisors</h2>
  </div>
  {% include sections/team-grid.html team=site.data.team.advisors %}
  {% endif %}
</section>

<section class="container">
  <div class="guidelines-box text-center">
    <h3>Join the Team</h3>
    <p>We are always looking for passionate open-source contributors, developers, and educators. If you want to help build Assam's first AI & open-source community, reach out on GitHub or Telegram.</p>
    <div class="hero-buttons" style="justify-content: center; margin-top: 1rem;">
      <a href="https://github.com/Axomiya-IT-Labs" target="_blank" rel="noopener noreferrer" class="btn btn-primary">Become a Contributor</a>
      <a href="https://t.me/AxomiyaITLabs" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">Chat on Telegram</a>
    </div>
  </div>
</section>
