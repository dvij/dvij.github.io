# dvij.github.io — Blog Setup

This directory contains the Quarto-powered blog that lives at `dvij.github.io/blog`.

## Structure

```
blog/
├── _quarto.yml          # Quarto project config (theme, KaTeX, TOC, etc.)
├── index.qmd            # Blog listing page
├── _assets/
│   └── custom.scss      # Typography, math, dark mode styles
└── posts/
    ├── tractable-qcqps/
    │   └── index.qmd    # Post: A Map of Tractable QCQPs
    └── vibe-coding-reliability/
        └── index.qmd    # Post: The Intent Gap
.github/
└── workflows/
    └── blog.yml         # Auto-build + deploy on push to main
```

## Local Development

1. **Install Quarto**: https://quarto.org/docs/get-started/

2. **Preview locally:**
   ```bash
   cd blog
   quarto preview
   ```
   Opens a live-reloading browser at `localhost:4848/blog/`

3. **Render to static HTML:**
   ```bash
   quarto render blog/
   ```
   Output goes to `docs/blog/` (served by GitHub Pages).

## Adding a New Post

```bash
mkdir blog/posts/my-new-post
```

Create `blog/posts/my-new-post/index.qmd` with this front matter:

```yaml
---
title: "Your Post Title"
description: "One sentence summary shown in listing."
date: 2026-03-15
author: "Dj"
categories: [optimization, AI]   # pick from existing or add new
toc: true
---
```

Then write in Markdown with full KaTeX math support:

- Inline math: `$x^\top A x$`
- Display math: `$$\min_{x} f(x) \text{ s.t. } g(x) \leq 0$$`
- Code blocks: standard fenced blocks with language tag
- Callouts: `::: {.callout-note}` / `.callout-important` / `.callout-tip`

## GitHub Pages Setup

Ensure GitHub Pages is configured in your repo settings:
- **Source**: Deploy from branch `gh-pages`
- **Directory**: `/ (root)`

The workflow in `.github/workflows/blog.yml` handles everything on push to `main`.

## Math Tips

KaTeX is fast but has slightly less coverage than MathJax. For edge cases:
- Use `\operatorname{rank}` not `\rank`
- Matrices: `\begin{pmatrix}...\end{pmatrix}`
- For very complex displays, consider rendering as SVG and embedding as image
