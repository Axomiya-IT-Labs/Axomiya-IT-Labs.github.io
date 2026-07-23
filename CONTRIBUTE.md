# 📘 Axomiya IT Labs — Master Architecture & Contribution Guide (`CONTRIBUTE.md`)

Welcome to the central master documentation and contributor manual for **Axomiya IT Labs**. This repository powers our static website and community platform, engineered with an **Anthropic-inspired warm minimalist design aesthetic**, fully **mobile-first**, accessible, and 100% hosted on **GitHub Pages** (Jekyll).

---

## 🏛️ 1. Core Mission & Identity

> **Rooted in Assam — Assam's first AI & open-source community.**  
> Everyone is welcome — no matter your age, background, or technical skill. If you are curious and want to learn, build, or share, you belong here.

### The Three Pillars:
- 📖 **Learn**: Read short guides, watch practical tutorials, and explore AI tools in plain language. *(Clear language lowers fear.)*
- 🔨 **Build**: Create real projects: websites, AI tools, automation scripts, and educational platforms. *(Visible progress keeps motivation alive.)*
- 🤝 **Share**: Share what you learn, even if it feels small. Every translation, tutorial, example, bug report, and line of code removes friction for the next person. *(Small help compounds.)*

---

## 📂 2. Master Repository Architecture

```text
axomiyaitlabs/
├── .github/
│   └── workflows/
│       └── pages.yml              # 🚀 GitHub Actions automated build & deployment workflow
├── _data/                         # 📊 YAML Data Files
│   ├── navigation.yml             # Main navigation menu structure (with dropdown support)
│   └── team.yml                   # Team member profiles & roles
├── _includes/                     # 🧩 Reusable HTML Components
│   ├── header.html                # Responsive header + OpenAI-style Live Search + Mobile Drawer
│   ├── footer.html                # Dark minimalist footer with row columns & copyright bottom bar
│   ├── components/                # UI Cards (announcements, members, team)
│   ├── partials/                  # Newsletters & reusable forms
│   └── sections/                  # Homepage & community layout sections
├── _layouts/                      # 📐 Jekyll Layout Templates
│   ├── default.html               # Master layout (SEO tags, Google Fonts, header, footer, search modal)
│   ├── page.html                  # Standard page template
│   ├── post.html                  # Blog & research post layout
│   ├── project.html               # Project detail layout
│   ├── announcements.html         # Announcements hub template
│   ├── community.html             # Community landing template
│   └── team.html                  # Team page template
├── _pages/                        # 📄 Main Page Views
│   ├── about/index.md             # /about/
│   ├── contribute/index.md        # /contribute/
│   ├── projects/index.md          # /projects/ (Active projects + Ideas bar)
│   ├── announcements/index.md     # /announcements/
│   ├── research/index.md          # /research/
│   ├── community/index.md         # /community/ (Official channels with platform SVG icons)
│   └── team/index.md              # /team/
├── _posts/                        # ✍️ Research Articles (YYYY-MM-DD-title.md)
├── _projects/                     # 🛠️ Project Collection (.md files for active projects & ideas)
├── _announcements/                # 📢 Announcements Collection
├── _sass/                         # 🎨 SASS Stylesheets (Anthropic Design System)
│   ├── base.scss                  # Typography, variables, global reset, buttons
│   ├── layout.scss                # Header, search modal, full-screen mobile nav, dark footer
│   ├── components/                # Modular SASS components
│   └── pages/                     # Page-specific styling rules
├── assets/                        # 🖼️ Static Assets
│   ├── css/
│   │   └── main.scss              # SCSS entry point compiled to main.css
│   ├── js/
│   │   └── main.js                # Core interactive JavaScript
│   └── images/
│       ├── icons/                 # Official SVG icons (github, x, linkedin, telegram, etc.)
│       ├── og-image.webp          # OpenGraph social preview image
│       └── {projects,team,etc}/   # Asset media directories
├── search.json                    # 🔍 Dynamic Jekyll search index generator
├── _config.yml                    # ⚙️ Jekyll Site Configuration
├── Gemfile                        # 💎 Ruby dependencies
├── index.md                       # 🏠 Landing Page
├── README.md                      # 📖 GitHub Repository README & Documentation Hub
├── PROJECT.md                     # 🛠️ Project Updates & Ideas Guide
├── RESEARCH.md                    # 🔬 Research & Articles Guide
└── CONTRIBUTE.md                  # 📘 Master Architecture & Git Manual (This File)
```

---

## 🎨 3. Design System & Key Features

### Anthropic Warm Minimalist Design System
```scss
:root {
  --bg-main: #fcfbfa;            /* Warm off-white page background */
  --bg-card: #ffffff;            /* Pure white content cards */
  --bg-subtle: #f4f0ea;          /* Warm subtle beige containers */
  --bg-dark: #141413;            /* Dark minimalist footer */
  --text-main: #191919;          /* Primary dark charcoal text */
  --text-muted: #595755;        /* Secondary muted charcoal text */
  --accent-warm: #cc5500;        /* Signature warm terracotta/amber accent */
  --border-light: #e8e3dc;       /* Clean subtle line borders */
  --font-serif: 'Instrument Serif', Georgia, serif; /* Editorial headings */
  --font-sans: 'Inter', sans-serif;                /* Body & navigation */
}
```

### Key Technical Features
1. **🔍 OpenAI-Style Live Search**:
   - Integrated search trigger button in header with `⌘K` / `Ctrl+K` shortcut.
   - Live modal querying auto-updating `search.json`.
2. **📱 Mobile Drawer Navigation**:
   - Full-screen overlay (`top: 0`) with `z-index: 1000000` toggle button ensuring 100% visibility.
3. **🦶 Structured Dark Footer**:
   - Dual-column desktop layout (`Quick Links` & `Connect` side-by-side) with pinned copyright bottom bar.
4. **⚡ Official Platform SVG Icons**:
   - Vector SVG icons across `/community/` and footer.

---

## 💻 4. Local Development Setup

### Prerequisites
- **Ruby** (v3.0+)
- **Bundler** (`gem install bundler`)

### Step-by-Step Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Axomiya-IT-Labs/axomiya-it-labs.github.io.git
   cd axomiya-it-labs.github.io
   ```
2. **Install Ruby gems**:
   ```bash
   bundle install
   ```
3. **Run local Jekyll server**:
   ```bash
   bundle exec jekyll serve
   ```
4. **Open in browser**: Visit `http://localhost:4000`.

---

## 🤝 5. Git & Pull Request (PR) Workflow

1. **Fork the Repository**: Click "Fork" on GitHub.
2. **Create a Feature Branch**:
   ```bash
   git checkout -b feature/my-contribution
   ```
3. **Make Your Changes**: Add/modify files.
4. **Verify Locally**: Run `bundle exec jekyll serve` to verify layout.
5. **Commit & Push**:
   ```bash
   git add .
   git commit -m "feat: your descriptive commit message"
   git push origin feature/my-contribution
   ```
6. **Open Pull Request**: Submit a PR to `Axomiya-IT-Labs/axomiya-it-labs.github.io`.

---
*Maintained with ❤️ by Axomiya IT Labs community.*
