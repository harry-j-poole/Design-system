---
name: Harry Poole Portfolio
description: Personal portfolio design system for a senior UX/UI Product Designer. Clean, minimal, and professional — communicating clarity of thought and design craft.
colors:
  primary: "#1A1A1A"
  secondary: "#555555"
  accent: "#2563EB"
  surface: "#f9f9f1"
  surface-subtle: "#F7F7F7"
  border: "#E5E5E5"
  on-surface: "#1A1A1A"
  on-surface-muted: "#6B7280"
typography:
  display:
    fontFamily: Space Grotesk
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: -0.02em
  h1:
    fontFamily: Space Grotesk
    fontSize: 36px
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: -0.015em
  h2:
    fontFamily: Space Grotesk
    fontSize: 24px
    fontWeight: 700
    lineHeight: 1.3
  h3:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: 0.08em
  body-lg:
    fontFamily: Space Grotesk
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.7
  body-md:
    fontFamily: Space Grotesk
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0.06em
  nav:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1
rounded:
  none: 0px
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 48px
  xxl: 80px
  gutter: 24px
  section: 96px
  max-width: 1100px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    rounded: "{rounded.sm}"
    padding: "12px 24px"
    typography: "{typography.label}"
  button-primary-hover:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.surface}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    rounded: "{rounded.sm}"
    padding: "12px 24px"
    borderColor: "{colors.border}"
  nav-link:
    textColor: "{colors.secondary}"
    typography: "{typography.nav}"
  nav-link-hover:
    textColor: "{colors.primary}"
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.sm}"
    borderColor: "{colors.border}"
    padding: "0px"
  card-label:
    textColor: "{colors.on-surface-muted}"
    typography: "{typography.label}"
  tag:
    backgroundColor: "{colors.surface-subtle}"
    textColor: "{colors.secondary}"
    rounded: "{rounded.full}"
    padding: "4px 10px"
    typography: "{typography.label}"
---

# Harry Poole — Portfolio Design System

## Overview

A senior UX/UI product designer's personal portfolio. The aesthetic is quiet, editorial, and confident — letting the work speak. The UI echoes the discipline of good design: nothing wasted, nothing missing. The entire site uses Space Grotesk, a monospaced typeface, as its sole font — a deliberate, distinctive choice that gives the portfolio a technical, grid-conscious character. White space is generously applied; the grid is structured but not rigid. The overall feel is analogous to a well-typeset developer blog or a design-led zine.

The target audience is hiring managers, design leads, and product teams in B2B SaaS and civic/mapping technology sectors. The emotional response sought is trust, credibility, and a sense that this designer thinks carefully before acting.

## Colors

The palette is deliberately restrained — near-monochrome with a single interaction accent.

