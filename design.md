---
name: Harry Poole Portfolio
description: Personal portfolio design system for a senior UX/UI Product Designer. Clean, minimal, and professional — communicating clarity of thought and design craft.
colors:
  primary: "#1A1A1A"
  accent: "#3f8348"
  surface: "#f9f9f1"
  surface-subtle: "#f0f0e8"
  border: "#E5E5E5"
  on-surface: "#1A1A1A"
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
borders:
  strong: "2px solid #000000"
  subtle: "1px solid #E5E5E5"
rounded:
  none: 0px
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
    rounded: "{rounded.none}"
    padding: "12px 24px"
    typography: "{typography.label}"
  button-primary-hover:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.surface}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.none}"
    padding: "12px 24px"
    border: "{borders.strong}"
  nav-link:
    textColor: "{colors.on-surface}"
    typography: "{typography.nav}"
  nav-link-hover:
    textColor: "{colors.primary}"
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.none}"
    border: "none"
    padding: "0px"
  card-hover:
    imageTransform: "scale(1.05)"
    imageTransition: "all 0.25s ease-in-out"
  card-label:
    textColor: "{colors.on-surface}"
    typography: "{typography.label}"
  card-title-link:
    textColor: "{colors.accent}"
  card-title-link-hover:
    textColor: "{colors.accent}"
    textDecoration: underline
  tag:
    backgroundColor: "{colors.surface-subtle}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.none}"
    padding: "4px 10px"
    border: "{borders.subtle}"
    typography: "{typography.label}"
---

# Harry Poole — Portfolio Design System

## Overview

A senior UX/UI product designer's personal portfolio. The aesthetic is quiet, editorial, and confident — letting the work speak. The UI echoes the discipline of good design: nothing wasted, nothing missing. The entire site uses Space Grotesk, a monospaced typeface, as its sole font — a deliberate, distinctive choice that gives the portfolio a technical, grid-conscious character. White space is generously applied; the grid is structured but not rigid. The overall feel is analogous to a well-typeset developer blog or a design-led zine.

The target audience is hiring managers, design leads, and product teams in B2B SaaS and civic/mapping technology sectors. The emotional response sought is trust, credibility, and a sense that this designer thinks carefully before acting.

## Colors

The palette is deliberately restrained — near-monochrome with a single interaction accent.

