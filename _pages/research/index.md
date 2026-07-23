---
layout: default
title: Research & Insights
permalink: /research/
---

<div class="hero-section">
  <span class="hero-badge">Real Problems. Real Tech Solutions.</span>
  <h1 class="hero-title">Research & Insights</h1>
  <p class="hero-subtitle">This is not dry academic theory. We publish practical breakdowns of everyday problems in Assam and India — and how AI / open-source tech solves them.</p>
</div>

<section class="container">
  <div class="guidelines-box text-center">
    <h3>Want to submit a problem breakdown?</h3>
    <p>Check out our <a href="https://github.com/Axomiya-IT-Labs" target="_blank" rel="noopener noreferrer">GitHub Repo</a> or discuss it on our <a href="{{ '/community/' | relative_url }}">Community page</a>.</p>
  </div>
</section>

<section class="container">
  <div class="text-center">
    <h2 class="section-title">Latest Breakdowns</h2>
    <p class="section-subtitle">Problem → Friction → AI Solution</p>
  </div>

  <div class="research-grid">
    {% for post in site.posts %}
    <article class="research-card listing-card">
      {% if post.image %}
      <div class="listing-image">
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
        <span class="listing-badge">Research</span>
      </div>
      {% endif %}
      <div class="listing-content">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="listing-meta">
          <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
          {% if post.author %}<span>✍️ {{ post.author }}</span>{% endif %}
        </p>
        <p class="listing-excerpt">{{ post.excerpt | default: post.content | strip_html | truncate: 160 }}</p>
        {% if post.tags %}
        <div class="listing-tags">
          {% for tag in post.tags %}
          <span class="tag">#{{ tag }}</span>
          {% endfor %}
        </div>
        {% endif %}
        <a href="{{ post.url | relative_url }}" class="listing-read-more">Read Breakdown →</a>
      </div>
    </article>
    {% endfor %}
  </div>
</section>
