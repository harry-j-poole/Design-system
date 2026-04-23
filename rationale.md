# Harry Poole — Portfolio Design System Rationale

This document captures the reasoning behind design decisions in this system: what was decided, why, and what constraints each decision places on the interface. It is not a spec — token values and component rules live in [design.md](design.md). This document exists to prevent those rules from being eroded when decisions are revisited without context.

---

## Audience & intended response

The primary audience is hiring managers, design leads, and product leads at B2B and B2C SaaS companies. These are people who review many portfolios and are acutely sensitive to visual noise, inconsistency, and effort that signals insecurity rather than confidence.

The intended emotional response is **trust, credibility, and careful thinking** — not delight, novelty, or expressiveness. Every design decision in this system is oriented toward that goal. When a choice feels "too plain", that is often correct.

---

## Decision log

### 1. Single typeface — Space Grotesk only

**What was decided:** The entire interface uses Space Grotesk exclusively — no secondary typeface at any scale or context. Hierarchy is achieved through size, weight (`400` vs `700`), and colour alone.

**Why:** A dual-typeface approach is a common portfolio convention used to create perceived visual richness. For this audience — experienced designers and leads — that richness reads as decoration rather than craft. A single typeface, applied with restraint and precision, signals that hierarchy was achieved through discipline rather than variety. Space Grotesk was chosen specifically for its technical, grid-conscious character: the monospaced-influenced proportions give headlines a structural quality that suits a designer who operates between design and engineering.

**Constraint:** No second typeface may be introduced, even for code samples, captions, or special contexts. If hierarchy is insufficient, the solution is size, weight, or colour — not a new font.

**Validation:** To be confirmed

---

### 2. Near-monochrome palette with a single interaction accent

**What was decided:** The palette is near-black (`primary: #1A1A1A`), mid-grey (`secondary: #555555`), and warm off-white (`surface: #f9f9f1`, `surface-subtle: #f0f0e8`) — supplemented by a single accent green (`accent: #3f8348`) used exclusively for interactive affordances. The accent appears on linked card titles, contact links, focus rings, and active filter tags. It never appears as a decorative colour, background fill, or illustrative element.

**Why:** The audience encounters colour-saturated portfolio sites frequently. Restraint is the differentiator. Near-monochrome establishes credibility and directs attention entirely to the work. The accent green serves a functional purpose — it tells the user "this is interactive" — without competing with the case study content. Green was chosen over blue to avoid the visual language of generic enterprise SaaS; it is confident and fresh without being expressive.

The warm surface tones (`#f9f9f1`, `#f0f0e8`) were chosen over pure white to soften long reading sessions and create a slight editorial quality, reminiscent of good print design. Pure white can read as clinical in the context of a portfolio.

**Constraint:** The accent colour may not be used on any element that is not interactive. If a new UI element needs colour for decoration or structure, use `surface-subtle` or `border` — not `accent`. Any introduction of additional hues (even neutrals) must be deliberate and recorded here.

**Validation:** To be confirmed

---

### 3. Whitespace as the primary structural tool

**What was decided:** Section-level vertical spacing is set at `96px` (`section` token). Component-level breathing room is `48px` (`xl`). The page container caps at `1100px` (`max-width`) with a `24px` gutter on smaller viewports.

**Why:** The audience's reading context is a considered, deliberate review — not a skimmed feed. Generous vertical rhythm creates a slow scroll cadence that encourages evaluation of each section before moving on. The `1100px` cap keeps line lengths readable without overextending on wide monitors, and keeps the layout in line with editorial conventions the audience will recognise from well-designed publications and design-led product sites.

**Constraint:** Do not tighten section spacing to fit more content on screen. If a section feels too long, the content should be edited — not the spacing reduced. Spacing tokens below `xl` are for internal component padding only, not between content sections.

---

### 4. Flat surfaces — depth through whitespace, not shadow

**What was decided:** The system uses no drop shadows anywhere — not at rest, not on hover. Cards are borderless at rest and communicate interaction through image zoom (`scale(1.05)`, `all 0.25s ease-in-out`) alone. No blur effects, glassmorphism, or layered elevation.

**Why:** Depth effects (shadows, blur, elevation) are associated with material UI metaphors and high-density interfaces. This portfolio is neither. Shadow implies competition between elements — that some cards are "above" others — which fragments attention. Image zoom keeps the interaction signal contained within the content itself: the work responds to the user rather than the container. This is a more considered, less conventional affordance pattern for a portfolio that is trying to demonstrate exactly that kind of thinking.

**Constraint:** No drop shadow may be used on any element at any state. If a new component needs to signal interactivity, the solution is a content-level or colour-level change — not elevation.

---

### 5. Colour used only for interaction — never hierarchy

**What was decided:** Accent green (`#3f8348`) is reserved solely for interactive affordances. It is never used to visually distinguish sections, highlight key content, or create emphasis.

**Why:** If the accent appears on non-interactive elements, the user learns — consciously or not — that green does not reliably mean "clickable." This erodes the signal value of the colour and increases cognitive load. Maintaining strict colour discipline means users only need to learn one rule: green means interaction.

**Constraint:** Any component that appears interactive but is not (e.g. a decorative callout styled like a link) must not use the accent colour. If a new component is added that is interactive, it should adopt accent on its key affordance.

---

### 6. Fully square geometry — no border radius

**What was decided:** Every element in the system — buttons, cards, tags, inputs, containers — uses `border-radius: 0px`. No rounding is introduced at any scale.

**Why:** The square geometry is a direct extension of the typeface choice. Space Grotesk's letterforms are angular and grid-constructed; introducing rounded containers would create a visual tension between the type and the UI shapes. Keeping both fully square makes the typeface and the layout feel like they belong to the same system — formal, precise, and deliberately constructed. It also avoids associations with consumer-facing product aesthetics (rounded cards and pill tags are visual shorthand for apps like Notion or Figma), which is the wrong register for a portfolio targeting B2B and civic tech hiring audiences.

**Constraint:** No `border-radius` value other than `0px` may be used anywhere in the interface. Portrait/avatar images that appear circular are the only exception — that shape is determined by the content, not a container style.

**Validation:** To Be Confirmed

---

## What this means in practice

These decisions collectively produce a system with a small number of firm constraints:

- One typeface, two weights, no exceptions.
- Accent green on interactive elements only — never decorative.
- Depth through whitespace only — no shadows anywhere, at any state.
- Hierarchy through size, weight, and colour — not variety.
- Spacing is not negotiable to fit content; content is edited to fit the spacing.

[design.md](design.md) contains the token values and component rules that implement these decisions. Changes to tokens should be traced back to a decision recorded here.

---

## Open questions & validation backlog

| Question | Priority | Method |
|----------|----------|--------|
| Does the accent green (`#3f8348`) meet WCAG AA on `surface` for body-sized interactive text? | High | Contrast checker — confirm before shipping card title links |
| Does the single-typeface approach read as confident or limited to first-time visitors? | Medium | First-impression testing or hallway testing with 3–5 target-audience peers |
| Does the hero section establish credibility within the first 5 seconds? | Medium | Five-second test with hiring manager / design lead participants |
| Does the slow-scroll cadence (96px section gaps) feel deliberate or slow on mobile? | Low | Usability walkthrough on iOS Safari — may require a responsive spacing adjustment |
| Should the nav become sticky or fixed on scroll, or remain static? | Low | Behaviour testing — note any confusion about where the nav is after scrolling past the hero |
