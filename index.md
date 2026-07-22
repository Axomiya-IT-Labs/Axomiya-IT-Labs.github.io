---
layout: default
title: Home
---

<div class="hero-section">
  <span class="hero-badge">Rooted in Assam</span>
  <h1 class="hero-title">Assam's first AI & open-source community.</h1>
  <p class="hero-subtitle">Everyone is welcome — no matter your age, background, or technical skill. If you are curious and want to learn, build, or share, you belong here.</p>
  <div class="hero-buttons">
    <a href="{{ '/projects/' | relative_url }}" class="btn btn-primary">Explore FOSS Projects</a>
    <a href="{{ '/community/' | relative_url }}" class="btn btn-secondary">Join Community</a>
  </div>
</div>

<section class="mission-block text-center container">
  <h2 class="section-title">Our Mission</h2>
  <p class="lead">
    The internet is the greatest free encyclopedia humanity has ever built. We are here to collect precise information, make thoughtful analyses, present clear findings, add local context, and make all of it accessible to everyone in Assam — so that no one is left behind by international standards of technology and knowledge.
  </p>
  <p class="lead">
    If you want to share what you know, benefit others, and explore new fields with genuine curiosity, this is your community. Assam's first AI and open-source space — where everyone is welcome, whatever you do professionally.
  </p>
</section>

<section class="what-we-do-section container">
  <div class="text-center">
    <h2 class="section-title">What We Do</h2>
    <p class="section-subtitle">Three words. One community.</p>
  </div>

  <div class="three-column-grid">
    <div class="card-item">
      <div class="card-icon">📖</div>
      <h3>Learn</h3>
      <p>Read short guides, watch practical tutorials, and explore AI tools in plain language. Each lesson is written to feel friendly, not intimidating, so beginners can keep going without getting bored.</p>
      <p class="card-quote">"Clear language lowers fear."</p>
    </div>

    <div class="card-item">
      <div class="card-icon">🔨</div>
      <h3>Build</h3>
      <p>Create real projects: websites, AI tools, automation scripts, and educational platforms. We keep the steps visible and the code open, so people feel progress quickly and can improve what already exists.</p>
      <p class="card-quote">"Visible progress keeps motivation alive."</p>
    </div>

    <div class="card-item">
      <div class="card-icon">🤝</div>
      <h3>Share</h3>
      <p>Share what you learn, even if it feels small. Every translation, tutorial, example, bug report, and line of code removes friction for the next person and makes the community feel easier to enter.</p>
      <p class="card-quote">"Small help compounds."</p>
    </div>
  </div>
</section>

<section class="principles-section container">
  <div class="text-center">
    <h2 class="section-title">What We Believe</h2>
    <p class="section-subtitle">Three principles that guide everything we build.</p>
  </div>

  <div class="principles-list">
    <div class="principle-card">
      <div class="principle-num">01</div>
      <h3>From Scrolling to Creating</h3>
      <p>Most people spend hours scrolling through things other people made. We help you turn that same curiosity into useful projects, small income paths, and real problem-solving. With AI assistants like ChatGPT, Copilot, and open-source models, you can start before you feel ready. No degree. No perfect English. Just one small build at a time.</p>
      <div class="principle-takeaway">Start with something small enough to finish today.</div>
    </div>

    <div class="principle-card">
      <div class="principle-num">02</div>
      <h3>Open Source, Made Easier by AI</h3>
      <p>Everything we make is free, transparent, and community-driven, built with contributors instead of only for users. AI reduces the hard parts: drafting docs, translating content, reviewing code, and finding bugs. That gives people more energy for ideas, judgment, and impact.</p>
      <div class="principle-takeaway">You can contribute even if your first contribution is a correction.</div>
    </div>

    <div class="principle-card">
      <div class="principle-num">03</div>
      <h3>Accessible Tech & Learning</h3>
      <p>Language does not decide who gets to learn. We build clear, accessible resources so every learner starts with confidence. Understanding comes first. Speed comes after.</p>
      <div class="principle-takeaway">Understanding comes first. Speed comes after.</div>
    </div>
  </div>
</section>

<section class="who-this-is-for container text-center">
  <h2 class="section-title">Who This Is For</h2>
  <p class="lead">Built for every person in Assam — and beyond.</p>
  <p>You do not need to be a developer. You do not need to be an expert. If you are curious, you belong here. AI removes the barriers — we just need your willingness to explore and learn.</p>

  <div class="pill-cloud" style="margin-top: 1.5rem;">
    <span class="pill-badge">Kids</span>
    <span class="pill-badge">Students</span>
    <span class="pill-badge">Teachers</span>
    <span class="pill-badge">Parents</span>
    <span class="pill-badge">Developers</span>
    <span class="pill-badge">Entrepreneurs</span>
    <span class="pill-badge">Freelancers</span>
    <span class="pill-badge">Job Seekers</span>
    <span class="pill-badge">Govt. Employees</span>
    <span class="pill-badge">Small Businesses</span>
    <span class="pill-badge">Creators</span>
    <span class="pill-badge">Lifelong Learners</span>
  </div>
</section>

<section class="container">
  <div class="guidelines-box text-center">
    <h3>Open Source — Not Open for Business Promotions</h3>
    <p>Axomiya IT Labs is a free and open-source community. Please do not use this space for business promotions, paid services, or commercial advertisements. All contributions must genuinely benefit the community. For business collaborations, sponsorships, or paid opportunities, please join our Telegram community and speak directly with the admins.</p>
  </div>
</section>

<section class="latest-announcements-section container">
  <div class="text-center">
    <h2 class="section-title">Latest Announcements</h2>
  </div>
  <div class="announcements-grid">
    {% for announcement in site.data.announcements limit:3 %}
      {% include components/announcement-card.html announcement=announcement %}
    {% endfor %}
  </div>
</section>
