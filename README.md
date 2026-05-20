# muru825.github.io

Personal website for Murari Ganesan. Built with Jekyll, deployed via GitHub Pages.

---

## Editing your content

### Personal info & bio

Open `_config.yml` and edit the `author:` block:

- **name, email, github** — contact info used in nav and footer
- **bio** — the paragraph on your homepage
- **photo** — set to `/assets/img/profile.jpg` and drop your photo there (or leave `""` for placeholder)
- **interests** — the tags shown below your bio
- **stats** — the three sidebar stats (advisor, publications, open to)

Changes to `_config.yml` require a page reload to appear locally; GitHub Pages picks them up on push.

---

### Research papers

Edit `_data/research.yml`. Add one block per paper:

```yaml
- title: "Paper Title"
  authors: "Murari Ganesan, Co-author"
  venue: "ACL 2025"
  year: 2025
  url: "https://arxiv.org/abs/..."  # or leave ""
```

Papers appear in the order listed, so put the most recent first.

---

### Blog posts

Create a new file in `_posts/` named `YYYY-MM-DD-your-title.md`:

```markdown
---
layout: post
title: "Post Title"
date: 2026-03-15
excerpt: "One-sentence summary shown in the listing."
---

Post body in Markdown here.
```

Delete `_posts/2026-01-01-example-post.md` when you add your first real post.

---

### Photography

Drop image files (`.jpg`, `.jpeg`, `.png`, or `.webp`) into `assets/photos/`.
They appear automatically in a 3-column grid on the Photography page — no code needed.

---

### CV

Replace `assets/Murari_Ganesan_CV.pdf` with your latest PDF (keep the same filename, or update `cv.html` if you rename it).

---

### Profile photo

Add your photo to `assets/img/profile.jpg`, then set in `_config.yml`:

```yaml
author:
  photo: /assets/img/profile.jpg
```

---

## Running locally (optional)

```bash
bundle install
bundle exec jekyll serve
```

Open [http://localhost:4000](http://localhost:4000).

Requires Ruby ≥ 2.7 and Bundler. GitHub Pages builds automatically without this step.

---

## Deploying

Push to the `master` branch of `muru825/muru825.github.io`.
GitHub Pages detects Jekyll and builds the site automatically — no CI needed.

---

## File structure

```
muru825.github.io/
├── _config.yml          ← site settings + your personal info
├── _data/
│   └── research.yml     ← add papers here
├── _layouts/
│   ├── default.html     ← shared nav + footer wrapper
│   └── post.html        ← blog post template
├── _posts/              ← blog posts (YYYY-MM-DD-title.md)
├── assets/
│   ├── css/main.css     ← all styles
│   ├── img/             ← profile photo goes here
│   ├── photos/          ← photography images go here
│   └── *.pdf            ← CV PDF goes here
├── index.html           ← homepage
├── research.html        ← research listing
├── photography.html     ← photo grid
├── blog.html            ← post listing
└── cv.html              ← CV embed + download
```
