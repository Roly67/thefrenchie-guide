# The Frenchie Guide - Design System Reference

## 🎨 Design Philosophy

Warm, playful, and inviting — like hanging out with your best Frenchie. Every element is designed to make you smile.

## Color Palette

### Light Mode
- **Primary:** Slate Blue (#6B7C93) - links, key UI elements
- **Accent:** Terracotta (#D17B5C) - CTAs, highlights
- **Background:** Warm Cream (#FAF7F2) - main background
- **Text:** Warm Charcoal (#2C2520) - body text

### Dark Mode
Automatically switches with user preference. Colors adjust to maintain warmth and readability.

## Typography

- **Headings:** Outfit (rounded, friendly, bold personality)
- **Body:** Nunito Sans (clean, highly readable, warm)
- **Monospace:** Space Mono (for technical content)

All fonts loaded from Google Fonts with optimal performance.

## Hugo Shortcodes

### Product Card
```hugo
{{</* product-card 
  name="Puppia Soft Harness" 
  image="/images/products/puppia.jpg" 
  price="£24.99" 
  rating="4.5" 
  url="https://amazon.co.uk/..." 
  pros="Comfortable,Easy to put on,Breathable" 
  cons="Limited colours,Sizing runs small" 
*/>}}
Your product review content here...
{{</* /product-card */>}}
```

### Star Rating
```hugo
{{</* star-rating score="4.5" */>}}
```

### Tested Badge
```hugo
{{</* tested-badge */>}}
{{</* tested-badge text="Buster Approved" */>}}
```

### Pros & Cons
```hugo
{{</* pros-cons 
  pros="Durable,Comfortable,Great value" 
  cons="Runs small,Limited colors" 
*/>}}
```

### Callout Boxes
```hugo
{{</* callout type="tip" title="Pro Tip" */>}}
Content here
{{</* /callout */>}}
```

Types: `tip`, `warning`, `buster-says`, `jago-says`, `vet-note`

### Affiliate Button
```hugo
{{</* affiliate-button url="https://..." text="Check Price on Amazon" */>}}
```

### Comparison Table
```hugo
{{</* comparison-table */>}}
| Feature | Product A | Product B |
|---------|-----------|-----------|
| Price   | £29.99    | £34.99    |
| Rating  | ⭐⭐⭐⭐⭐    | ⭐⭐⭐⭐     |
{{</* /comparison-table */>}}
```

## Key Features

### 🎯 Affiliate-Optimized
- Eye-catching CTA buttons with proper disclosure
- Product cards with star ratings
- Comparison tables for side-by-side reviews
- "Tested by Buster & Jago" trust badges

### 📱 Mobile-First
- Responsive grid layouts
- Touch-friendly buttons and links
- Optimized typography scaling
- Fast, lightweight CSS

### ♿ Accessible
- WCAG AA contrast ratios
- Semantic HTML
- Keyboard navigation support
- Screen reader friendly
- Respects prefers-reduced-motion

### 🎬 Subtle Animations
- Card hover effects
- Button transitions
- Smooth scrolling
- Fade-in on scroll (when appropriate)

### 🎨 Consistent Styling
- Rounded corners everywhere (Frenchies are round!)
- Generous spacing
- Cohesive color system
- Dark mode support

## Files Created

### CSS
- `assets/css/extended/custom.css` - Complete design system (19KB)

### Partials
- `layouts/partials/extend_head.html` - Google Fonts + meta tags
- `layouts/partials/star-rating.html` - Reusable star rating partial

### Shortcodes
- `layouts/shortcodes/product-card.html`
- `layouts/shortcodes/star-rating.html`
- `layouts/shortcodes/tested-badge.html`
- `layouts/shortcodes/pros-cons.html`
- `layouts/shortcodes/callout.html`
- `layouts/shortcodes/affiliate-button.html`
- `layouts/shortcodes/comparison-table.html`

### Documentation
- `content/style-guide.md` - Complete component showcase (draft)
- `DESIGN-SYSTEM.md` - This reference guide

### Configuration
- Updated `hugo.toml` with design system parameters

## Usage Tips

1. **View the style guide:** `hugo server -D` and navigate to `/style-guide/`
2. **All images** should use descriptive alt text
3. **Product images** should be optimized and use lazy loading
4. **Affiliate links** should always use the affiliate-button shortcode for proper disclosure
5. **Reviews** should include the tested-badge for credibility

## Next Steps

- Add favicon files to `/static/`
- Create product image placeholders
- Set up email signup form integration
- Configure AdSense ad units
- Add more product reviews using the new components!

---

Built with ❤️ and 🐾 for Frenchie parents everywhere.
