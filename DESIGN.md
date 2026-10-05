---
name: PayRoll Protect
description: The financial verification layer between construction sites and payroll approval.
colors:
  lime: "oklch(0.770 0.206 151)"
  lime-dk: "oklch(0.680 0.210 151)"
  lime-text: "oklch(0.400 0.130 151)"
  lime-grad-start: "oklch(0.710 0.215 148)"
  btn-ink: "oklch(0.18 0.015 145)"
  danger: "oklch(0.65 0.20 25)"
  danger-bg: "oklch(0.20 0.020 25)"
  audit-night: "oklch(0.170 0.008 115)"
  surface: "oklch(0.225 0.010 115)"
  surface-deep: "oklch(0.175 0.010 115)"
  surface-lift: "oklch(0.210 0.012 115)"
  surface-subtle: "oklch(0.203 0.008 115)"
  border: "oklch(0.280 0.008 115)"
  muted: "oklch(0.630 0.008 115)"
  dim: "oklch(0.680 0.006 115)"
  ink: "oklch(0.920 0.004 110)"
typography:
  display:
    fontFamily: "'Montserrat', system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 3.2vw, 2.75rem)"
    fontWeight: 450
    lineHeight: 1.12
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "'Montserrat', system-ui, sans-serif"
    fontSize: "clamp(2rem, 4vw, 3.25rem)"
    fontWeight: 200
    lineHeight: 1.12
    letterSpacing: "-0.025em"
  body:
    fontFamily: "'Geist', system-ui, sans-serif"
    fontSize: "clamp(1rem, 1.4vw, 1.125rem)"
    fontWeight: 300
    lineHeight: 1.65
    letterSpacing: "0.01em"
  label:
    fontFamily: "'Geist', system-ui, sans-serif"
    fontSize: "0.775rem"
    fontWeight: 300
    lineHeight: 1
    letterSpacing: "0.07em"
  display-numeric:
    fontFamily: "'Barlow Condensed', 'Montserrat', system-ui, sans-serif"
    fontSize: "clamp(4rem, 11vw, 8rem)"
    fontWeight: 700
    fontStyle: "italic"
    lineHeight: 0.88
    letterSpacing: "-0.02em"
rounded:
  focus: "2px"
  btn: "7px"
  card: "10px"
  card-lg: "16px"
  pill: "999px"
spacing:
  xs: "0.5rem"
  sm: "1rem"
  md: "1.5rem"
  lg: "2.5rem"
  section: "clamp(5.5rem, 10vw, 9.5rem)"
  section-lg: "clamp(7.5rem, 14vw, 12rem)"
components:
  button-primary:
    backgroundColor: "linear-gradient(90deg, oklch(0.710 0.215 148), oklch(0.840 0.210 155))"
    textColor: "{colors.btn-ink}"
    rounded: "{rounded.btn}"
    padding: "0.9rem 2.125rem"
    typography: "body"
  button-primary-hover:
    backgroundColor: "linear-gradient(90deg, oklch(0.710 0.215 148), oklch(0.840 0.210 155))"
    textColor: "{colors.btn-ink}"
    rounded: "{rounded.btn}"
    padding: "0.9rem 2.125rem"
  button-primary-active:
    backgroundColor: "linear-gradient(90deg, oklch(0.710 0.215 148), oklch(0.840 0.210 155))"
    textColor: "{colors.btn-ink}"
    rounded: "{rounded.btn}"
    padding: "0.9rem 2.125rem"
  button-cta:
    backgroundColor: "linear-gradient(90deg, oklch(0.710 0.215 148), oklch(0.840 0.210 155))"
    textColor: "{colors.btn-ink}"
    rounded: "{rounded.btn}"
    padding: "0.6rem 1.375rem"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "0"
    padding: "0.5rem 0"
---

# Design System: PayRoll Protect

## Overview

**Creative North Star: "The Verification Layer"**

PayRoll Protect is a financial control mechanism, not a consumer application. Every visual decision reads as institutional rigour — the interface is what stands between a contractor's claim and a payment leaving the account. The visual language communicates: this system does not approve things lightly.

The palette is austere by design. Near-black surfaces (Audit Night) form the operating environment. Montserrat provides architectural, authoritative headings at low weight — the kind of type found on a planning document, not a startup landing page. Geist handles all prose and data with clinical legibility. Lime — the single accent colour — appears only at verified, approved, or actionable moments. It is earned. Seeing lime means something cleared.

Interaction is restrained and professional. Controls recede until needed. There are no animations for decoration. Motion serves comprehension: it reveals verified states, draws attention to discrepancies, and confirms that an action has landed.

