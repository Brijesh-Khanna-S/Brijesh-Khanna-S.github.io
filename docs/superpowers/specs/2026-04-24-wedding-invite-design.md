# Wedding Invite — Design Spec
**Date:** 2026-04-24  
**Project:** Brijesh & Monica Wedding Invitation  
**Hosting:** GitHub Pages (static, single `index.html`)

---

## Overview

A single-page scrollable wedding invitation website shared via WhatsApp link. Works on mobile and desktop browsers. No build tools, no npm, no external JS libraries — one `index.html` file with embedded CSS and vanilla JS Canvas animations.

**Only external dependency:** one Google Fonts `<link>` (Cormorant Garamond + Jost). Degrades gracefully to system serif if offline.

---

## Event Details

| Event | Date | Time |
|---|---|---|
| Reception | 24 June 2026 | 7:30 PM |
| Wedding | 25 June 2026 | 9:30 AM |

**Venue:** Lindes Garden, Coimbatore, Tamil Nadu  
**Map link:** https://maps.app.goo.gl/7ZRrLHDYwLgpE1vk7

---

## Visual Design

### Color Palette
| Role | Value |
|---|---|
| Accent / primary | `#b06070` (dusty rose) |
| Secondary floral | `#c9909a` |
| Petal light | `#e8b0bc` |
| Leaf / soft | `#d4a0a8` |
| Background | `#fdf8f5` (warm off-white) |
| Card | `#ffffff` |
| Border | `#ddd0c8` |

### Typography
- **Names & headings:** Cormorant Garamond (serif, weight 300/400, italic for ampersand)
- **Labels & UI:** Jost (sans-serif, weight 300/400)

### Layout
- Max-width: `480px`, centered, responsive
- Card has triple border: outer `1.5px`, inner `1px` at `inset:9px`, faint `0.5px` at `inset:16px`
- Page padding: `28px 16px 60px`

---

## Page Sections (top to bottom)

1. **Top border band** — animated canvas: wavy stem, 6-petal flowers every ~40px, leaves between, height 68px
2. **Hero** — eyebrow text, 3-layer spinning botanical wreath around "B & M" initials, couple names, tagline
3. **Floral divider** — animated SVG blooms on fading lines
4. **Personal message** — italic serif quote, signed "— Brijesh & Monica"
5. **Floral divider**
6. **Schedule** — two event cards (Reception / Wedding) with date number, month, event name, time; pulsing glow animation
7. **Floral divider**
8. **Venue** — Lindes Garden, city label, "Get Directions" button → Google Maps
9. **Bottom border band** — same as top band, flipped wave direction
10. **Footer** — "2026 · Brijesh & Monica"

**Persistent overlays (z-index above all):**
- Left & right side vines — full-height canvas: waving stem, 6-petal blooms every ~90px, alternating leaf pairs
- 4 corner florals — SVG botanical branches, independently swaying via CSS keyframes
- Falling petals — fixed-position canvas, 65 petals (3 shapes: oval, teardrop, round), dusty rose palette

---

## Animation Summary

| Element | Technique | Timing |
|---|---|---|
| Wreath outer ring | CSS `rotate` | 40s linear infinite |
| Wreath mid ring | CSS `rotate` reverse | 28s linear infinite |
| Wreath inner ring | CSS `rotate` | 20s linear infinite |
| Corner florals | CSS `rotate + scale` keyframes | 6–8s ease-in-out |
| Section divider blooms | CSS `scale + rotate` keyframes | 4–5.5s ease-in-out |
| Event card glow | CSS `box-shadow` keyframes | 5s, offset 2.5s |
| Side vines | requestAnimationFrame canvas | 60fps |
| Border bands | requestAnimationFrame canvas | 60fps |
| Falling petals | requestAnimationFrame canvas | 60fps |

---

## File Structure

```
Wedding_Invite/
├── index.html          ← entire site (HTML + CSS + JS inline)
└── .gitignore
```

No other files needed. GitHub Pages serves `index.html` from the `main` branch root.

---

## GitHub Pages Setup

1. Push `index.html` to `main` branch root
2. In repo Settings → Pages → Source: `main` branch, `/ (root)`
3. Share the `https://<username>.github.io/<repo>/` URL via WhatsApp

---

## Personal Message (default)

> "With hearts full of joy, we invite you to be part of our most cherished celebration. Your presence will make this day truly complete."
> — Brijesh & Monica
