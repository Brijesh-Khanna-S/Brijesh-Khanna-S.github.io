# Brijesh & Monica — Wedding Invitation

A single-page animated wedding invitation hosted on GitHub Pages, shareable via WhatsApp.

**Live:** https://brijesh-khanna-s.github.io/Wedding_Invite/

---

## Events

| Event | Date | Time |
|---|---|---|
| Reception | 24 June 2026 | 7:30 PM |
| Wedding | 25 June 2026 | 9:30 AM |

**Venue:** Lindes Garden, Coimbatore, Tamil Nadu

---

## Features

- Spinning 3-layer botanical wreath with B & M initials
- Animated falling rose petals (Canvas, 65 petals)
- Full-height side vine borders with blooming flowers
- Animated top & bottom floral border bands
- 4 swaying corner floral branches
- Animated section dividers
- Event schedule cards with pulsing glow
- Google Maps "Get Directions" button
- Mobile-first, works on all screen sizes

---

## Tech

Single `index.html` — no build tools, no npm, no frameworks.

- HTML5 + CSS3 (keyframe animations)
- Canvas 2D API (petals, vines, border bands)
- Google Fonts (Cormorant Garamond + Jost)

---

## Customisation

All content is in `index.html`. To update:

- **Names / dates / venue** — search for the text and replace directly
- **Accent colour** — find `#b06070` and replace with your chosen colour
- **Personal message** — update the `.message-text` paragraph
- **Map link** — replace the `href` on `.map-btn`
