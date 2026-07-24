---
layout: default
title: Community
permalink: /community/
---

<div class="hero-section">
    <span class="hero-badge">Join Us</span>
    <h1 class="hero-title">Assam's AI & Open-Source Community</h1>
    <p class="hero-subtitle">Connect with builders, learners, and innovators from Assam and beyond.</p>
    <div class="hero-buttons" style="justify-content: center; margin-top: 1.5rem;">
        <a href="https://t.me/AxomiyaITLabs" target="_blank" rel="noopener noreferrer" class="btn btn-primary">Join Telegram</a>
        <a href="https://github.com/Axomiya-IT-Labs" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">Visit GitHub</a>
    </div>
</div>

<section class="community-stats container text-center" style="margin: 3rem 0;">
    <h2 class="section-title">Our Community at a Glance</h2>
    <div class="three-column-grid">
        <div class="card-item">
            <div style="font-size: 2.5rem; font-weight: 700; color: var(--accent-warm); margin-bottom: 0.5rem;">{{ site.data.community.stats.total_members }}</div>
            <h3 style="margin-top: 0;">Members</h3>
            <p>Builders, learners, and curious minds</p>
        </div>
        <div class="card-item">
            <div style="font-size: 2.5rem; font-weight: 700; color: var(--accent-warm); margin-bottom: 0.5rem;">{{ site.data.community.stats.active_contributors }}</div>
            <h3 style="margin-top: 0;">Contributors</h3>
            <p>Active open-source contributors</p>
        </div>
        <div class="card-item">
            <div style="font-size: 2.5rem; font-weight: 700; color: var(--accent-warm); margin-bottom: 0.5rem;">{{ site.data.community.stats.projects }}</div>
            <h3 style="margin-top: 0;">Projects</h3>
            <p>Live tools and experiments</p>
        </div>
    </div>
</section>

<section class="container" style="margin: 3rem 0;">
    <h2 class="section-title text-center">Featured Members</h2>
    <div class="listings-grid">
        {% for member in site.data.community.featured_members limit: 6 %}
        <div class="card-item">
            <h3 style="margin-top: 0;">{{ member.name }}</h3>
            <p><strong>{{ member.role }}</strong></p>
            <p style="font-size: 0.9rem; color: var(--text-light);">📍 {{ member.location }}</p>
            {% if member.skills %}
            <div style="margin: 1rem 0;">
                {% for skill in member.skills %}
                <span class="pill-badge">{{ skill }}</span>
                {% endfor %}
            </div>
            {% endif %}
            {% if member.github %}
            <a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener noreferrer" class="btn btn-secondary btn-sm">View GitHub</a>
            {% endif %}
        </div>
        {% endfor %}
    </div>
</section>

<section class="container">
    <div class="guidelines-box text-center">
        <h3>How to Get Involved</h3>
        <p>Start with any of these paths:</p>
        <div class="three-column-grid" style="margin-top: 1.5rem;">
            <div>
                <h4>1. Share Knowledge</h4>
                <p>Write a tutorial, guide, or research post in our repository.</p>
            </div>
            <div>
                <h4>2. Build Together</h4>
                <p>Contribute to open-source projects or propose your own.</p>
            </div>
            <div>
                <h4>3. Join Discussions</h4>
                <p>Connect on Telegram, GitHub, or at community events.</p>
            </div>
        </div>
    </div>
</section>