**Key Characteristics:**
- Austere dark surfaces — no light mode
- Lime reserved for approval and verification only; never decorative
- Danger red for unverified, disputed, or flagged states
- Low-weight display type (Montserrat 200–450) over dense body copy (Geist 300)
- Flat tonal layering with one structural shadow on floating elements
- Precision spacing — deliberate rhythm between evidence and action

## Colors

A binary palette: dark neutrals for the operating environment; lime for what's verified; red for what isn't.

### Primary
- **Verification Green** (`oklch(0.770 0.206 151)` / `--lime`): The single approval signal. Used on primary CTAs, verified-state icons, active indicators, and key data figures. Seeing this colour means a claim has cleared — never use it decoratively.
- **Deep Verification Green** (`oklch(0.680 0.210 151)` / `--lime-dk`): Darker lime for text on dark surfaces where full lime would be too bright. Keyword emphasis, inline highlights.
- **Lime Text Dark** (`oklch(0.400 0.130 151)` / `--lime-text-dk`): Low-luminance lime for small labels or eyebrows on mid-dark surfaces where contrast is needed without full saturation.
- **Lime Gradient Start** (`oklch(0.710 0.215 148)` / `--lime-grad-start`): The warmer, darker start of the primary button gradient. Exists only inside `--lime-grad` (`linear-gradient(90deg, oklch(0.710 0.215 148), oklch(0.840 0.210 155))`). Not a standalone application colour — never used outside the gradient context.
- **Button Ink** (`oklch(0.18 0.015 145)` / `--btn-ink`): The near-black that sits on lime buttons. Ensures legibility on the lime gradient.

### Secondary
- **Unverified Red** (`oklch(0.65 0.20 25)` / `danger`): The opposite of lime. Used on invoice discrepancy states, warning icons, disputed line items, and any value that could not be verified against attendance. Never combine with lime in the same visual element.
- **Danger Surface** (`oklch(0.20 0.020 25)` / `danger-bg`): Deep red-tinted background behind danger icons. Opaque — ensures the background line in step lists doesn't show through.

### Neutral
- **Audit Night** (`oklch(0.170 0.008 115)` / `--dark-bg`): Page background. A near-black with a faint warm-grey cast — not pure black. The operating floor of the entire interface.
- **Site Surface** (`oklch(0.225 0.010 115)` / `--dark-mid`): Card and component backgrounds. One tonal step above Audit Night — the layer where content lives.
- **Surface Deep** (`oklch(0.175 0.010 115)` / `--dark-deeper`): One micro-step below Site Surface. Used for inset card backgrounds (testimonial resting state) where a slight recession from the card standard is needed. Not for page-level use.
- **Surface Lift** (`oklch(0.210 0.012 115)` / `--dark-lift`): One micro-step above Audit Night. Used for active/selected card states (testimonial active) where a subtle elevation signal is needed without reaching full Site Surface brightness.
- **Ledger Border** (`oklch(0.280 0.008 115)` / `--dark-border`): All 1px dividers, card borders, and structural separators. The third tonal step.
- **Secondary Text** (`oklch(0.630 0.008 115)` / `--dark-muted`): Supporting body copy, captions, metadata. Enough contrast to read, not enough to compete with primary content.
- **Dim Text** (`oklch(0.680 0.006 115)` / `--dark-dim`): One step lighter than muted; used for slightly elevated secondary text, step descriptions.
- **Primary Text** (`oklch(0.920 0.004 110)` / `--dark-ink`): Near-white heading and primary body text. Slightly warm — never pure `#FFFFFF`.

### Named Rules
**The One Signal Rule.** Lime is the approval signal. It may not appear on decorative elements, backgrounds, section dividers, or hover states not associated with a verified/approved action. On any given screen, lime should occupy ≤15% of the visible surface.

**The Binary Verdict Rule.** Red and lime do not share a visual field at the same hierarchy. When red appears (unverified claim), lime recedes. When lime appears (verified), red is not present on the same row. The visual system enforces a binary outcome — never ambiguous.

## Typography

**Display Font:** Montserrat (with system-ui, sans-serif fallback)
**Body Font:** Geist (with system-ui, sans-serif fallback)
**Display Numeric Font:** Barlow Condensed (italic 700) — reserved exclusively for large statistical figures

**Character:** Montserrat at low weights (200–300) reads as architectural authority — the kind of type on a site permit or a planning document. It is not decorative; it is structural. Geist handles all detail: it is sharp, legible at small sizes, and neutral enough to carry payroll data without drawing attention to itself. The pairing separates claim from evidence. Barlow Condensed italic is a third-register voice used only for headline numbers (£30K, 97%, etc.) at display scale — its condensed italic form communicates raw data with urgency.

