---
name: dalesackrider-blog
title: Authoring & Publishing for dalesackrider.com
description: Author, format, review, and publish blog posts and thought-leadership essays for Dale Sackrider's personal blog at dalesackrider.com. Use when drafting new articles, refining ideas, matching Dale's distinct voice (executive cloud leadership, systems thinking, practical analogies, operational clarity), formatting Astro markdown frontmatter, and deploying to Cloudflare.
version: 1.0.0
author: Dale Sackrider
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Writing, Blogging, Thought-Leadership, Cloud-Architecture, Dale-Sackrider, Astro]
    category: domain
    requires_toolsets: []
---

# Authoring & Publishing for dalesackrider.com

## Overview
This skill guides agents in writing, reviewing, and publishing articles for **Dale Sackrider's personal blog** at [dalesackrider.com](https://dalesackrider.com). 

The site is built with **Astro**, version-controlled in Git, and hosted on **Cloudflare Edge**.

---

## 🎙️ Dale Sackrider's Voice & Editorial Style Guide

### Who Dale Is
* **Role:** Vice President of Cloud Engineering at Frontline Education; previously led large-scale cloud transformations at SAP Global Cloud Services; started as a hands-on systems administrator.
* **Core Philosophy:** "Make things work better, make them simpler, and make them easier for people to build on."
* **Audience:** Engineering leaders, architects, SRE/DevOps practitioners, enterprise executives, and thoughtful technologists.

### Voice & Tone Principles
1. **Direct & Pragmatic:** Cut straight to the point. Avoid academic jargon, buzzword padding, and passive voice.
2. **Systems-First Thinking:** Connect individual problems (e.g., a ticket queue, a failed project proposal, a bad meeting) to underlying feedback loops, incentives, and operational architecture.
3. **Relatable Analogies:** Use concrete, everyday stories or analogies from real life (e.g., household chores, dull scissors, marriage QBRs) to anchor complex organizational principles.
4. **Anti-Hype & Grounded:** Skeptical of silver bullets (like "just sprinkle in AI" or "hire 10 more engineers"). Focus on operational friction, clarity, and accountability.
5. **Vulnerable & Authentic:** Share real career setbacks, lay-offs, missteps, and hard-learned truths with humility and humor.

### Standard Essay Structure
* **The Hook:** A short, punchy opening line or real-world conversation/scenario (e.g., *"You make it sound easy! That’s what a co-worker said to me yesterday..."*).
* **The Tension / The Myth:** Unpack the common misconception or surface-level reaction people have.
* **The Underlying System:** Explain the deeper mechanics or hidden costs at play.
* **Actionable Takeaways:** Provide 2–4 practical, memorable rules of thumb.
* **Closing:** A crisp takeaway or reflective question that leaves the reader thinking.

---

## 📁 Repository & File Structure

* **Project Root:** `/Users/skippy/repos/dalesackrider-com`
* **Content Directory:** `/Users/skippy/repos/dalesackrider-com/src/content/blog/`
* **GitHub Repository:** `https://github.com/dsackr/dalesackrider-com`
* **Live Site:** `https://dalesackrider.com`

---

## 📝 Post Format Specification

Every article is a single Markdown file located at `/Users/skippy/repos/dalesackrider-com/src/content/blog/<slug>.md`.

### Frontmatter Schema
```yaml
---
title: "Article Title in Title Case or Direct Statement"
description: "A compelling 1-2 sentence preview under 160 characters for social cards and search."
pubDate: "YYYY-MM-DD"
draft: false
tags: ["leadership", "cloud", "systems"]
---
```

### Formatting Rules
* Use standard Markdown headings (`##`, `###`).
* Keep paragraphs concise (2–4 sentences).
* Use blockquotes (`>`) for notable quotes or dialogue.
* Use bullet points for lists and comparisons.

---

## 🚀 Step-by-Step Authoring & Publishing Workflow

### 1. Draft the Post
Create `/Users/skippy/repos/dalesackrider-com/src/content/blog/<slug>.md` with frontmatter and Markdown body.

### 2. Verify Build Locally
Run the Astro build to ensure TypeScript and content collections validate without error:
```bash
cd /Users/skippy/repos/dalesackrider-com
npm run build
```

### 3. Deploy Live to Cloudflare
Deploy the updated assets to Cloudflare Edge:
```bash
cd /Users/skippy/repos/dalesackrider-com
npx wrangler deploy
```

### 4. Commit and Push to GitHub
```bash
cd /Users/skippy/repos/dalesackrider-com
git add .
git commit -m "Publish: <Title of Post>"
git push origin main
```

---

## 🔍 Quality Checklist Before Publishing
- [ ] Does this sound like Dale (practical, grounded, systems-focused)?
- [ ] Is the title punchy and free of generic clickbait?
- [ ] Is `pubDate` set correctly in `YYYY-MM-DD` format?
- [ ] Is `description` under 160 characters?
- [ ] Did `npm run build` succeed with 0 errors?
- [ ] Is the article visible on https://dalesackrider.com?
