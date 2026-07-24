---
layout: default
title: Research & Articles
permalink: /research/
---

<div class="announcements-header-block text-center">
    <h2>Research & Guides</h2>
    <p>Tutorials, case studies, AI breakdowns, and technical deep-dives.</p>
</div>

{% assign research_posts = site.posts | where_exp: "item", "item.published != false" | sort: "date" | reverse | where_exp: "item", "item.title != 'Welcome to Axomiya IT Labs! 🚀'" %}
{% if research_posts.size > 0 %}
<div class="listings-grid">
    {% for post in research_posts %}
    <article class="listing-card">
        <div class="listing-content">
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p class="listing-meta">
                {% if post.date %}<span>{{ post.date | date: "%B %d, %Y" }}</span>{% endif %}
                {% if post.author %}<span>{{ post.author }}</span>{% endif %}
            </p>
            <p class="listing-excerpt">{{ post.excerpt }}</p>
            {% if post.tags %}
            <div class="listing-tags">
                {% for tag in post.tags %}
                    <span class="tag">#{{ tag }}</span>
                {% endfor %}
            </div>
            {% endif %}
            <a href="{{ post.url | relative_url }}" class="listing-read-more">Read More →</a>
        </div>
    </article>
    {% endfor %}
</div>
{% else %}
<div class="card-item text-center" style="margin-top: 2rem;">
    <p class="lead">No research articles yet. Stay tuned!</p>
</div>
{% endif %}