### Hierarchy
- **Display** (weight 450, `clamp(1.75rem, 3.2vw, 2.75rem)`, line-height 1.12, tracking -0.025em): Hero headline only. Uppercase. This is the first read on the page — the promise before the evidence.
- **Headline** (weight 200, `clamp(2rem, 4vw, 3.25rem)`, line-height 1.12, tracking -0.025em): Section h2 headings. Low weight at large size reads as deliberate and unhurried — authority without aggression.
- **Title** (weight 300–400, `clamp(1rem, 1.5vw, 1.05rem)`, line-height 1.3): Step titles, card headings, list item leads. Capitalized, not uppercase.
- **Body** (weight 300, `clamp(1rem, 1.4vw, 1.125rem)`, line-height 1.65, tracking 0.01em): All prose, descriptions, supporting copy. Max line length 54ch enforced via `max-width`. Geist only.
- **Label** (weight 300, 0.775rem, tracking 0.07em, uppercase): Section tags, stat labels, badge text. These are wayfinding elements — they categorize, they never lead.
- **Display Numeric** (Barlow Condensed, italic 700, `clamp(4rem, 11vw, 8rem)`, tracking -0.02em): Large statistical figures in "The Bigger Picture" section only. `font-variant-numeric: tabular-nums`. Not used anywhere else — this voice belongs to hard numbers at hero scale.

### Named Rules
**The Weight Separation Rule.** Display and Headline use Montserrat at 200–450. Body and Label use Geist at 300. Never use Montserrat below 18px and never use it for running prose. The two fonts occupy separate registers; mixing them at the same size blurs the hierarchy.

**The Negative Tracking Rule.** All Montserrat headings carry negative letter-spacing (-0.025em minimum). Positive tracking on display type is prohibited — it reads as stretched, not authoritative.

## Layout

**Container:** `max-width: 1320px`, horizontal padding `clamp(1.5rem, 5vw, 3.5rem)`. All sections share this container.

**Grid rhythm:** Card grids sit at `1.5rem`–`2rem` gaps on desktop so the composition reads as deliberately generous rather than uniformly dense. These tighten at `780px` and again at `480px`, where the width is worth more to card contents than to the gutter. The dashboard mock (`.dash__*`) is the deliberate exception and stays at `0.5rem` — its density is what makes it read as real software.

**Section padding scale (two tiers only):**
- Standard: `clamp(5.5rem, 10vw, 9.5rem)` — supporting sections (calculator, stat bridges).
- Hero-scale: `clamp(7.5rem, 14vw, 12rem)` — all primary narrative sections (gap, trust). Hero is unique at `clamp(6rem, 11vw, 8.5rem)` to account for nav offset.

**Hero grid:** `1.2fr 0.8fr` — intentionally asymmetric. Copy leads (wider), widget supports (narrower). This proportion is not variable.

**Section rhythm:** Sections that mark a narrative shift use `border-top: 1px solid var(--dark-border)` to signal the transition. Sections that continue the same argument flow without a border.

**Responsive behavior:** Mobile-first via container padding. Hero grid collapses to single column. Three-column grids (How It Works steps) collapse to stacked single column on narrow viewports. The mobile nav is a full-overlay panel.

**Spacing scale:** xs 0.5rem → sm 1rem → md 1.5rem → lg 2.5rem. Section gaps use the two-tier clamp values above, not the scale steps.

## Elevation & Depth

Depth is expressed through tonal layering: Audit Night (bg) → Site Surface (mid) → Ledger Border (border). Three steps, no shadows on static surfaces.

One structural shadow is permitted on floating or interactive elements — the nav on scroll, the social FAB, and any card that lifts on hover interaction.

### Shadow Vocabulary
- **Structural float** (`0 4px 24px oklch(0.08 0.008 115 / 0.6)`): Used on the nav (post-scroll), FAB, and modals. Soft, dark-tinted. Suggests elevation above the page surface without drawing attention.

### Named Rules
**The Flat-By-Default Rule.** Static surfaces carry no box-shadow. Cards are defined by their background color and a 1px border — not shadow. The structural float shadow is reserved for elements that actually leave the document flow (fixed position, overlay, interactive lift). Using it on static cards violates the tonal hierarchy.

## Shapes

**Buttons** use `7px` radius — gently squared. Not pill-shaped (that reads as playful); not sharp (that reads as aggressive). 7px is precise and purposeful.

**Cards and panels** use `10px` (standard) or `16px` (prominent, featured). These radii are not interchangeable — use 10px for data cards and step containers; 16px for hero-scale CTAs and featured modules.

