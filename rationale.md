# Harry Poole — Portfolio Design System Rationale

This document captures the reasoning behind design decisions in this system: what was decided, why, and what constraints each decision places on the interface. It is not a spec — token values and component rules live in [design.md](design.md). This document exists to prevent those rules from being eroded when decisions are revisited without context.

---

## Audience & intended response

The primary audience is hiring managers, design leads, and product leads at B2B and B2C SaaS companies. These are people who review many portfolios and are acutely sensitive to visual noise, inconsistency, and effort that signals insecurity rather than confidence.

The intended emotional response is **trust, credibility, and careful thinking** — not delight, novelty, or expressiveness. Every design decision in this system is oriented toward that goal. When a choice feels "too plain", that is often correct.

---

## Decision log

### 1. Single typeface — Space Grotesk only

**What was decided:** The entire interface uses Space Grotesk exclusively — no secondary typeface at any scale or context. Hierarchy is achieved through size and weight (`400` vs `700`) alone — not colour, not typeface variety.

**Why:** A dual-typeface approach is a common portfolio convention used to create perceived visual richness. For this audience — experienced designers and leads — that richness reads as decoration rather than craft. A single typeface, applied with restraint and precision, signals that hierarchy was achieved through discipline rather than variety. Space Grotesk was chosen specifically for its technical, grid-conscious character: the monospaced-influenced proportions give headlines a structural quality that suits a designer who operates between design and engineering.

**Constraint:** No second typeface may be introduced, even for code samples, captions, or special contexts. If hierarchy is insufficient, the solution is size or weight — not a new font, and not a colour change.

**Validation:** To be confirmed

---

### 2. Near-monochrome palette with a single interaction accent

**What was decided:** All text uses a single colour: `on-surface: #1A1A1A`. There are no grey text variants for secondary or muted content — hierarchy within text is achieved through size and weight only. The sole colour departure for text is the accent green (`#3f8348`), used exclusively on interactive elements (links, focus rings, active states). Background colours are `surface: #f9f9f1` as the primary canvas and `surface-subtle: #f0f0e8` as a secondary background for grouped or nested content — table rows, informational cards, tag chips. The structural border colour `#E5E5E5` is used on smaller elements only.

**Why:** The audience encounters colour-saturated portfolio sites frequently. Restraint is the differentiator. Removing grey text variants forces hierarchy to be solved through typography alone — which is the harder, more disciplined solution, and the one that holds up best at scale. A mid-grey body text is a common default that signals convention rather than intention.

The warm surface tones were chosen over pure white to soften long reading sessions and give the UI a slight editorial quality. `surface-subtle` provides just enough visual separation for nested content without introducing a new colour — it reads as the same family as the main surface, just slightly cooler.

**Constraint:** No grey text variants. If content feels insufficiently differentiated, the solution is a size or weight change — not a colour change. `surface-subtle` may be used freely as a background within content areas. Any introduction of additional hues must be deliberate and recorded here.

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

### 5. Colour used only for interaction — never hierarchy or decoration

**What was decided:** Colour plays no role in text hierarchy. All non-link text is `#1A1A1A` regardless of its position in the content structure — headlines, body, labels, captions, metadata. The accent green (`#3f8348`) is the only colour used on text, and only when that text is interactive. Colour is not used to create emphasis, section differentiation, or visual weight within prose.

**Why:** Using grey text for secondary content is a convention so common it has become invisible — it no longer communicates a deliberate decision. Flattening all text to a single colour forces every other aspect of the system (size, weight, spacing, position) to do more work. The result is a more disciplined hierarchy that holds up under scrutiny. It also means the accent green carries an unambiguous signal: the moment a user sees it, they know they can interact. No other colour competes for that meaning.

**Constraint:** Any component that appears interactive but is not must not use the accent colour. Any component that is interactive should use accent on its key affordance. Grey text variants must not be reintroduced — if a piece of content needs to feel subordinate, reduce its size or weight.

---

### 6. Fully square geometry — no border radius

**What was decided:** Every element in the system — buttons, cards, tags, inputs, containers — uses `border-radius: 0px`. No rounding is introduced at any scale.

**Why:** The square geometry is a direct extension of the typeface choice. Space Grotesk's letterforms are angular and grid-constructed; introducing rounded containers would create a visual tension between the type and the UI shapes. Keeping both fully square makes the typeface and the layout feel like they belong to the same system — formal, precise, and deliberately constructed. It also avoids associations with consumer-facing product aesthetics (rounded cards and pill tags are visual shorthand for apps like Notion or Figma), which is the wrong register for a portfolio targeting B2B and civic tech hiring audiences.

**Constraint:** No `border-radius` value other than `0px` may be used anywhere in the interface. Portrait/avatar images that appear circular are the only exception — that shape is determined by the content, not a container style.

**Validation:** To Be Confirmed

---

### 7. Two-tier border system — strong for structure, subtle for detail

**What was decided:** Two border styles are used across the system. Main UI components (buttons, inputs, structural containers) use `2px solid #000000`. Smaller elements and dividers (tags, table rules, separators) use `1px solid #E5E5E5`. No other border values are introduced.

**Why:** A uniform single-weight border across all elements creates a flat, undifferentiated surface — everything competes at the same visual register. The strong border (`2px solid black`) gives primary interactive components a defined, confident edge that reinforces the formal geometry of the system and signals affordance without colour. The subtle border (`1px #E5E5E5`) handles structural detail at a finer scale — separating rows, containing chips — without adding visual weight to areas that should recede. The distinction is functional: strong borders say "this is a component you interact with", subtle borders say "this is a structural division."

**Constraint:** Do not use `borders.strong` as a decorative divider or section separator. Do not use `borders.subtle` as the border on a primary interactive component. If a new component sits ambiguously between the two, default to `borders.strong` — erring toward clarity.

---

## What this means in practice

These decisions collectively produce a system with a small number of firm constraints:

- One typeface, two weights, no exceptions.
- All text is `#1A1A1A`. Hierarchy is size and weight only — no grey text variants.
- Accent green on interactive elements only — never for emphasis or decoration.
- Two border weights: `2px solid #000` on main components, `1px solid #E5E5E5` on detail elements.
- Depth through whitespace only — no shadows anywhere, at any state.
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
