# The Frenchie Guide

**Real advice from real Frenchie parents. Product reviews, care guides, and tips for French Bulldog owners — tested by Buster & Jago.**

🌐 **Live site:** [thefrenchie-guide.com](https://thefrenchie-guide.com)  
📸 **Instagram:** [@thefrenchie.guide](https://instagram.com/thefrenchie.guide)  
👍 **Facebook:** [The Frenchie Guide](https://facebook.com/thefrenchie.guide)

## About This Project

This is a Hugo-based static site for The Frenchie Guide, an affiliate content site focused exclusively on French Bulldogs. The site features:

- **Product reviews** — Harnesses, food, toys, accessories, all tested by our Frenchies
- **Care guides** — Health, grooming, training, breed-specific advice
- **Honest recommendations** — We only recommend what we'd buy again
- **UK-based perspective** — But relevant worldwide

## Tech Stack

- **Static Site Generator:** [Hugo](https://gohugo.io) (v0.139.4)
- **Theme:** [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **Hosting:** GitHub Pages
- **Deployment:** GitHub Actions (auto-deploy on push to `main`)
- **Domain:** thefrenchie-guide.com

## Content Structure

```
content/
├── gear/               # Harnesses, collars, leads, beds, accessories
├── nutrition/          # Food, treats, supplements
├── training/           # Training guides, behavior tips
├── lifestyle/          # Health, grooming, care
├── breed/              # Breed info, history, characteristics
├── reviews/            # Product reviews
├── about.md            # About page
├── affiliate-disclosure.md  # FTC/ASA disclosure
├── privacy.md          # Privacy policy
└── start-here.md       # New visitor landing page
```

## Local Development

### Prerequisites

- Hugo Extended v0.139.4 or later ([installation guide](https://gohugo.io/installation/))
- Git

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Roly67/thefrenchie-guide.git
   cd thefrenchie-guide
   ```

2. **Initialize theme submodule** (if not already done):
   ```bash
   git submodule update --init --recursive
   ```

3. **Run the development server:**
   ```bash
   hugo server -D
   ```

4. **View the site:**
   Open [http://localhost:1313](http://localhost:1313) in your browser.

The `-D` flag includes draft posts. Remove it to see only published content.

### Creating New Content

**New article:**
```bash
hugo new content/gear/article-slug.md
```

**New review:**
```bash
hugo new content/reviews/product-name.md
```

Edit the frontmatter (title, description, date, categories, tags) and set `draft: false` when ready to publish.

## Deployment

The site automatically deploys to GitHub Pages via GitHub Actions when you push to the `main` branch.

**Workflow file:** `.github/workflows/deploy.yml`

### Manual Deploy

To build the site locally:

```bash
hugo --minify
```

The built site will be in the `public/` directory.

## Theme Customization

The site uses the [PaperMod theme](https://github.com/adityatelange/hugo-PaperMod) with custom configuration in `hugo.toml`.

### Key PaperMod Features Enabled:

- Search (Fuse.js)
- Reading time
- Share buttons
- Table of contents
- Breadcrumbs
- RSS feed
- Open Graph & Twitter Cards

### Customizing Layouts

To override theme layouts, create files in `layouts/` matching the theme structure. Example:

```
layouts/
└── partials/
    └── custom-footer.html
```

## SEO & Analytics

### Google Analytics
Add your GA4 Measurement ID to `hugo.toml`:

```toml
googleAnalytics = "G-MEASUREMENT_ID"
```

### AdSense
Configure AdSense in `hugo.toml` under `[params.adsense]`.

## Affiliate Links

This site earns from affiliate links (Amazon Associates, ShareASale, etc.). See [affiliate-disclosure.md](/content/affiliate-disclosure.md) for full transparency.

**Important:** Always disclose affiliate relationships per FTC/ASA guidelines.

## Contributing

This is a personal project, but suggestions are welcome! Feel free to:

- Open an issue for bugs or feature requests
- Submit a pull request for typo fixes

## License

Content: © 2026 The Frenchie Guide. All rights reserved.  
Code: MIT License (Hugo theme and build scripts)

## Contact

📧 Email: hello@thefrenchie-guide.com  
📸 Instagram: [@thefrenchie.guide](https://instagram.com/thefrenchie.guide)  
👍 Facebook: [The Frenchie Guide](https://facebook.com/thefrenchie.guide)

---

**Built with ❤️ (and lots of dog treats) in Cornwall, UK.**