- **On Surface / Primary (#1A1A1A):** The sole text colour for all non-link content — headlines, body copy, labels, metadata, captions. No grey text variants. Hierarchy is achieved through size and weight only.
- **Accent (#3f8348):** Used exclusively for interactive elements — linked card titles, contact links, focus rings, and active tags. The only colour that deviates from near-black for text.
- **Surface (#f9f9f1):** The primary page background. Warm off-white rather than pure white — softens long reading sessions and gives the UI a slight editorial quality.
- **Surface Subtle (#f0f0e8):** A secondary background for use within content — table row alternation, small informational cards, tag backgrounds, and any element that needs to be distinguishable from the main surface without introducing a new colour.
- **Border (#E5E5E5):** Used for subtle structural dividers on smaller UI elements — tag outlines, table rules, fine separators. Not for main component borders.

Colour is used structurally, not decoratively. The accent green must never appear in decorative illustrations or backgrounds — only on interactive affordances.

## Borders

Two border styles are used, differentiated by context:

- **Strong (`2px solid #000000`):** Applied to main UI components — buttons (secondary variant), input fields, and any structural container that needs a defined edge. The weight reinforces the sharp, formal geometry of the system.
- **Subtle (`1px solid #E5E5E5`):** Applied to smaller UI elements — tags, table row dividers, fine separators. Present but visually recessive.

Never use `border-subtle` on a primary interactive component, and never use `border-strong` as a decorative divider.

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

Depth is achieved through whitespace and proximity, not shadows. Main UI components use `{borders.strong}` to define their edges. Smaller structural elements use `{borders.subtle}`. No drop shadows are used anywhere.

There are no exceptions. Cards do not gain shadow on hover — interaction is communicated entirely through image zoom (`scale(1.05)`, `all 0.25s ease-in-out`). No depth layer is ever added. See `card-hover` component tokens.

No blur effects, no glassmorphism. The design is matte and grounded.

## Shapes

All elements are fully square — `border-radius: 0px` across buttons, cards, tags, inputs, and containers without exception. The sharp geometry is a deliberate echo of Space Grotesk's own angular, grid-constructed letterforms. The typeface and the UI shapes reinforce each other: both precise, both built on a formal grid.

No rounding is introduced at any scale. Circular shapes (e.g. portrait images) are the only exception, where the shape is determined by content not container.

## Components

### Navigation

The top nav is horizontal and minimal. The site name/logo is set in Space Grotesk Bold, left-aligned. Navigation links use `{typography.nav}` in `{colors.on-surface}`, with no underline by default. Active page link uses `{colors.primary}` and a subtle bottom border in `{colors.primary}`.

### Project Cards

Cards display a 16:9 or 3:2 thumbnail image, followed by a category/tag row (using `tag` component tokens), and a card title using `{typography.h2}`. Card titles are rendered as links and use `card-title-link` tokens — `{colors.accent}` green at rest, with underline on hover. The image fills the card top with no border radius on the top edge. At rest, cards have no border or shadow — use `card` tokens. On hover, apply `card-hover` tokens: `scale(1.05)` on the image with a `all 0.25s ease-in-out` transition. No shadow is added at any state.

### Process Step Labels

The Define / Design / Prototype / Validate tabs on the Process page are rendered as a horizontal sequence of uppercase labels in `{typography.h3}`, using `{colors.on-surface}` at rest and `{colors.on-surface}` when active, with a 2px underline in `{colors.accent}` as the active indicator.

### Buttons

Primary CTAs (e.g. "View all projects") use `button-primary` tokens. They sit inline or below content blocks, never floating. Secondary navigation buttons use `button-secondary`. Buttons never use icons alone — always pair with a text label.

### Tags / Category Labels

Project category and year metadata uses the `tag` component — small, square-cornered, surface-subtle background with muted text. These are always non-interactive when used as labels. When used as filters, they adopt `{colors.accent}` background and white text in the selected state.

### Contact Links

The contact section renders each method (LinkedIn, Email, Call) as a large H2 Space Grotesk Bold link — the link text is `{colors.primary}` at rest and `{colors.accent}` on hover, with no underline by default, an underline on hover. These are intentionally oversized — they feel like invitations, not buttons.

## Do's and Don'ts

- **Do** use the accent green exclusively for interactive affordances — linked card titles, contact links, focus rings, active states, selected tags. Never as decoration.
- **Do** allow generous whitespace between sections. When in doubt, add more space.
- **Do** use Space Grotesk exclusively — no other typeface should ever be introduced.
- **Do** establish hierarchy through size and weight alone — Regular vs Bold, large vs small. Colour is not used to differentiate text levels.
- **Do** use `{colors.on-surface}` (#1A1A1A) for all text. The only exception is link text, which uses `{colors.accent}`.
- **Do** use `{borders.strong}` on main UI components and `{borders.subtle}` on smaller elements and dividers.
- **Do** use `{colors.surface-subtle}` as a secondary background to differentiate nested or grouped content — table rows, info cards, tag chips.
- **Do** write category labels and process step labels in all-caps with tracked letter-spacing using `{typography.h3}`.
- **Don't** add decorative background colours, gradients, or patterns to section containers. Backgrounds are `{colors.surface}` or `{colors.surface-subtle}` only.
- **Don't** use more than two font weights per view (Regular and Bold only).
- **Don't** use shadows anywhere — at rest or on hover.
- **Don't** introduce any border radius — all elements are square. No exceptions.
- **Don't** centre-align body copy or long-form text. Left-alignment only.
- **Do** maintain WCAG AA contrast ratios at all times. On-surface text on surface: 15.3:1. Accent green on surface: verify passes AA (4.5:1 minimum).
