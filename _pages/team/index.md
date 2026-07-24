---
layout: default
title: Team
permalink: /team/
---

<div class="hero-section">
    <span class="hero-badge">Meet the Team</span>
    <h1 class="hero-title">Meet Our Builders</h1>
    <p class="hero-subtitle">The passionate people behind Axomiya IT Labs.</p>
</div>

<section class="container text-center">
    <h2 class="section-title">Leadership & Founders</h2>
    <div class="listings-grid">
        {% for member in site.data.team.leadership %}
        <div class="card-item" style="text-align: center;">
            {% if member.image %}
            <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 120px; height: 120px; border-radius: 50%; margin-bottom: 1rem; object-fit: cover;">
            {% endif %}
            <h3 style="margin-top: 0;">{{ member.name }}</h3>
            <p style="color: var(--accent-warm); font-weight: 600; margin-bottom: 0.5rem;">{{ member.role }}</p>
            <p style="font-size: 0.9rem; color: var(--text-light);">{{ member.bio }}</p>
            {% if member.twitter or member.github or member.linkedin %}
            <div style="margin-top: 1rem;">
                {% if member.github %}
                <a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener noreferrer" class="btn btn-secondary btn-sm">GitHub</a>
                {% endif %}
                {% if member.twitter %}
                <a href="https://twitter.com/{{ member.twitter }}" target="_blank" rel="noopener noreferrer" class="btn btn-secondary btn-sm">Twitter</a>
                {% endif %}
                {% if member.linkedin %}
                <a href="https://linkedin.com/in/{{ member.linkedin }}" target="_blank" rel="noopener noreferrer" class="btn btn-secondary btn-sm">LinkedIn</a>
                {% endif %}
            </div>
            {% endif %}
        </div>
        {% endfor %}
    </div>
</section>

<section class="container text-center" style="margin-top: 3rem;">
    <h2 class="section-title">Contributors</h2>
    <p class="section-subtitle">Thank you to everyone helping build this community!</p>
    <p>Visit our <a href="https://github.com/Axomiya-IT-Labs" target="_blank" rel="noopener noreferrer">GitHub organization</a> to see all contributors.</p>
</section>
