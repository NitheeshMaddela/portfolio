---
name: Nitheesh Maddela
description: Graphite engineering studio portfolio
colors:
  accent: "#e6a17c"
  accent-hover: "#f4bb99"
  on-accent: "#181b1f"
  paper: "#14171b"
  ink: "#edf0f4"
  secondary: "#a6b0bb"
  wash: "#1d2229"
  line: "#3b4652"
  line-strong: "#687786"
  selection: "#634534"
  workflow-bg: "#222a33"
  workflow-text: "#d4dbe3"
typography:
  display: {fontFamily: "Hanken Grotesk, Segoe UI, sans-serif", fontSize: "clamp(3rem, 7.6vw, 6rem)", fontWeight: 550, lineHeight: 1.08, letterSpacing: "-0.04em"}
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
  button-primary: {backgroundColor: "{colors.accent}", textColor: "{colors.on-accent}", rounded: "{rounded.square}", padding: "14px 24px"}
  button-primary-hover: {backgroundColor: "{colors.accent-hover}"}
  button-primary-active: {backgroundColor: "{colors.ink}"}
  button-menu: {textColor: "{colors.ink}", padding: "10px 14px"}
  input: {backgroundColor: "{colors.paper}", textColor: "{colors.ink}", rounded: "{rounded.square}", padding: "12px"}
  architecture: {backgroundColor: "{colors.wash}", padding: "32px 40px 24px"}
---

# Design System: Nitheesh Maddela

## Overview

**Creative North Star: "Independent engineering studio — graphite edition"**

The graphite edition preserves the studio’s broad name masthead, open asymmetric project spreads and compact career rows. Graphite surfaces, silver typography and restrained copper accents express the user’s requested technical direction. Hanken Grotesk remains the display and reading face; actual system diagrams carry the technical detail.

The material is flat and direct: square controls, plain technology lists and restrained state changes. The current implementation uses HTML and inline SVG rather than raster imagery. The user selected this world after rejecting the previous AI-generated appearance; gradients, badges and generic card layouts are not binding.

**Key Characteristics:**

- Graphite surfaces, silver text and copper actions and technical emphasis.
- One locally served type family with a strong display-to-body contrast.
- Open spreads, fine rules and square controls.
- Native disclosure and diagrams of actual system stages.

<!-- Source-derived from index.html; refreshed for the user-approved graphite/silver/copper refinement. Rendered screenshots and computed-style inspection remain unavailable. Surface review disposition: recapture; this document is not whole-surface ship approval. -->

## Colors

Graphite and silver support copper as the action and technical-emphasis color. Frontmatter owns the exact values. The user explicitly selected this dark treatment; print output remains light.

### Primary

- **Copper / Light Copper:** Primary actions, links, active navigation, outcome figures and retrieval emphasis; Light Copper is the primary hover state.
- **On Copper:** Dark text on the filled copper actions.

### Neutral

- **Graphite / Silver:** Page and input surfaces; main reading and heading text.
- **Secondary Silver:** Supporting copy, dates and stack information.
- **Raised Graphite / Technical Graphite:** Architecture, contact and agent-workflow surfaces.
- **Quiet Rule / Strong Rule:** Content dividers and readable component and diagram boundaries.
- **Copper Selection:** Selected text background, paired with Silver.
- **Workflow Silver:** Supporting text on the agent workflow.

**The Copper Emphasis Rule.** Reserve copper for actions, links, current navigation, measured outcomes and meaningful retrieval emphasis; reading copy stays silver or secondary silver.

## Typography

**Display Font:** Hanken Grotesk (Segoe UI, sans-serif fallbacks).
**Body Font:** Hanken Grotesk (same fallbacks).

The variable font is locally served from `assets/fonts/HankenGrotesk-Variable.ttf`, preloaded, with weights (100–900) and `font-display: swap`. Scale and weight distinguish roles. A system monospace stack is limited to actual technology strings, dates and measured outcomes; ordinary copy and headings retain Hanken Grotesk. The frontmatter records the reused desktop roles.

The mobile name uses (`clamp(3rem, 12vw, 5.5rem)`) and a narrow measure (9ch). Secondary project titles use (`clamp(1.75rem, 2.5vw, 2.1rem)`); contact headings use (`clamp(2rem, 3.5vw, 3rem)`). Reading copy generally stays within (64–72ch), with supporting text from (0.8rem) to (1.08rem). Dates and outcome figures use tabular numerals. Text keeps natural case.

