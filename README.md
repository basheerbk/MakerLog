# iLab Maker Journal

A personal activity log for my work as a **Maker Mentor** at **iLab**.

This site documents mentoring sessions, maker projects guided, and systems implemented over time.

---

## What's Inside

- **Session journals** — logged after each mentoring session
- **Project notes** — summaries of maker projects I've guided


---

## Running Locally

### Prerequisites

- Python 3.x
- pip

### Setup

```bash
# Clone the repo
git clone https://github.com/basheerbk/MakerLog.git
cd MakerLog

# Install dependencies
pip install -r requirements.txt

# Serve locally
mkdocs serve
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

---

## Adding a New Session Log

1. Create a new branch:

```bash
git checkout -b log/YYYY-MM-DD-session-name
```

2. Add a new post at:

```
docs/blog/posts/YYYY-MM-DD-session-name.md
```

3. Use this front matter:

```yaml
---
title: 'iLab Session #XX: Session Name'
date: YYYY-MM-DD
authors: [mentor]
slug: ilab-session-XX-name
description: >
  Short description of the session.
tags:
  - mentoring
  - projects
---
```

4. Commit and push:

```bash
git add .
git commit -m "Add session log YYYY-MM-DD"
git push -u origin log/YYYY-MM-DD-session-name
```

5. Open a pull request to `main` — GitHub Actions will auto-deploy to GitHub Pages.

---

## Journal Entry Template

```markdown
## Overview
3–6 lines about what happened.

## Mentees / Participants
- Name – what they're working on

## Projects Guided
- **Project Name** — one-line summary

## Activities
- What you did hands-on

## Highlights
- Key wins or breakthroughs

## Challenges
- Blockers or areas to follow up

## Next Steps
- [ ] Action item

## Next Session
- Focus: TBD
- Date: TBD
```

---

## Deployment

This site auto-deploys to GitHub Pages via GitHub Actions on every push to `main`.

Set up GitHub Pages:
1. Go to your repo → **Settings** → **Pages**
2. Set source to `gh-pages` branch
