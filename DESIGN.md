---
name: ASAP — Platform Design System
version: 2.0
description: Brand and design system for the ASAP platform and its three Genie products. Use this file as the single source of truth for any design or implementation task across asapgenie.com, Zone Genie, Site Genie, and Fence Genie.
---

# ASAP Platform Design System

## 0. How to Read This File

This document has two layers:

1. **Platform layer** — ASAP brand tokens, typography, spacing, and component rules that apply to the main website (asapgenie.com) and any cross-product surface.
2. **Product layer** — Per-product brand identities for Zone Genie, Site Genie, and Fence Genie. Each product has its own color system that lives within the platform frame.

When building for the **platform website**: use platform tokens. When building for a **product-specific surface** (a product's own app, landing page, or marketing material): use that product's tokens.

---

## 1. Platform Brand — ASAP

### Creative North Star

"Spatial Clarity." ASAP takes something dense and civic — zoning codes, permit workflows, parcel data — and renders it with the calm confidence of a system that has already done the hard work. Every surface should feel like the answer has been found; the user is just reading it.

The platform aesthetic is **dark-first, editorial, restrained**. Reference: x.ai — large type does the work, no decorative fills, no gradient cards. Serious, modern, unhurried.

### Personality

Approachable, Modern, Civic. Voice is confident but never arrogant. Clear without clinical. Expert, warm, direct. Talks to smart, busy people — no jargon, no fluff. Feels like a modern SaaS company that genuinely understands local government.

### Platform Audience (Primary)

Municipal decision-makers: Zoning Administrators, Planning Directors, Building Officials, City Managers at cities 50K–300K population. Time-pressured, accountable, skeptical of technology that overpromises. They need to trust before they demo.

---

## 2. Platform Color Tokens

### Dark Surface System (asapgenie.com)

```
--bg-base:     #080f1a   ← page background
--bg-surface:  #0a1628   ← slightly elevated sections (validation, alternating)
--bg-elevated: #0f2b4a   ← nav scrolled, modals, tooltips
--bg-card:     #0d1f38   ← card default state
```

### Text

```
--text-primary:   #e8f0f4                     ← headings, primary body
--text-secondary: rgba(232,240,244,0.58)      ← supporting copy
--text-tertiary:  rgba(232,240,244,0.32)      ← captions, disabled, labels
```

### Platform Accent (Teal — aligned with Zone Genie flagship)

```
--accent:        #3db5a6
--accent-dim:    #2a8a7e
--accent-glow:   rgba(61,181,166,0.10)
--accent-border: rgba(61,181,166,0.20)
```

### Borders

```
--border:        rgba(255,255,255,0.07)
--border-light:  rgba(255,255,255,0.11)
```

### Shadow Rule

All box-shadows use `rgba(15,43,74,…)` — the Deep Civic Navy — not `rgba(0,0,0,…)`. Keeps elevation in the brand palette.

```
Shadow SM:  0 1px 3px rgba(15,43,74,0.08)
Shadow MD:  0 4px 16px rgba(15,43,74,0.10)
Shadow LG:  0 12px 40px rgba(15,43,74,0.14)
```

---

## 3. Product Brand Identities

Each product has:
- A **primary color** (the dominant brand hue)
- A **secondary color** where applicable (dual-color brands)
- **Logo extraction** — exact hues pulled from the official logo
- **Dark surface tokens** — how the brand renders on the dark platform website
- **Light surface tokens** — how the brand renders on its own light-background surfaces (product apps, marketing)

---

### 3A. Zone Genie — Flagship

**Status:** Live in production  
**Audience:** Municipal planning departments  
**Tagline:** Modernizing Zoning & Permit Review

#### Brand Character
The civic authority product. Calm, structured, trustworthy. The ASAP platform accent teal IS the Zone Genie color — they share identity because Zone Genie is the flagship that established the platform.

#### Logo Colors (extracted from official logo)
```
Wordmark:         #162060   ← deep navy
Lamp body dark:   #1a2870   ← gradient start
Lamp body light:  #00c8e8   ← gradient end, bright cyan genie tail
Tagline:          #00b8d4   ← mid cyan
```

#### Platform (Dark Surface) Tokens
```css
--color-zg:           #3db5a6
--color-zg-border:    rgba(61,181,166,0.28)
--color-zg-bg:        rgba(61,181,166,0.06)
--color-zg-mark-from: #061e20
--color-zg-mark-to:   #0d4840
```

#### Suite Card Mark
- Background: `linear-gradient(135deg, #061e20, #0d4840)`
- Text/icon color: `#3db5a6`
- Border: `1px solid rgba(61,181,166,0.20)`

#### Light Surface Palette (product app, dedicated landing page)
```
Primary:    #3db5a6   ← teal CTA buttons, active states
Dark:       #162060   ← headings, heavy UI chrome (matches logo navy)
Mid:        #1e5a8a   ← secondary surfaces
Accent:     #00c8e8   ← highlights, data callouts, active badges
Background: #f0f9f8   ← page background (very light teal tint)
Text:       #1e2e34   ← body copy (teal-tinted near-black)
```

---

### 3B. Site Genie — Pipeline

**Status:** Coming Soon  
**Audience:** Real estate developers, acquisitions teams, site selection consultants  
**Tagline:** Smarter Site Selection for Developers

#### Brand Character
The opportunity-finding product. Fresh, growth-oriented, analytical. Green signals land, nature, growth, and go — a natural choice for a product about finding what's buildable. Brighter and more energetic than Zone Genie's civic restraint.

#### Logo Colors (extracted from official logo)
```
Wordmark "Site":  #1a5a22   ← dark forest green
Wordmark "Genie": #1a5a22   ← same dark forest green
Lamp body dark:   #1a5a22   ← gradient start
Lamp body light:  #78c820   ← gradient end, lime genie tail
Tagline:          #6abf20   ← bright lime green
```

#### Platform (Dark Surface) Tokens
```css
--color-sg:           #5ec42a
--color-sg-border:    rgba(94,196,42,0.28)
--color-sg-bg:        rgba(94,196,42,0.06)
--color-sg-mark-from: #0c1e06
--color-sg-mark-to:   #1c4208
```

#### Suite Card Mark
- Background: `linear-gradient(135deg, #0c1e06, #1c4208)`
- Text/icon color: `#5ec42a`
- Border: `1px solid rgba(94,196,42,0.20)`

#### Light Surface Palette (product app, dedicated landing page)
```
Primary:    #5ec42a   ← CTA buttons, active states, progress indicators
Dark:       #1a5a22   ← headings (matches logo dark green)
Mid:        #2d8a38   ← secondary UI surfaces
Accent:     #78c820   ← highlights, data callouts
Background: #f2f9f0   ← page background (very light green tint)
Text:       #1a2e1c   ← body copy (green-tinted near-black)
```

---

### 3C. Fence Genie — Pipeline

**Status:** Live (fence-site-plan.web.app) — ASAP website treats as pipeline  
**Audience:** Homeowners, fencing contractors, DIY permit applicants  
**Tagline:** Smarter Fence Plans. Faster Approvals.

#### Brand Character
The most approachable product. Homeowner-facing, friendly, practical. The dual-color identity (orange + teal) reflects the two-part brand: "Fence" (the orange, warm, residential) and "Genie" (the teal, the AI magic). Orange is the lead differentiator — it's what makes Fence Genie distinct from the teal-dominant ASAP family.

#### Logo Colors (extracted from official logo)
```
Wordmark "Fence": #d4831c   ← warm orange/amber — PRIMARY DIFFERENTIATOR
Wordmark "Genie": #1a5a6b   ← deep teal
Lamp body dark:   #1a5a6b   ← gradient start (teal)
Lamp body light:  #3bb8c8   ← gradient end (bright teal genie tail)
Flame:            #d4831c   ← orange, matches "Fence" wordmark
Tagline:          #3aa8b8   ← medium teal
```

#### Platform (Dark Surface) Tokens
```css
--color-fg:           #d4831c
--color-fg-border:    rgba(212,131,28,0.28)
--color-fg-bg:        rgba(212,131,28,0.06)
--color-fg-mark-from: #1e0e00
--color-fg-mark-to:   #4a2600
--color-fg-secondary: #1a5a6b   ← use for secondary accents, not primary
```

#### Suite Card Mark
- Background: `linear-gradient(135deg, #1e0e00, #4a2600)`
- Text/icon color: `#d4831c`
- Border: `1px solid rgba(212,131,28,0.20)`

#### Light Surface Palette (product app, dedicated landing page)
```
Primary:    #d4831c   ← CTA buttons, active states, key highlights
Dark:       #1a5a6b   ← headings (matches "Genie" teal from logo)
Mid:        #2a8a9a   ← secondary UI surfaces, borders
Accent:     #3bb8c8   ← data callouts, lamp/magic motifs
Background: #fdf6ef   ← page background (very light warm tint)
Text:       #2a1e14   ← body copy (warm-tinted near-black)
```

---

## 4. Product Color Quick Reference

| Product | Primary | Dark (wordmark) | Accent (lamp tail) | Status |
|---|---|---|---|---|
| Zone Genie | `#3db5a6` teal | `#162060` navy | `#00c8e8` cyan | Live |
| Site Genie | `#5ec42a` lime | `#1a5a22` forest | `#78c820` lime | Pipeline |
| Fence Genie | `#d4831c` orange | `#1a5a6b` teal | `#3bb8c8` bright teal | Pipeline |

**Rule:** On the dark platform website, only the Primary column is used (as the mark color and hover accent). On light product surfaces, use the full per-product palette.

---

## 5. Typography

### Font Families

```
Display / Headings (h1–h3, brand marks): Space Grotesk — weights 500/600/700
Body / UI (everything else): Inter — weights 400/500/600
```

**The Two-Font Rule.** Space Grotesk for headings and the footer brand mark only. Inter for body, labels, buttons, form fields, nav links. Never swap them.

**Note for new product surfaces:** Space Grotesk and Inter are the established ASAP system fonts. Product-specific landing pages should use this pairing for consistency. Do not introduce new typefaces without a documented brand reason.

### Scale

```
Display:  Space Grotesk 700, clamp(2.4rem, 5vw, 3.6rem), lh 1.15, ls -0.02em
          → Hero h1 only. One per page. Negative tracking for editorial confidence.

Headline: Space Grotesk 700, clamp(1.8rem, 3.5vw, 2.6rem), lh 1.15
          → Section h2. One per section.

Title:    Space Grotesk 600, clamp(1.2rem, 2vw, 1.5rem), lh 1.3
          → Card h3, step headings.

Body:     Inter 400, 1rem, lh 1.6, max 65ch
          → All paragraph text.

Label:    Inter 600, 0.8rem, ls 0.12em, UPPERCASE
          → Section eyebrows only. One per section maximum.
          → Teal Light on dark, Civic Teal on light.
```

---

## 6. Spacing & Layout

```
--section-pad: clamp(80px, 10vw, 140px)   ← full sections top/bottom
--container:   1160px                      ← max content width
--gutter:      clamp(20px, 5vw, 48px)      ← horizontal padding
```

**Section rhythm rule:** Adjacent section edges that share a background change may use `clamp(48px, 6vw, 80px)` on the touching side to reduce dead space. Full `--section-pad` applies when sections share the same background.

### Rounded Corners
```
sm:   8px    ← inputs, small badges
md:   12px   ← feature cards, table containers
lg:   20px   ← benefit tiles, larger containers
pill: 50px   ← all buttons (brand choice, not default)
```

---

## 7. Components

### Buttons

All buttons are pill-shaped (50px border-radius). This is a deliberate brand decision — not a framework default.

```
Primary (on dark):     White fill #ffffff, Deep Navy text #0f2b4a
                       Shadow: 0 4px 20px rgba(255,255,255,0.25)
                       → Use on hero sections only

Teal/Brand (on light): Gradient fill 135deg #0f2b4a→#3db5a6, white text
                       Shadow MD at rest, Shadow LG on hover
                       → Primary CTA on light sections

Secondary (on dark):   Transparent fill, white text, 2px solid rgba(255,255,255,0.4)

Outline (on light):    Transparent fill, navy text, 2px solid #dce4e4
                       Hover: border and text shift to Civic Teal

Hover:  translateY(-2px) + Shadow LG — guard with @media (hover: hover) and (pointer: fine)
Active: scale(0.97) — apply to every button and pressable element
```

### Cards

```
Feature Card:    12px radius, white bg, 1px solid #dce4e4 border, 32px 24px padding
                 Hover: translateY(-4px) + Shadow LG + Teal Light border

Benefit Tile:    20px radius, #f8fafa bg, no border
                 Hover: white bg + Shadow LG + translateY(-4px)

Dark Gradient:   20px radius, 160deg #163d64→#1e5a8a gradient, white text
                 → Problem visuals, platform feature pills

Suite Card:      16px radius, var(--bg-card) bg, 1px solid var(--border)
                 Active product: teal-tinted bg gradient, product-color border
                 Pipeline: 0.55 opacity, lifts to 0.75 on hover
```

**Nested cards are prohibited.** Cards never appear inside other cards.

### Suite Card Marks (Product Logos)

The 52×52px product logo mark in the top-left of each suite card:

```
Zone Genie:  bg linear-gradient(135deg, #061e20, #0d4840)
             text/icon #3db5a6, border 1px solid rgba(61,181,166,0.20)

Site Genie:  bg linear-gradient(135deg, #0c1e06, #1c4208)
             text/icon #5ec42a, border 1px solid rgba(94,196,42,0.20)

Fence Genie: bg linear-gradient(135deg, #1e0e00, #4a2600)
             text/icon #d4831c, border 1px solid rgba(212,131,28,0.20)
```

When product logo image files are available (transparent background PNG/SVG), replace the letter marks with `<img>` elements inside the mark container, using `mix-blend-mode: screen` if logos have white backgrounds.

### Navigation

```
Default:   Transparent bg, 12px padding. Logo: inline SVG globe + "ASAP" in Space Grotesk 700.
           Links: rgba(255,255,255,0.8), Inter 0.9rem 500.

Scrolled:  rgba(15,43,74,0.95) + backdrop-filter: blur(20px), 8px padding.
           Transition: background-color, box-shadow, padding only — never transition: all.

CTA pill:  rgba(255,255,255,0.15) bg, 1px white-tinted border.
```

### Form Fields

```
Radius:      8px
Border:      1px solid rgba(255,255,255,0.2)
Background:  rgba(255,255,255,0.06)
Focus:       Border shifts to #3db5a6, no glow
Placeholder: rgba(255,255,255,0.35)
```

---

## 8. Animation & Motion

### Hero Entrance (above-fold, fires on page load)

```css
@keyframes heroFadeUp {
  from { opacity: 0; transform: translateY(14px); }
  to   { opacity: 1; transform: translateY(0); }
}
.hero-enter { animation: heroFadeUp 500ms cubic-bezier(0.23,1,0.32,1) both; }
```

Stagger delays: 0ms, 80ms, 160ms, 240ms, 320ms per element.  
**Do not use IntersectionObserver for above-fold hero content.** It is unreliable on initial load.

### Scroll-Triggered (below fold)

```css
.fade-up { opacity: 0; transform: translateY(12px);
           transition: opacity 400ms, transform 400ms; }
.fade-up.visible { opacity: 1; transform: translateY(0); }
```

IntersectionObserver threshold: 0.08. 12px vertical travel only — the fade carries the weight.

### Easing Curves

```
--ease-out:    cubic-bezier(0.23, 1, 0.32, 1)    ← UI interactions entering
--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1)   ← on-screen movement
```

### Rules

- Never `transition: all` — specify exact properties (transform, box-shadow, border-color, opacity)
- Guard every hover transform with `@media (hover: hover) and (pointer: fine)`
- Always include `prefers-reduced-motion` — strip transforms, keep opacity fades
- Add `:active { transform: scale(0.97) }` to every button and pressable element
- Hover transforms: `translateY(-2px)` for cards, `translateY(-3px)` for suite cards

---

## 9. The Brand Gradient

```
135deg, #0f2b4a → #1e5a8a → #2a8a7e → #3db5a6
```

**Reserved for:** Hero sections, How It Works sections, and final CTA sections only.  
**Never use on:** Cards, sidebars, badges, or secondary elements.  
This gradient marks the most important conversion surfaces — applying it elsewhere dilutes that signal.

---

## 10. Platform Do's and Don'ts

### Do

- Use Space Grotesk exclusively for h1–h3 and the footer brand mark; Inter for everything else
- Keep section padding at `clamp(80px, 10vw, 140px)` on desktop. Generous rhythm is intentional
- Use tinted shadows `rgba(15,43,74,…)` on every box-shadow — never `rgba(0,0,0,…)`
- Guard every hover transform with `@media (hover: hover) and (pointer: fine)`
- Specify exact CSS properties in transitions. Never `transition: all`
- Add `:active { transform: scale(0.97) }` to every button and submit element
- Use `prefers-reduced-motion` — strip transforms, keep opacity fades
- Use WCAG 2.1 AA contrast on all text. Test both light and dark surfaces
- On the dark site: use per-product color tokens for suite card marks and hover borders

### Don't

- Don't use generic govtech patterns — stock city hall photography, "citizen-centric solutions" language, institutional serifs. If it looks like a .gov portal, rework it.
- Don't use the SaaS-cream look — off-white/beige, rounded purple accents, generic AI marketing cards
- Don't place the brand gradient on cards, sidebars, or secondary elements
- Don't use hero-metric templates — big number, small label, supporting stat. PRODUCT.md prohibits this
- Don't use identical card grids — vary structure between feature cards and benefit tiles
- Don't use black shadows `rgba(0,0,0,…)` — every shadow uses the navy tint
- Don't nest cards inside cards
- Don't use gradient text (`background-clip: text`) — solid color for all text
- Don't use border-left stripe accents greater than 1px
- Don't animate on keyboard-triggered actions or high-frequency interactions
- Don't let pipeline products (Site Genie, Fence Genie) compete visually with Zone Genie on the platform site — keep them at 55% opacity, lift on hover

---

## 11. Anti-References

These are explicitly banned aesthetics for all ASAP and Genie surfaces:

- **Generic govtech** — city hall stock photos, blue gradients, "citizen-centric solutions," slow institutional design
- **SaaS-cream AI startup** — off-white/beige + rounded cards + purple accent. Overused, undifferentiated
- **Dashboard screenshot hero** — cluttered UI fills trying to prove sophistication through complexity
- **Hero-metric template** — big number, small label, supporting stat. SaaS cliché, especially harmful for government trust audiences

---

## 12. File Structure Reference

```
ASAP WEBSITE/
├── index.html              ← Platform homepage (dark-first, Zone Genie lead)
├── DESIGN.md               ← This file
├── PRODUCT.md              ← Audience, positioning, brand personality
├── asap-logo-white.svg     ← ASAP wordmark (white version — legacy, has dark fills, avoid)
├── asap-globe.svg          ← Globe mark asset
├── zone-genie-logo.png     ← Zone Genie logo (white background — use mix-blend-mode: screen on dark)
├── logo-1.svg              ← Site Genie or Fence Genie logo (confirm identity before use)
└── logo-2.svg              ← Site Genie or Fence Genie logo (confirm identity before use)
```

**Logo background note:** All current logo files have white backgrounds. On dark surfaces, use `mix-blend-mode: screen` to eliminate the white bg and show only the colored illustration. On light surfaces, use as-is.

---

## 13. CSS Variable Reference (asapgenie.com)

```css
:root {
  /* Platform surfaces */
  --bg-base:     #080f1a;
  --bg-surface:  #0a1628;
  --bg-elevated: #0f2b4a;
  --bg-card:     #0d1f38;

  /* Text */
  --text-primary:   #e8f0f4;
  --text-secondary: rgba(232,240,244,0.58);
  --text-tertiary:  rgba(232,240,244,0.32);

  /* Platform accent */
  --accent:        #3db5a6;
  --accent-dim:    #2a8a7e;
  --accent-glow:   rgba(61,181,166,0.10);
  --accent-border: rgba(61,181,166,0.20);

  /* Borders */
  --border:        rgba(255,255,255,0.07);
  --border-light:  rgba(255,255,255,0.11);

  /* Zone Genie */
  --color-zg:        #3db5a6;
  --color-zg-border: rgba(61,181,166,0.28);
  --color-zg-bg:     rgba(61,181,166,0.06);

  /* Site Genie */
  --color-sg:        #5ec42a;
  --color-sg-border: rgba(94,196,42,0.28);
  --color-sg-bg:     rgba(94,196,42,0.06);

  /* Fence Genie */
  --color-fg:        #d4831c;
  --color-fg-border: rgba(212,131,28,0.28);
  --color-fg-bg:     rgba(212,131,28,0.06);

  /* Fonts */
  --font-display: 'Space Grotesk', sans-serif;
  --font-body:    'Inter', sans-serif;

  /* Easing */
  --ease-out:    cubic-bezier(0.23, 1, 0.32, 1);
  --ease-in-out: cubic-bezier(0.77, 0, 0.175, 1);

  /* Layout */
  --section-pad: clamp(80px, 10vw, 140px);
  --container:   1160px;
  --gutter:      clamp(20px, 5vw, 48px);
}
```