**Badges and pills** use `999px` (full radius). Only for status indicators, trust badges, and nav tags. Never for primary CTAs.

**Borders:** 1px solid `var(--dark-border)` on all card outlines and horizontal section dividers. No decorative colored borders. Border-left accents are prohibited — they are a craft-floor violation in this system.

**Icons:** Authored SVG geometry, 18px viewBox, 1.4–1.5px stroke-width. Consistent weight throughout. No emoji, no icon-font glyphs, no colored icon libraries. Danger icons use the danger token; verified icons use lime.

## Components

### Buttons
Restrained by default — they recede until needed. The primary button carries all the hierarchy; everything else steps back.

- **Shape:** 7px radius (`--radius-btn`)
- **Primary:** Lime gradient background (`oklch(0.710 0.215 148)` → `oklch(0.840 0.210 155)`), btn-ink text (`oklch(0.18 0.015 145)`), padding `0.9rem 2.125rem`. Includes a single-pass shimmer animation on page load. Only one per viewport section.
- **Hover:** `filter: brightness(0.93)` only. No position change. No shadow addition.
- **Active/Press:** `transform: scale(0.97)`, transition `80ms ease-out`. Instant tactile response.
- **CTA (nav-size):** Same gradient, smaller padding `0.6rem 1.375rem`. Used in the nav bar only.
- **Ghost:** Transparent background, muted text (`oklch(0.630 0.008 115)`). Hover: ink text. Active: `opacity: 0.6`. Never a border.

### Cards / Containers
- **Corner Style:** 10px standard, 16px featured
- **Background:** `var(--dark-mid)` — one tonal step above page bg
- **Elevation:** Border only (`1px solid var(--dark-border)`). No shadow at rest.
- **Internal Padding:** `clamp(1.5rem, 3vw, 2.25rem)` to `clamp(2rem, 4vw, 3rem)` depending on card prominence

### Navigation
- **Default:** `background: transparent`, no border
- **Scrolled:** `background: oklch(0.225 0.010 115 / 0.85)`, `backdrop-filter: blur(20px)`, subtle bottom border
- **Links:** Geist 300, muted color → ink on hover. Active/current: ink. `touch-action: manipulation` for instant response.
- **Mobile:** Full-overlay panel from top, Montserrat 300 type, lime on hover

### Signature: Verification Step List
The "Small Gaps. Big Losses." section uses a vertical connected list with a `::before` pseudo-element line, grid-aligned icons (40×40px, 8px radius), and inline danger / neutral state variants. This pattern communicates sequential verification — it is not a generic feature list. Danger variant: `border-color: oklch(0.65 0.20 25 / 0.45)`, `background: oklch(0.20 0.020 25)`. Verified variant: standard border + `var(--dark-mid)`.

### Social FAB
Fixed bottom-right floating action button. 44×44px, `border-radius: 50%`. Trigger opens 3 social icon links fanned above (LinkedIn, Facebook, Instagram) with staggered entrance (0ms, 60ms, 120ms delay, bottom-up). Share icon → X icon on toggle. `scale(0.92)` active state, 80ms. Hidden until page scroll > 400px.

## Do's and Don'ts

### Do:
- **Do** use lime (`oklch(0.770 0.206 151)`) only on verified, approved, and actionable states — CTAs, cleared figures, confirmed icons.
- **Do** use negative letter-spacing on all Montserrat headings (`-0.025em` minimum at section-heading scale).
- **Do** keep section-opening padding to exactly two tiers: `clamp(5rem, 10vw, 8rem)` for standard, `clamp(7rem, 14vw, 10.5rem)` for hero-scale.
- **Do** use the tonal stack (audit-night → surface → border) for depth. Three steps only.
- **Do** give all interactive elements `touch-action: manipulation` and `:active { transform: scale(0.97); transition: 80ms }`.
- **Do** use SVG geometry icons at 18px, 1.4–1.5px stroke-weight, authored consistently.

### Don't:
- **Don't** use lime decoratively — no lime dividers, backgrounds, section accents, or hover treatments unrelated to approval states.
- **Don't** apply `translateY(-Xpx)` on button hover. Position change is reserved for the active/press state only.
- **Don't** use gradient text or colored `border-left` on cards, list items, or callouts.
- **Don't** place an eyebrow/kicker label above a section heading — the heading carries its own weight.
- **Don't** add box-shadow to static card surfaces. Border defines the card; shadow is reserved for floating elements only.
- **Don't** use Montserrat for body copy or at sizes below 18px. Geist owns all running prose and data.
- **Don't** combine lime and danger red in the same visual field at the same hierarchy level. The system communicates binary outcomes — verified or not.
