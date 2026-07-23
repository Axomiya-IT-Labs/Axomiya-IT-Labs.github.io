---
layout: default
title: Projects
permalink: /projects/
---

<div class="hero-section">
  <span class="hero-badge">What We Build</span>
  <h1 class="hero-title">Things We Build to Solve Real Problems</h1>
  <p class="hero-subtitle">Open-source tools, AI experiments, and community platforms created to remove friction for learners and builders in Assam and beyond.</p>
</div>

<section class="container">
  <div class="text-center">
    <h2 class="section-title">Active Projects</h2>
    <p class="section-subtitle">Live, beta, and in-progress builds from the community.</p>
  </div>

  {% assign active_projects = site.projects | where_exp: "project", "project.status != 'Idea'" %}
  {% if active_projects.size > 0 %}
  <div class="listings-grid">
    {% for project in active_projects %}
    <article class="listing-card">
      {% if project.image %}
      <div class="listing-image">
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
        {% if project.status %}<span class="listing-badge">{{ project.status }}</span>{% endif %}
      </div>
      {% endif %}
      <div class="listing-content">
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        <p class="listing-meta">
          {% if project.category %}<span>{{ project.category }}</span>{% endif %}
          {% if project.tech_stack %}<span>• {{ project.tech_stack | join: ", " }}</span>{% endif %}
        </p>
        <p class="listing-excerpt">{{ project.excerpt | default: project.content | strip_html | truncate: 160 }}</p>
        {% if project.tags %}
        <div class="listing-tags">
          {% for tag in project.tags %}
          <span class="tag">#{{ tag }}</span>
          {% endfor %}
        </div>
        {% endif %}
        <a href="{{ project.url | relative_url }}" class="listing-read-more">View Project →</a>
      </div>
    </article>
    {% endfor %}
  </div>
  {% else %}
  <div class="card-item text-center" style="margin-top: 2rem;">
    <p class="lead">No active projects yet. We are building in public — check back soon or contribute an idea.</p>
  </div>
  {% endif %}
</section>

<section class="container">
  <div class="text-center">
    <h2 class="section-title">Ideas Bar</h2>
    <p class="section-subtitle">Open project ideas — build them with us.</p>
  </div>

  {% assign ideas = site.projects | where_exp: "project", "project.status == 'Idea'" %}
  {% if ideas.size > 0 %}
  <div class="listings-grid">
    {% for project in ideas %}
    <article class="listing-card">
      {% if project.image %}
      <div class="listing-image">
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
        <span class="listing-badge">{{ project.status }}</span>
      </div>
      {% endif %}
      <div class="listing-content">
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        <p class="listing-meta">
          {% if project.category %}<span>{{ project.category }}</span>{% endif %}
          {% if project.tech_stack %}<span>• {{ project.tech_stack | join: ", " }}</span>{% endif %}
        </p>
        <p class="listing-excerpt">{{ project.excerpt | default: project.content | strip_html | truncate: 160 }}</p>
        {% if project.tags %}
        <div class="listing-tags">
          {% for tag in project.tags %}
          <span class="tag">#{{ tag }}</span>
          {% endfor %}
        </div>
        {% endif %}
        <a href="{{ project.url | relative_url }}" class="listing-read-more">View Idea →</a>
      </div>
    </article>
    {% endfor %}
  </div>
  {% else %}
  <div class="card-item text-center" style="margin-top: 2rem;">
    <p class="lead">No open ideas yet. Have a problem you want solved with AI? Share it with the community.</p>
  </div>
  {% endif %}
</section>

<section class="container">
  <div class="guidelines-box text-center">
    <h3>Have an open-source idea?</h3>
    <p>Submit a PR on GitHub or chat with the community on Telegram to turn your idea into a real project.</p>
    <div class="hero-buttons" style="justify-content: center; margin-top: 1rem;">
      <a href="https://github.com/Axomiya-IT-Labs" target="_blank" rel="noopener noreferrer" class="btn btn-primary">Submit a PR on GitHub</a>
      <a href="https://t.me/AxomiyaITLabs" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">Chat on Telegram</a>
    </div>
  </div>
</section>
