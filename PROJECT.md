# 📘 Axomiya IT Labs — Ultimate Master Documentation (`PROJECT.md`)

Welcome to the single-source-of-truth master documentation for **Axomiya IT Labs**. This static website is engineered with an **Anthropic-inspired warm minimalist design aesthetic**, fully **mobile-first & desktop-friendly**, and 100% compatible with **GitHub Pages** (Jekyll).

---

## 🏛️ 1. Core Mission & Identity

> **Rooted in Assam — Assam's first AI & open-source community.**
> Everyone is welcome — no matter your age, background, or technical skill. If you are curious and want to learn, build, or share, you belong here.

### The Three Pillars (Learn, Build, Share):
- 📖 **Learn**: Read short guides, watch practical tutorials, and explore AI tools in plain language. *(Clear language lowers fear.)*
- 🔨 **Build**: Create real projects: websites, AI tools, automation scripts, and educational platforms. *(Visible progress keeps motivation alive.)*
- 🤝 **Share**: Share what you learn, even if it feels small. Every translation, tutorial, example, bug report, and line of code removes friction for the next person. *(Small help compounds.)*

### The Three Guiding Principles:
1. **01 From Scrolling to Creating**: Turn curiosity into useful projects. Start with something small enough to finish today.
2. **02 Open Source, Made Easier by AI**: Everything is free and community-driven. You can contribute even if your first contribution is a correction.
3. **03 Accessible Tech & Learning**: Language does not decide who gets to learn. Understanding comes first. Speed comes after.

---

## 📂 2. Repository Architecture & Layout

```text
axomiyaitlabs/
├── .github/
│   └── workflows/
│       └── pages.yml              # 🚀 GitHub Actions deployment workflow
├── _data/                         # 📊 Data files (Single source of content)
│   ├── announcements.yml          # Product launches & updates
│   ├── community.yml              # Member profiles & statistics
│   ├── nav.yml                    # Main navigation bar links
│   ├── projects.yml               # FOSS repositories & Ideas Bar ideas
│   └── team.yml                   # Leadership, developers, & advisors
├── _includes/                     # 🧩 Reusable HTML Components
│   ├── header.html                # Responsive header & drawer menu
│   ├── footer.html                # Dark minimalist footer
│   ├── components/
│   │   ├── announcement-card.html # Announcement card
│   │   ├── member-card.html       # Member card
│   │   └── team-card.html         # Team member card
│   ├── partials/
│   │   └── newsletter-signup.html # Newsletter form
│   └── sections/
│       ├── community-stats.html   # Community stats grid
│       └── team-grid.html         # Team grid layout
├── _layouts/                      # 📐 HTML Page Layout Templates
│   ├── default.html               # Head, Google Fonts (Instrument Serif + Inter), SEO tags
│   ├── page.html                  # Standard page template
│   ├── post.html                  # Blog post template
│   ├── announcements.html         # Announcements hub template
│   ├── community.html             # Community landing template
│   └── team.html                  # Team page template
├── _pages/                        # 📄 Main Pages
│   ├── about.md                   # /about/
│   ├── announcements/index.md     # /announcements/
│   ├── community/index.md         # /community/
│   ├── projects/index.md          # /projects/ (FOSS & Ideas Bar)
│   └── team/index.md              # /team/
├── _posts/                        # ✍️ Blog Posts (YYYY-MM-DD-title.md)
│   └── 2026-07-20-welcome-to-axomiya.md
├── _sass/                         # 🎨 SASS Stylesheets (Anthropic Design System)
│   ├── base.scss                  # Fonts, typography, design tokens, buttons
│   ├── layout.scss                # Header, mobile navigation drawer, dark footer
│   ├── components/
│   │   └── _ai-chat.scss          # AI assistant widget styles
│   └── pages/
│       ├── _announcements.scss    # Announcements grid
│       ├── _community.scss       # Member cards & stats grid
│       ├── _projects.scss         # FOSS project cards & Ideas Bar styles
│       └── _team.scss             # Team member cards
├── assets/                        # 🖼️ Static Assets
│   ├── css/
│   │   └── main.scss              # Main stylesheet entrypoint
│   ├── js/
│   │   └── main.js                # Mobile drawer menu & smooth scroll JS
│   └── images/                    # Image assets
├── _config.yml                    # ⚙️ Jekyll Configuration
├── Gemfile                        # 💎 Dependencies
├── index.md                       # 🏠 Home Page
├── README.md                      # GitHub Repository README
└── PROJECT.md                     # 📖 This Documentation File
```

---

## 🎨 3. Design System & Theme Tokens (Anthropic Aesthetic)

The design system mimics Anthropic's warm, elegant editorial aesthetic (`anthropic.com`):

```scss
:root {
  --bg-main: #fcfbfa;            /* Warm off-white background */
  --bg-card: #ffffff;            /* Pure white card backgrounds */
  --bg-subtle: #f4f0ea;          /* Warm subtle beige containers */
  --bg-dark: #141413;            /* Warm dark footer */
  --text-main: #191919;          /* Deep charcoal primary text */
  --text-muted: #595755;        /* Muted charcoal secondary text */
  --accent-warm: #cc5500;        /* Signature warm terracotta/amber accent */
  --border-light: #e8e3dc;       /* Warm subtle border lines */
  --font-serif: 'Instrument Serif', Georgia, serif; /* Editorial headings */
  --font-sans: 'Inter', sans-serif;                /* Clean sans-serif body */
}
```

### Key Principles:
- **Mobile-First**: Base CSS applies to mobile devices; upward scaling `@media (min-width: 768px)` enhances desktop layouts.
- **No Heavy Hard Colors**: Clean, warm off-white tones, subtle borders, high readability.
- **Editorial Typography**: Large, elegant serif headings paired with clean modern body sans-serif.

---

## 🛠️ 4. How to Update Anything on the Site

### ✍️ A. Publishing Articles / Blog Posts
1. Create `_posts/YYYY-MM-DD-your-title.md`.
2. Add Front Matter:
```markdown
---
layout: post
title: "Article Title"
author: "Author Name"
categories: [AI, Learning]
excerpt: "Article summary."
image: "/assets/images/announcements/2026-07/welcome.jpg"
---

Write article content in Markdown...
```

### 👨‍💻 B. Adding Team Members
Edit `_data/team.yml` under `leadership`, `developers`, `designers`, or `advisors`.

### 📢 C. Adding Announcements
Edit `_data/announcements.yml`.

### 💡 D. Adding FOSS Software Repositories & Ideas to the Ideas Bar
Edit `_data/projects.yml`:
- Add to `projects` for completed open-source software.
- Add to `ideas_bar` for project ideas that developers/nerds can pick up and build.

---

## 🚀 5. Running & Deploying

### Local Development:
```bash
bundle install
bundle exec jekyll serve
```
Open `http://localhost:4000`.

### GitHub Pages (2026 Standard):
Pushes to `main` automatically deploy via `.github/workflows/pages.yml`.

---
*Documentation maintained by Axomiya IT Labs.*
