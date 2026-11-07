---
name: Nitheesh Maddela
description: Independent engineering studio portfolio
colors:
  rust: "#a13f2b"
  rust-dark: "#7f2f20"
  paper: "#ffffff"
  ink: "#252522"
  secondary: "#62625c"
  wash: "#f1f1ed"
  line: "#d6d6ce"
  selection: "#f1d4c7"
  field-border: "#92928a"
  review-line: "#53534c"
  review-muted: "#d3d3c8"
typography:
  display: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "clamp(3rem, 7.6vw, 6rem)", fontWeight: 600, lineHeight: 1.08, letterSpacing: "-0.04em"}
  headline: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "1.8rem", fontWeight: 600, lineHeight: 1.2, letterSpacing: "-0.025em"}
  project-title: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "clamp(2rem, 3vw, 2.75rem)", fontWeight: 600, lineHeight: 1.15, letterSpacing: "-0.03em"}
  career-title: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "1.25rem", fontWeight: 600, lineHeight: 1.35, letterSpacing: "-0.015em"}
  body: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "1rem", fontWeight: 400, lineHeight: 1.65}
  label: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "0.9rem", fontWeight: 400, lineHeight: 1.65}
rounded:
  square: "0"
spacing:
  space-1: "8px"
  space-2: "16px"
  space-3: "24px"
  space-4: "32px"
  space-5: "48px"
  space-6: "72px"
  space-7: "104px"
components:
  button-primary: {backgroundColor: "{colors.rust}", textColor: "{colors.paper}", rounded: "{rounded.square}", padding: "14px 24px"}
  button-primary-hover: {backgroundColor: "{colors.rust-dark}"}
  button-primary-active: {backgroundColor: "{colors.ink}"}
  button-menu: {textColor: "{colors.ink}", padding: "10px 14px"}
  input: {backgroundColor: "{colors.paper}", textColor: "{colors.ink}", rounded: "{rounded.square}", padding: "12px"}
  architecture: {backgroundColor: "{colors.wash}", padding: "32px 40px 24px"}
---

# Design System: Nitheesh Maddela

## Overview

**Creative North Star: "Independent engineering studio"**

The Independent engineering studio uses white, charcoal and rust with a broad name masthead, open asymmetric project spreads and compact career rows. Hanken Grotesk carries both display and reading text. Rules, spacing and real system diagrams establish hierarchy.

The material is flat and direct: square controls, plain technology lists and restrained state changes. The current implementation uses HTML and inline SVG rather than raster imagery. The user selected this world after rejecting the previous AI-generated appearance; gradients, badges and generic card layouts are not binding.

**Key Characteristics:**

- White surfaces, charcoal text and rust emphasis.
- One locally served type family with a strong display-to-body contrast.
- Open spreads, fine rules and square controls.
- Native disclosure and diagrams of actual system stages.

<!-- Source-derived from index.html. Rendered screenshots and computed-style inspection remain unavailable. Surface review disposition: recapture; this document is not whole-surface ship approval. -->

## Colors

White and warm charcoal give rust a clear role as the single action and emphasis color. Frontmatter owns the exact values.

### Primary

- **Rust:** Links, primary action, current navigation, employers, outcome figures and retrieval-stage emphasis.
- **Deep Rust:** Primary button hover.

### Neutral

- **White Paper / Warm Charcoal:** Page and field surfaces; main text and the dark workflow field.
- **Secondary Gray:** Reading copy, metadata and diagram connectors.
- **Pale Wash / Quiet Line:** Architecture and contact backgrounds; fine dividers and stage borders.
- **Selection Peach / Field Gray:** Text selection background and form-field borders.
- **Review Divider / Review Text:** Separators and supporting text on the dark workflow field.

**The Rust Emphasis Rule.** Use rust for links, current navigation, selected technical emphasis and the primary action; keep reading text charcoal or secondary gray.

## Typography

**Display Font:** Hanken Grotesk (Segoe UI, sans-serif fallbacks).
**Body Font:** Hanken Grotesk (same fallbacks).

The variable font is locally served from `assets/fonts/HankenGrotesk-Variable.ttf`, preloaded, with weights (100–900) and `font-display: swap`. Scale and weight distinguish roles; no separate mono face is used. The frontmatter records the reused desktop roles.

The mobile name uses (`clamp(3rem, 12vw, 5.5rem)`) and a narrow measure (9ch). Secondary project titles use (`clamp(1.75rem, 2.5vw, 2.1rem)`); contact headings use (`clamp(2rem, 3.5vw, 3rem)`). Reading copy generally stays within (64–72ch), with supporting text from (0.8rem) to (1.08rem). Dates and outcome figures use tabular numerals. Text keeps natural case.

