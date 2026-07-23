---
layout: default
title: Announcements
permalink: /announcements/
---

<div class="announcements-header-block text-center">
    <h2>📢 Latest Community Announcements</h2>
    <p>Discover product launches, news, upcoming events, and project milestones.</p>
</div>

{% assign announcements_list = site.announcements | where_exp: "item", "item.published != false" | sort: "date" | reverse %}
{% if announcements_list.size > 0 %}
<div class="listings-grid">
    {% for announcement in announcements_list %}
    <article class="listing-card">
        {% if announcement.image %}
        <div class="listing-image">
            <img src="{{ announcement.image | relative_url }}" alt="{{ announcement.title }}">
            {% if announcement.type %}<span class="listing-badge">{{ announcement.type | capitalize }}</span>{% endif %}
        </div>
        {% endif %}
        <div class="listing-content">
            <h2><a href="{{ announcement.url | relative_url }}">{{ announcement.title }}</a></h2>
            <p class="listing-meta">
                {% if announcement.date %}<span>📅 {{ announcement.date | date: "%B %d, %Y" }}</span>{% endif %}
                {% if announcement.author %}<span>✍️ {{ announcement.author }}</span>{% endif %}
            </p>
            <p class="listing-excerpt">{{ announcement.excerpt }}</p>
            {% if announcement.tags %}
            <div class="listing-tags">
                {% for tag in announcement.tags %}
                    <span class="tag">#{{ tag }}</span>
                {% endfor %}
            </div>
            {% endif %}
            <a href="{{ announcement.url | relative_url }}" class="listing-read-more">Read More →</a>
        </div>
    </article>
    {% endfor %}
</div>
{% else %}
<div class="card-item text-center" style="margin-top: 2rem;">
    <p class="lead">No announcements yet. Stay tuned — big updates are coming soon.</p>
</div>
{% endif %}
