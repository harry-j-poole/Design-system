# Harry Poole — Design System

This repository defines the design system for [harrypoole.co.uk](https://harrypoole.co.uk) — a personal portfolio for a senior UX/UI product designer working across B2B and B2C. The system is intended as the canonical reference for building future websites, apps, and interfaces that extend or sit alongside the portfolio — ensuring visual and behavioural consistency regardless of who or what builds them.

---

## What this system is

A minimal, editorial design system built around a single idea: the interface should communicate discipline and careful thinking, not personality or decoration. Every visual decision — the typeface, the palette, the geometry, the spacing — is in service of one goal: to make a hiring manager or design lead trust the work before they have read a single word.

The aesthetic is flat, formal, and typographically driven. It is not warm, playful, or expressive. It is precise.

---

## Aesthetic values

**Restraint over richness.** Visual complexity is a liability. The system uses one typeface, two weights, and one accent colour. Hierarchy comes from size, weight, and colour — never from variety.

**Geometry that echoes the type.** Space Grotesk's letterforms are angular and grid-constructed. Every UI element — buttons, cards, tags, inputs — is fully square (`border-radius: 0px`). The shapes and the type belong to the same formal language.

**Colour as a functional signal.** The accent green (`#3f8348`) means one thing: this is interactive. It never appears as decoration, emphasis, or background fill. The rest of the palette is near-monochrome — warm off-white surfaces, near-black text, mid-grey for secondary content.

**Depth through whitespace, not elevation.** There are no drop shadows anywhere in the system. Separation between elements is achieved through space and a single `1px` border token. Cards signal interactivity through image zoom alone — the content responds, not the container.

**Slow, deliberate pace.** Generous section spacing (`96px`) is intentional. The audience is reading carefully, not scanning. Space is not wasted — it is doing structural work.

---

## Non-negotiable rules

When building any interface using this system, the following rules hold without exception:

1. **One typeface only — Space Grotesk.** No second font for any purpose.
2. **Two weights only — Regular (`400`) and Bold (`700`).**
3. **Accent green on interactive affordances only** — links, focus rings, active states, selected filters. Never decorative.
4. **No border radius.** All elements are square. `border-radius: 0px` everywhere.
5. **No drop shadows** at any state on any element.
6. **No gradients, blur effects, or glassmorphism.**
7. **Left-align all body copy.** Centre-alignment is not used.
8. **Backgrounds are white or surface-subtle only.** No decorative fills on section containers.
9. **Spacing is fixed.** Do not reduce section spacing to fit content — edit the content instead.
10. **WCAG AA contrast must be maintained** at all times across all text and interactive elements.

---

## Files in this system

| File | Purpose |
|------|---------|
| [design.md](design.md) | Token definitions and component specs — the implementation reference |
| [rationale.md](rationale.md) | Decision log — what was decided, why, and what constraints each decision creates |

**Start with [design.md](design.md)** when building a new interface. It contains the colour tokens, typography scale, spacing values, and component rules needed to construct any screen consistently.

**Consult [rationale.md](rationale.md)** before making any change to the system, or when a design decision needs to be revisited. It explains the reasoning that produced each rule — reading it prevents well-intentioned changes from quietly eroding the system's coherence.

---

## Intended use

This system is designed to be usable by AI tools building new interfaces. Any interface generated from this system should pass the following test: does it feel like it was made by the same person who made harrypoole.co.uk? If it introduces rounding, shadows, second typefaces, decorative colour, or expressive motion — it does not belong to this system.

When in doubt, do less.
