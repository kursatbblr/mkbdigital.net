# Odakla — "Warm Focus" Design Brief

> Not purple SaaS. Not cold tech. A warm, human-centered focus timer landing page.

---

## Concept

**"Warm Focus"** — a design language that feels calm, grounded, and inviting. No generic AI-site aesthetics (mesh gradients, neon purple, glassmorphism overdose). Instead: a dark canvas with a single warm light source — like a desk lamp in a quiet room.

---

## Color Palette

| Role | Value | Usage |
|------|-------|-------|
| Background | `#0D0D18` | Deep dark canvas |
| Text | `#ECE4D9` | Warm off-white, not stark |
| Muted | `#8A7E6E` | Warm gray, readable but soft |
| CTA | `#E07040` | Terracotta-orange, the warmest touch |
| CTA hover | `#C85A2A` | Deeper burned orange |
| Surface | `rgba(255,255,255,0.04)` | Subtle card backgrounds |
| Border | `rgba(255,255,255,0.07)` | Barely-there separators |
| Glow | `rgba(224,112,64,0.12)` | Hero ambient light |

---

## Typography

**Nunito** (Google Fonts, weights: 500–900)

- Rounded, friendly, approachable — the opposite of Inter/Roboto
- No system-ui fallback look; intentionally warm
- Large hero title at `clamp(2.2rem, 6vw, 4.2rem)` with tight line-height for impact
- Body text stays at readable sizes, never under 0.92rem

---

## Logo Mark

A custom SVG built from concentric rings + a clock hand:

- Three translucent circles suggesting focus rings / ripples
- A solid center dot (the point of focus)
- A single line from center to top (timer hand at 12 o'clock)
- Warm terracotta color, subtle pulse animation (4s ease-in-out)

No text in the mark — the brand name "Odakla" doesn't appear as a wordmark. The symbol carries the meaning alone.

---

## Layout

```
┌─────────────────────────────────┐
│  ← MKB Digital (back link)      │
├─────────────────────────────────┤
│                                 │
│           ◉ (logo mark)         │
│                                 │
│     Warm focus,                 │
│     simple rhythm.              │
│                                 │
│     Pomodoro timer. Task list.  │
│     Daily flow. A calmer route  │
│     into deep work.             │
│                                 │
│        [Try on Google Play]     │
│                                 │
│       ~ ambient glow behind ~   │
├─────────────────────────────────┤
│  ┌─────────┐┌─────────┐┌──────┐│
│  │ Focus   ││ Task    ││Daily ││
│  │ timer   ││ flow    ││rhythm││
│  └─────────┘└─────────┘└──────┘│
├─────────────────────────────────┤
│  Free. Simple. Built to focus.  │
│        [Try on Google Play]     │
├─────────────────────────────────┤
│  © 2026  Privacy  Contact  ← MKBD│
└─────────────────────────────────┘
```

---

## Anti-Patterns (deliberately avoided)

- **No purple gradients** — the default AI aesthetic
- **No glassmorphism cards** — overused, feels generic
- **No mesh/blobby backgrounds** — another AI tell
- **No system fonts** — Inter/Roboto/SF Pro feel corporate
- **No animated counters or flashy reveals** — calm, not busy
- **No dark-mode toggle** — the page *is* dark mode, intentionally warm

---

## Motion

- Logo mark: subtle 4s breathe/pulse (`scale 1 → 1.04`)
- CTA hover: gentle lift (`translateY(-1px)`) + glow intensify
- Feature cards: border color shifts to warm on hover
- No scroll-triggered animations — keeps the page feeling quiet

---

## Page: `odakla/index.html`

- **Hero**: Logo centered, two-line title, short description, CTA
- **Features**: 3-column grid, icon + title + one-sentence description each
- **Bottom CTA**: Centered callout band, single line + button
- **Footer**: Minimal — privacy, contact, back link

---

## Files

| File | Purpose |
|------|---------|
| `odakla/index.html` | Landing page |
| `odakla/privacy.html` | Privacy policy (existing) |
| `odakla/DESIGN.md` | This document |
| `styles.css` (bottom) | All `.odakla-landing` scoped styles |
| `index.html` (main) | Studio row links to `/odakla` |
| `vercel.json` | Route `/odakla` → `/odakla/index.html` |
