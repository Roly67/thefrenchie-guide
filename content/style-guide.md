---
title: "Style Guide"
description: "Complete design system reference for The Frenchie Guide"
date: 2025-02-15
draft: true
---

# The Frenchie Guide Style Guide

This page demonstrates all design components and styles used across the site. Reference this when creating content.

---

## Typography Scale

# Heading 1 - Main Page Titles
## Heading 2 - Major Section Headers
### Heading 3 - Sub-sections
#### Heading 4 - Minor Sections
##### Heading 5 - Small Headings
###### Heading 6 - Smallest Headings

**Body text:** This is regular paragraph text. It uses Nunito Sans, a clean and highly readable typeface that pairs beautifully with our playful Outfit headings. Notice the warm, comfortable feel and generous line-height that makes reading a joy.

**Bold text** and *italic text* work as expected. You can also use ***bold italic*** for extra emphasis.

Small text can be useful for disclaimers and footnotes.

`Inline code` uses Space Mono for technical content.

---

## Colour Palette

Our colours are inspired by French Bulldogs themselves:

- **Fawn/Cream** - Primary background and warm accents
- **Slate Blue** - Like a blue Frenchie, used for links and key UI elements
- **Terracotta** - Rich brindle-inspired accent for CTAs
- **Warm Charcoal** - Deep, approachable text colour

Both light and dark modes are fully supported!

---

## Product Reviews

### Star Ratings

{{< star-rating score="5" >}}
{{< star-rating score="4.5" >}}
{{< star-rating score="4" >}}
{{< star-rating score="3.5" >}}
{{< star-rating score="3" >}}

### Tested Badge

{{< tested-badge >}}
{{< tested-badge text="Tested by Buster" >}}
{{< tested-badge text="Jago Approved" >}}

### Pros & Cons

{{< pros-cons 
  pros="Extremely comfortable,Breathable mesh design,Easy to put on,Machine washable,Great value for money" 
  cons="Limited colour options,Sizing runs slightly small,Not suitable for strong pullers" 
>}}

### Full Product Card

{{< product-card 
  name="Puppia Soft Harness" 
  image="/images/placeholder-product.jpg" 
  price="£24.99" 
  rating="4.5" 
  url="https://amazon.co.uk" 
  pros="Comfortable,Easy to put on,Breathable" 
  cons="Limited colours,Sizing runs small" 
>}}

{{< tested-badge >}}

We've been using the Puppia Soft Harness with Buster for over 6 months now, and it's become our go-to choice for daily walks. The soft mesh material doesn't irritate his sensitive skin, and the step-in design makes it quick to get ready for adventures.

**Best for:** Daily walks, small to medium Frenchies, sensitive skin

**Not ideal for:** Strong pullers, rough play, outdoor swimming

{{< /product-card >}}

---

## Callout Boxes

### Tips

{{< callout type="tip" title="Pro Tip" >}}
Always measure your Frenchie before ordering a harness online. Sizes can vary significantly between brands!
{{< /callout >}}

### Warnings

{{< callout type="warning" title="Important Warning" >}}
French Bulldogs are brachycephalic (flat-faced) and can overheat quickly. Never exercise them in hot weather and always have water available.
{{< /callout >}}

### Buster Says

{{< callout type="buster-says" title="Buster's Take" >}}
I absolutely LOVE this harness! It doesn't pull on my neck when I get excited about squirrels (which is often). Five paws up! 🐾
{{< /callout >}}

### Jago Says

{{< callout type="jago-says" title="Jago's Opinion" >}}
More treats, less walks. That's my motto. But if we must go out, at least make it comfortable!
{{< /callout >}}

### Vet Notes

{{< callout type="vet-note" title="Vet Advice" >}}
When choosing a harness for French Bulldogs, opt for H-style or step-in harnesses that distribute pressure across the chest rather than the neck. This is especially important for brachycephalic breeds.
{{< /callout >}}

---

## Affiliate Buttons

{{< affiliate-button url="https://amazon.co.uk" text="Check Price on Amazon" >}}

{{< affiliate-button url="https://example.com" text="View on Chewy" >}}

{{< affiliate-button url="https://example.com" text="Compare Prices" >}}

---

## Comparison Tables

{{< comparison-table >}}

| Feature | Puppia Soft | Ruffwear Front Range | Julius-K9 |
|---------|-------------|----------------------|-----------|
| **Price** | £24.99 | £39.99 | £32.99 |
| **Rating** | ⭐⭐⭐⭐½ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Material** | Mesh | Nylon | Nylon |
| **Breathability** | Excellent | Good | Fair |
| **Ease of Use** | Very Easy | Easy | Moderate |
| **Best For** | Daily walks | Active adventures | Working dogs |

{{< /comparison-table >}}

---

## Text Formatting

### Lists

Unordered lists:
- French Bulldogs are affectionate
- They love to play
- They make great apartment dogs
- They snore (a lot!)

Ordered lists:
1. Measure your dog's chest
2. Check the size chart
3. Order one size up if between sizes
4. Test the fit before removing tags

### Blockquotes

> "A house is not a home without a Frenchie."
> 
> — Every Frenchie parent ever

> **Editor's Note:** This is a longer blockquote example that demonstrates how multi-paragraph quotes look with our design system. Notice the warm accent border and comfortable spacing.

### Links

Regular links look like [this link to our homepage](/). They use our signature slate blue colour and have smooth hover transitions.

External links to [Amazon](https://amazon.co.uk) or other affiliate partners should use the affiliate button shortcode instead.

---

## Code Blocks

Inline code: `hugo server -D`

Code block:
```bash
# Build the site
hugo

# Run local development server
hugo server -D

# Clean build cache
hugo mod clean
```

---

## Images

Images should be descriptive, well-lit, and show French Bulldogs being their adorable selves.

![Placeholder image description](/images/placeholder.jpg)

Use `loading="lazy"` for all images below the fold.

---

## Email Signup

(This would be styled with the `.frenchie-signup` class when implemented)

```html
<div class="frenchie-signup">
  <h3>🐾 Get Frenchie Tips in Your Inbox</h3>
  <p>Join 5,000+ Frenchie parents getting weekly care tips, product reviews, and cute photos.</p>
  <form>
    <input type="email" placeholder="your@email.com" required>
    <button type="submit">Subscribe</button>
  </form>
  <p style="font-size: 0.875rem; margin-top: 1rem; opacity: 0.9;">No spam, just Frenchie goodness. Unsubscribe anytime.</p>
</div>
```

---

## Ad Placements

Ad zones are clearly defined but not intrusive:

<div class="frenchie-ad">
  Ad Placement Zone (300x250)
</div>

---

## Accessibility

All components meet WCAG AA standards:
- ✓ Sufficient colour contrast ratios
- ✓ Keyboard navigation support
- ✓ Screen reader friendly
- ✓ Reduced motion support for users who prefer it
- ✓ Focus indicators on all interactive elements

---

## Design Principles

When creating content, remember:

1. **Warm & Inviting** - Every element should feel friendly
2. **Rounded Corners** - Frenchies are round, our design should be too!
3. **Generous Spacing** - Let content breathe
4. **Subtle Playfulness** - Fun but not childish
5. **Mobile-First** - Most readers are on phones
6. **Fast Loading** - Minimal JS, CSS-only animations
7. **Make People Smile** - Like a Frenchie does! 🐶

---

*This style guide is a living document. Update it as new components are added.*