- **Primary (#1A1A1A):** Near-black used for all headline text and primary actions. Warmer than pure black, avoiding harshness.
- **Secondary (#555555):** Mid-grey for body copy, navigation links, and secondary labels. Readable without competing with headlines.
- **Accent (#2563EB):** A confident, professional blue used exclusively for interactive elements — links in hover state, focus rings, and active tags. Signals interaction without dominating.
- **Surface (#FFFFFF):** Pure white as the primary canvas. The design lives in the open air; backgrounds are always white or near-white.
- **Surface Subtle (#F7F7F7):** A near-white used for project card hover states, tag backgrounds, and section demarcation. Barely perceptible, keeps the palette clean.
- **Border (#E5E5E5):** A light mid-tone used for card outlines, dividers, and nav underlines. Structural but invisible at a glance.
- **On Surface Muted (#6B7280):** Used for metadata text — dates, category labels, captions — subordinate to the main content hierarchy.

Colour is used structurally, not decoratively. The accent blue must never appear in decorative illustrations or backgrounds — only on interactive affordances.

## Typography

The entire site uses a single typeface: **Space Grotesk**, a monospaced font with strong technical character. This is an unconventional choice for a portfolio — it signals a designer who is comfortable with code and systematic thinking, and gives the site a distinctive, slightly editorial feel that stands out from the standard sans-serif portfolio aesthetic.

- **Display & Headlines:** Space Grotesk Bold at large sizes. The monospaced character widths create a natural rhythm and grid-like quality in headlines.
- **Body:** Space Grotesk Regular at 16–18px with generous line height (1.6–1.7). Monospaced body text is deliberately slower to read — this suits a portfolio where considered, careful reading is encouraged.
- **Labels & Metadata:** Space Grotesk Regular at 12px with generous letter-spacing. Used for project categories, year tags, nav items, and button text.
- **H3 / Eyebrow:** Space Grotesk Bold at 14px, all-caps with tracked letter-spacing.

Because Space Grotesk is the sole typeface, hierarchy is achieved entirely through size, weight (Regular vs Bold), and colour — not through typeface contrast. Never introduce a second font.

## Layout

The layout follows a centred, max-width container model (1100px), with generous horizontal padding on smaller viewports. The grid is informal — not a rigid column system, but a disciplined use of vertical rhythm and horizontal breathing room.

Sections are separated by large vertical space (96px between major content blocks) to create a slow, deliberate scroll cadence. Project cards use a two- or three-column masonry-style grid on desktop, collapsing to single column on mobile.

Navigation is minimal: a fixed or sticky top bar with the designer's name left-anchored and nav links right-aligned. No mega-menus, no dropdowns.

The hero section is asymmetric by intent — a large headline with a single CTA on the left, and a portrait or hero image sitting offset to the right, creating visual tension and energy.

## Elevation & Depth

Depth is achieved almost entirely through whitespace and proximity, not shadows. Cards are distinguished from the background via a subtle 1px border (`{colors.border}`) rather than drop shadows. This keeps the UI flat and refined.

The one exception is image thumbnails on project cards on hover — a very subtle `box-shadow: 0 4px 16px rgba(0,0,0,0.08)` may appear to lift the card gently. This should feel like lifting a piece of paper, not a material UI elevation.

No blur effects, no glassmorphism. The design is matte and grounded.

## Shapes

All interactive and container elements use a minimal corner radius. The language is architectural — sharp enough to feel precise, with just enough rounding to feel modern.

- **Buttons and tags:** 4px radius — firm, structured.
- **Input fields:** 4px radius.
- **Cards:** 4px radius, or fully square (0px) for hero image containers.
- **Pill tags** (category labels): 9999px (full) — the only soft shape in the system, used to clearly distinguish metadata chips from interactive elements.

Avoid large radius values (>16px) on any structural container. Circular shapes are reserved for avatar/portrait images only.

## Components

### Navigation

The top nav is horizontal and minimal. The site name/logo is set in Space Grotesk Bold, left-aligned. Navigation links use `{typography.nav}` in `{colors.secondary}`, transitioning to `{colors.primary}` on hover with no underline by default. Active page link uses `{colors.primary}` and a subtle bottom border in `{colors.primary}`.

### Project Cards

Cards display a 16:9 or 3:2 thumbnail image, followed by a category/tag row (using `tag` component tokens), and a card title using `{typography.h2}`. The image fills the card top with no border radius on the top edge. On hover, the image should subtly scale (transform: scale(1.02)) with a 200ms ease transition. Cards have no visible border at rest — a `{colors.border}` 1px border appears on hover alongside the image lift shadow.

### Process Step Labels

The Define / Design / Prototype / Validate tabs on the Process page are rendered as a horizontal sequence of uppercase labels in `{typography.h3}`, using `{colors.secondary}` at rest and `{colors.primary}` when active, with a 2px underline in `{colors.accent}` as the active indicator.

### Buttons

Primary CTAs (e.g. "View all projects") use `button-primary` tokens. They sit inline or below content blocks, never floating. Secondary navigation buttons use `button-secondary`. Buttons never use icons alone — always pair with a text label.

### Tags / Category Labels

Project category and year metadata uses the `tag` component — small, pill-shaped, surface-subtle background with muted text. These are always non-interactive when used as labels. When used as filters, they adopt `{colors.accent}` background and white text in the selected state.

### Contact Links

The contact section renders each method (LinkedIn, Email, Call) as a large H2 Space Grotesk Bold link — the link text is `{colors.primary}` at rest and `{colors.accent}` on hover, with no underline by default, an underline on hover. These are intentionally oversized — they feel like invitations, not buttons.

## Do's and Don'ts

- **Do** use the accent blue exclusively for interactive affordances — links, focus rings, active states, selected tags. Never as decoration.
- **Do** allow generous whitespace between sections. When in doubt, add more space.
- **Do** use Space Grotesk exclusively — no other typeface should ever be introduced.
- **Do** establish hierarchy through size, weight, and colour alone — Regular vs Bold, large vs small, primary vs muted.
- **Do** write category labels and process step labels in all-caps with tracked letter-spacing using `{typography.h3}`.
- **Don't** add decorative background colours, gradients, or patterns to section containers. Keep all backgrounds white or surface-subtle.
- **Don't** use more than two font weights per view (Regular and Bold only).
- **Don't** use card shadows at rest — only on hover, and keep them subtle.
- **Don't** use rounded corners larger than 8px on structural containers.
- **Don't** centre-align body copy or long-form text. Left-alignment only.
- **Do** maintain WCAG AA contrast ratios at all times. Primary text on white: 15.3:1. Secondary text on white: 7.4:1. Accent on white: 4.6:1 — passes AA.