**The Single Family Rule.** Use Hanken Grotesk for display, reading copy and controls. Reserve system monospace for actual technology strings, dates and measured outcomes.

## Layout

The centered container has a maximum width (1184px) and fluid gutters (`clamp(24px, 5vw, 80px)`). The spacing scale is in frontmatter. Main spreads use unequal columns (5fr / 7fr) with a usual gap (72px); the second project reverses them. Career rows use (3fr / 9fr), expertise rows (4fr / 8fr), and credentials two equal columns. Section openings use a Strong Rule top border (1px), top padding (32px) and space below (40px).

At (1000px), main column gaps become (40px), architecture padding becomes (24px) and the workflow becomes vertical. At (760px), major grids stack with (32px) gaps, reversed projects return to document order, career rows stack, and the JavaScript-enabled menu appears. The workflow remains vertical at narrower widths. At (420px), form rows stack; metric and evaluation label columns narrow. These behaviors still need rendered confirmation.

The desktop header is sticky; on mobile it is sticky only with JavaScript. Without JavaScript navigation remains visible in normal flow. Print styles hide navigation and the form, expand the container and avoid splitting project, career and credential groups.

## Elevation & Depth

There are no shadows. Whitespace, rules and graphite, raised graphite and workflow fields separate content. Positioned mobile navigation uses a bottom rule without an elevation effect.

**The Flat Surface Rule.** Use whitespace, rules and tonal fields to separate content. The implemented system has no shadows.

## Shapes

Controls, fields, diagram stages and evidence regions use square geometry. Inputs and the primary button explicitly set zero radius. Rules and diagram connectors are (1px). Inline stroke SVGs (18px) use rounded stroke ends; container geometry stays square.

## Components

### Buttons

Square, direct actions. The primary button uses Copper and On Copper, medium weight (500), minimum height (48px), and frontmatter padding. Hover uses Light Copper; active uses Silver with dark text. The transparent Menu control uses a Strong Rule border and minimum height (44px). Text links use copper and a stroke SVG. Links, buttons and summaries have a copper focus outline (2px), offset (5px).

### Cards / Containers

Open spreads have no surrounding border, radius or shadow. Architecture uses Raised Graphite with page-colored stages, strong outlines and precise connector ports. Retrieval has copper emphasis and parallel BM25/vector paths. The agent workflow uses Technical Graphite, silver text and internal rules. Career history uses ruled rows rather than enclosing cards.

### Inputs / Fields

Graphite, square fields have a Strong Rule border (1px), visible labels and Secondary Silver placeholders. Focus uses a copper outline (2px), offset (2px). The textarea resizes vertically with a minimum height (140px). Validation is native; no custom disabled or error treatment is defined. The form opens an email draft and keeps that explanation visible.

### Navigation

Plain links use (0.92rem) text and a minimum height (44px). Current-section links use copper and an underline. The header resume link has a Strong Rule outline; the introductory resume action is filled copper. The mobile menu uses vertical links with minimum height (48px); the live script updates expanded state and closes on selection or Escape.

A locally served, pinned Lenis (1.3.27) instance smooths wheel and trackpad input with interpolation (0.12); touch scrolling stays native. Nested scrolling and zoom gestures are preserved. Section links use the same engine with distance-based timing (900–2200ms), cubic ease-in-out and the CSS scroll-padding value to clear the sticky header. Pointer input, keyboard scrolling and history navigation cancel inertia. Reduced-motion preferences and the skip link use immediate navigation. Hash history and keyboard focus follow the selected section. If the library is unavailable, section links fall back to native browser smooth scrolling.

### Project Disclosure

Native details and summary use a top rule and a minimum summary height (56px). The inline SVG plus rotates (45deg) when open over (240ms) with the shared easing curve. Reduced motion removes this transition and smooth scrolling. Essential project scope stays visible before expansion.

### Architecture Diagram

Actual processing stages form a vertical text list with gaps (28px), narrow connectors, connection ports and a figure caption. Hybrid retrieval exposes parallel lexical BM25 and semantic vector paths. HTML and CSS provide the geometric diagram; no raster imagery is used.

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
