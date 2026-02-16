# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Hugo static site for **The Frenchie Guide** — a French Bulldog affiliate content site. Uses the **PaperMod** theme (git submodule at `themes/PaperMod`). Deployed to GitHub Pages via GitHub Actions on push to `main`. Live at www.thefrenchieguide.com.

## Commands

```bash
# Dev server (includes drafts)
hugo server -D

# Dev server (published content only)
hugo server

# Production build
hugo --gc --minify

# Create new content
hugo new content/gear/article-slug.md
hugo new content/reviews/product-name.md

# Initialize theme submodule (required after fresh clone)
git submodule update --init --recursive
```

Hugo Extended is required (v0.139.4+). The CI uses v0.146.0.

## Architecture

### Content Sections

Content lives in `content/` with these sections: `gear/`, `nutrition/`, `training/`, `lifestyle/`, `breed/`, `reviews/`. Each section has an `_index.md` for the list page. Standalone pages: `about.md`, `privacy.md`, `affiliate-disclosure.md`, `start-here.md`, `style-guide.md` (draft).

### Front Matter Convention

Articles use YAML front matter with: `title`, `description`, `date`, `lastmod`, `draft`, `category`, `tags`, `author`, `featured_image`, `toc`, and an `seo.keywords` list. New articles start as `draft: true` (via `archetypes/default.md`).

### Theme Customization Layer

PaperMod is extended without modifying the theme itself:

- **`layouts/partials/extend_head.html`** — Google Analytics (gtag G-H6DZ5HX101), Google Fonts (Outfit, Nunito Sans, Space Mono), favicon links, Schema.org JSON-LD, OG/Twitter meta
- **`assets/css/extended/custom.css`** — Complete design system overriding PaperMod defaults. Defines CSS variables for the color palette (Slate Blue `#6B7C93` primary, Terracotta `#D17B5C` accent, Warm Cream `#FAF7F2` background) with automatic dark mode support
- **`layouts/shortcodes/`** — Custom shortcodes for affiliate content (see below)

### Custom Shortcodes

All defined in `layouts/shortcodes/`:

| Shortcode | Purpose | Key params |
|-----------|---------|------------|
| `product-card` | Product review card with rating | `name`, `image`, `price`, `rating`, `url`, `pros`, `cons` |
| `star-rating` | Star display | `score` |
| `tested-badge` | "Tested by Buster & Jago" trust badge | `text` (optional) |
| `pros-cons` | Pros/cons list | `pros`, `cons` (comma-separated) |
| `callout` | Info/warning box | `type` (`tip`, `warning`, `buster-says`, `jago-says`, `vet-note`), `title` |
| `affiliate-button` | CTA button with disclosure | `url`, `text` |
| `comparison-table` | Wraps a markdown comparison table | (inner content) |

### Images

Static images go in `static/images/{section}/` matching the content section name. Referenced in front matter as `featured_image: "/images/gear/filename.jpg"` and in markdown as standard paths.

### Deployment

Push to `main` triggers `.github/workflows/deploy.yml` which builds with Hugo Extended and deploys to GitHub Pages. The `static/CNAME` file maps to the custom domain.

## Writing Style

Content is written in a personal, British English voice — first-person plural ("we"), informal but knowledgeable. All product recommendations reference real testing with the author's French Bulldogs (Buster and Jago). UK pricing (GBP). Affiliate links must always use the `affiliate-button` shortcode for proper FTC/ASA disclosure.
