# The Elite Architect — Design System

## Overview

This design system positions Ruzzel Maestro as a high-tier consultant and architect in business process automation and AI integration.

**Creative North Star:** "The Elite Architect of Automation"

## Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Background | #0A0A0A | Main page background |
| Surface | #131313 | Primary surfaces |
| Surface Container | #201F1F | Cards and elevated content |
| Surface Container Low | #1C1B1B | Inset content within cards |
| Surface Container Highest | #353534 | Floating elements, active states |
| Primary (Maroon) | #800000 | Primary accent, CTAs, highlights |
| Primary Light | #FF6B6B | Active states, hover effects |
| Text Primary | #E5E2E1 | Main text, nav |
| Text Secondary | #E2BFB9 | Secondary text |

## Typography

### Headings
- **Font:** Inter Bold
- **Weight:** 700–900
- **Letter-spacing:** -0.02em (tight)
- **Sizes:** 
  - Display LG: 3.5rem
  - Headline LG: 2rem
  - Headline MD: 1.5rem

### Body
- **Font:** Inter
- **Weight:** 400
- **Line-height:** 1.6–1.75
- **Size:** 1rem

### Labels
- **Font:** Space Grotesk
- **Weight:** 400–500
- **Size:** 0.875rem
- **Text-transform:** Uppercase

## Components

### Buttons
- **Primary:** Background #800000, text white, sharp corners (0px)
- **Secondary:** Border #5A413D, text #E5E2E1, sharp corners
- **Hover:** Add glow `0 0 20px rgba(128,0,0,0.6)`

### Navigation
- **Active state:** Text and underline #E5E2E1 (light gray)
- **Inactive:** Text #E5E2E1 (same for consistency)
- **Background:** Transparent, gains backdrop-blur on scroll

### Cards
- **Background:** #201F1F
- **Borders:** None (use tonal shifts instead)
- **Spacing:** Generous padding (2–3rem)

## Principles

1. **No 1px borders** — use background color shifts to define boundaries
2. **Sharp corners** — all elements have 0px border-radius
3. **Monochromatic** — keep UI 90% neutral, use maroon sparingly
4. **Generous whitespace** — luxury is empty space
5. **Intentional asymmetry** — avoid rigid 12-column grids

## Font Rendering

Applied across all elements:
- `-webkit-font-smoothing: antialiased`
- `-moz-osx-font-smoothing: grayscale`
- `text-rendering: optimizeLegibility`
- `font-feature-settings: "kern" 1`

## Spacing Scale

Base unit: 12px
- xs: 0.25rem (3px)
- sm: 0.5rem (6px)
- md: 1rem (12px)
- lg: 1.5rem (18px)
- xl: 2rem (24px)
- 2xl: 3rem (36px)
- 3xl: 4rem (48px)

## Animations

- **Scroll triggers:** Subtle fade-in and slide-up
- **Hover states:** Smooth transitions (200ms)
- **No layout-shifting animations** — use transform and opacity only

## Version

Design System v1.0 — March 2026