**The Single Family Rule.** Use Hanken Grotesk across display, body and controls; distinguish roles through scale, weight and spacing.

## Layout

The centered container has a maximum width (1184px) and fluid gutters (`clamp(24px, 5vw, 80px)`). The spacing scale is in frontmatter. Main spreads use unequal columns (5fr / 7fr) with a usual gap (72px); the second project reverses them. Career rows use (3fr / 9fr), expertise rows (4fr / 8fr), and credentials two equal columns. Section openings use a charcoal top rule (1px), top padding (32px) and space below (40px).

At (1000px), main column gaps become (40px), architecture padding becomes (24px) and the workflow becomes vertical. At (760px), major grids stack with (32px) gaps, reversed projects return to document order, career rows stack, and the JavaScript-enabled menu appears. The workflow returns to three columns at this width. At (420px), workflow and form rows stack; metric and evaluation label columns narrow. These behaviors still need rendered confirmation.

The desktop header is sticky; on mobile it is sticky only with JavaScript. Without JavaScript navigation remains visible in normal flow. Print styles hide navigation and the form, expand the container and avoid splitting project, career and credential groups.

## Elevation & Depth

There are no shadows. Whitespace, rules and white, wash and charcoal fields separate content. Positioned mobile navigation uses a bottom rule without an elevation effect.

**The Flat Surface Rule.** Use whitespace, rules and tonal fields to separate content. The implemented system has no shadows.

## Shapes

Controls, fields, diagram stages and evidence regions use square geometry. Inputs and the primary button explicitly set zero radius. Rules and diagram connectors are (1px). Inline stroke SVGs (18px) use rounded stroke ends; container geometry stays square.

## Components

### Buttons

Square, direct actions. The primary button uses Rust and White Paper, medium weight (500), minimum height (48px), and frontmatter padding. Hover uses Deep Rust; active uses Warm Charcoal. The transparent Menu control uses a Quiet Line border and minimum height (44px). Text links use rust and a stroke SVG. Links, buttons and summaries have a rust focus outline (2px), offset (5px).

### Cards / Containers

Open spreads have no surrounding border, radius or shadow. Architecture uses Pale Wash with white, fine-bordered stages; retrieval gets rust emphasis. The workflow uses charcoal with white text, muted descriptions and internal rules. Career history uses ruled rows rather than enclosing cards.

### Inputs / Fields

White, square fields have a Field Gray border (1px), visible labels and Secondary Gray placeholders. Focus uses a rust outline (2px), offset (2px). The textarea resizes vertically with a minimum height (140px). Validation is native; no custom disabled or error treatment is defined. The form opens an email draft and keeps that explanation visible.

### Navigation

Plain links use (0.92rem) text and a minimum height (44px). Current-section links use rust and an underline. The mobile menu uses vertical links with minimum height (48px); the live script updates expanded state and closes on selection or Escape.

A locally served, pinned Lenis (1.3.27) instance smooths wheel and trackpad input with interpolation (0.12); touch scrolling stays native. Nested scrolling and zoom gestures are preserved. Section links use the same engine with distance-based timing (900–2200ms), cubic ease-in-out and the CSS scroll-padding value to clear the sticky header. Pointer input, keyboard scrolling and history navigation cancel inertia. Reduced-motion preferences and the skip link use immediate navigation. Hash history and keyboard focus follow the selected section. If the library is unavailable, section links fall back to native browser smooth scrolling.

### Project Disclosure

Native details and summary use a top rule and a minimum summary height (56px). The inline SVG plus rotates (45deg) when open over (240ms) with the shared easing curve. Reduced motion removes this transition and smooth scrolling. Essential project scope stays visible before expansion.

### Architecture Diagram

Actual processing stages form a vertical text list with gaps (28px), narrow connectors and a figure caption. HTML and CSS provide the geometric diagram; no raster imagery is used.

## Do's and Don'ts

### Do:

- **Do** use the locally served Hanken Grotesk family and the established token palette.
- **Do** let project evidence occupy open grid columns and let career content sit in compact ruled rows.
- **Do** preserve visible keyboard focus, labeled fields and native disclosure behavior.
- **Do** show actual processing stages when using architecture diagrams.
- **Do** collapse grids at the implemented breakpoints and honor reduced motion.

### Don't:

- **Don't** introduce decorative gradients, badge collections or repeated generic cards as the default content structure.
- **Don't** add rounded or shadowed controls to this square, flat system.
- **Don't** substitute invented project imagery, clients or benchmarks for real evidence.
- **Don't** hide essential project scope inside disclosures.
