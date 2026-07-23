# 🔬 Axomiya IT Labs — Research & Articles Guide (`RESEARCH.md`)

Welcome to the dedicated guide for publishing **Research Articles, Case Studies, Tutorials, and Technical Guides** at **Axomiya IT Labs**. Anyone in our community can contribute research content to help educate others across Assam and the open-source world.

---

## 🎯 1. Core Goal of Our Research

Our research section (`/research/`) is designed to demystify artificial intelligence, data science, open-source tech, and local tech challenges. We write in plain language, breaking down complex topics into actionable, understandable articles.

---

## 📂 2. File Location & Naming Convention

Research articles are stored in the `_posts/` directory as Markdown files:

```text
axomiyaitlabs/
├── _posts/
│   ├── 2026-07-23-ai-problem-breakdown.md    # Example research post
│   └── YYYY-MM-DD-your-article-slug.md       # New research article
└── assets/images/research/                    # 🖼️ Article banner images (.webp preferred)
```

**Naming Rule**: Files MUST strictly follow `YYYY-MM-DD-title-slug.md` (e.g., `2026-07-24-intro-to-local-llms.md`).

---

## ✍️ 3. Article Front Matter Schema

Every research post must begin with Jekyll Front Matter:

```markdown
---
layout: post
title: "Understanding Local Language Models in Assam"
date: 2026-07-24
author: "Your Name"
permalink: /research/intro-to-local-llms/
excerpt: "A comprehensive breakdown of how localized AI models work and why open data matters for regional languages."
image: "/assets/images/research/local-llms.webp"
tags:
  - AI-In-Assam
  - Open-Source
  - NLP
---
```

---

## 📖 4. Editorial Guidelines & Structure

To ensure high quality across all articles:
1. **Plain Language First**: Explain technical terms simply. Clear language lowers fear.
2. **Actionable Takeaways**: Include real code snippets, visual diagrams, or step-by-step examples.
3. **Assamese Context**: When applicable, highlight local relevance for Assam and regional tech growth.
4. **Structured Headings**: Use `##` and `###` Markdown headings to organize sections.

---

## 🖼️ 5. Images & Media Assets

- Place article preview images in `assets/images/research/`.
- Use **`.webp`** format whenever possible to maintain fast page load speeds.
- Reference images in Markdown using relative URLs:  
  `![Diagram description]({{ '/assets/images/research/diagram.webp' | relative_url }})`

---

## 🤝 6. Submission & Contribution Steps

1. **Fork the Repository**: Fork `Axomiya-IT-Labs/axomiya-it-labs.github.io` on GitHub.
2. **Create Article File**: Add `_posts/YYYY-MM-DD-your-slug.md`.
3. **Test Locally**: Run `bundle exec jekyll serve` and check your article on `http://localhost:4000/research/`.
4. **Submit PR**: Open a Pull Request on GitHub with a brief description of your article.

---
*Maintained with ❤️ by Axomiya IT Labs community.*
