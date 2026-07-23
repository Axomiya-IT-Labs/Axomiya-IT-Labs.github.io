# 🛠️ Axomiya IT Labs — Projects & Contributor Guide (`PROJECTS.md`)

Welcome to the **Projects & Contributor Guide** for **Axomiya IT Labs**. This guide is designed for developers, designers, writers, students, and community members who want to build, contribute to, or scale open-source projects in our community.

---

## 🎯 1. Core Goal of Our Projects

At **Axomiya IT Labs**, we build technology to solve real problems for people in Assam and beyond. Every project aims to remove friction for learners, builders, and everyday users through clear language, Assamese localization, and accessible open-source AI tools.

---

## 📂 2. Project Architecture & File Structure

Projects on our website are powered by Jekyll collections located in the `_projects/` directory:

```text
axomiyaitlabs/
├── _projects/                          # 🛠️ All project collection files (.md)
│   ├── 00-TEMPLATE.md                  # Template for Live / Beta / In Progress projects
│   ├── 00-IDEA-TEMPLATE.md             # Template for Open Community Ideas
│   ├── what-after-12.md                # Real Project Entry
│   ├── axomiya-ai-tutor.md             # Real Project Entry
│   └── open-assam-data.md              # Real Project Entry
└── assets/images/projects/             # 🖼️ Project Screenshots & Thumbnails (.webp preferred)
```

---

## 🚦 3. Project Lifecycles & Status Badges

Every project has a designated `status` in its front matter. This determines how it is rendered on the `/projects/` page:

| Status | Meaning | Rendered Location |
| :--- | :--- | :--- |
| **`Live`** | Production-ready tool or platform. | Active Projects Section |
| **`Beta`** | Working prototype undergoing testing. | Active Projects Section |
| **`In Progress`** | Active development underway. | Active Projects Section |
| **`Idea`** | Open community proposal looking for builders. | Ideas Bar Section |

---

## ✍️ 4. How to Add a New Project or Idea (Step-by-Step)

### Step 1: Choose the Right Template
- For **working projects, prototypes, or live tools**: copy `_projects/00-TEMPLATE.md`.
- For **unbuilt proposals or community ideas**: copy `_projects/00-IDEA-TEMPLATE.md`.

### Step 2: Create Your Project Markdown File
Name your file with a lowercase slug matching your project name:
`_projects/your-project-slug.md`

### Step 3: Fill in Front Matter Fields

```yaml
---
layout: project
title: "Your Project Title"
permalink: /projects/your-project-slug/
date: 2026-07-23
status: Beta                     # Options: Live, Beta, In Progress, Idea
category: AI & Education         # Options: AI & ML, Education, Data & Automation, Web
image: /assets/images/projects/your-project.webp
tags:
  - Assamese-AI
  - Open-Source
repo: "https://github.com/Axomiya-IT-Labs/your-repo"
demo: "https://your-demo.vercel.app"
tech_stack:
  - Next.js
  - Python
  - Tailwind CSS
---
```

### Step 4: Write Project Body Content
Structure your content with clear markdown headings:
- **`## What It Solves`** — The real-world problem.
- **`## Key Features`** — Bullet points of capabilities.
- **`## Who Is It For`** — Target users (students, teachers, developers).
- **`## How to Contribute`** — Instructions for new contributors.

### Step 5: Add Assets & Images
- Place images in `assets/images/projects/`.
- **`.webp` format is highly preferred** for fast performance and low bandwidth consumption.
- Keep image file sizes below 200KB.

---

## 🤝 5. Contribution Workflow (Pull Requests)

1. **Fork the Repository**: Fork `axomiyaitlabs/axomiya-it-labs.github.io` on GitHub.
2. **Create a Feature Branch**: `git checkout -b add-project-my-idea`
3. **Add Your File**: Create `_projects/my-idea.md` and upload your image to `assets/images/projects/`.
4. **Test Locally**:
   ```bash
   bundle exec jekyll build
   ```
5. **Submit a Pull Request**: Push your branch and open a PR with a concise description of your project.

---

## 📈 6. Scaling to 50+ Projects

To ensure the website scales smoothly as our community grows:
- Maintain consistent tags and categories (`AI & ML`, `Education`, `Data & Automation`, `Community & Web`).
- Ensure all projects include a valid `repo` link to an open-source GitHub repository.
- Regularly review the **Ideas Bar** to promote community ideas to **In Progress** as maintainers step up.

---

*Questions? Reach out in our [Telegram Community](https://t.me/AxomiyaITLabs) or open an issue on [GitHub](https://github.com/Axomiya-IT-Labs).*
