# Mentat Design System v1.0

## Purpose

The Mentat design system creates a consistent visual language across:

- website
- articles
- LinkedIn carousels
- presentations
- diagrams
- documentation
- future applications

The objective is recognition through consistency.

Every artefact should feel like part of the same system.

---

# Design Philosophy

## Quiet Confidence

The design should communicate:

- intelligence
- precision
- craftsmanship
- technical depth

Avoid visual noise.

Avoid unnecessary decoration.

---

# Design Principles

## 1. Clarity First

Every visual decision should improve understanding.

Design serves communication.

---

## 2. Structure Through Design

Visual hierarchy should make thinking visible.

Use:

- spacing
- typography
- alignment
- grouping
- diagrams

to reveal structure.

---

## 3. Consistency Compounds

Repeated patterns create recognition.

Reuse components rather than creating new styles.

---

# Typography

## Primary Heading Font

Georgia

Usage:

- page titles
- major statements
- key messages
- article headlines

Purpose:

Create a distinctive editorial feel.

---

## Body Font

Inter (preferred), with a system sans-serif fallback.

Fallback stack: -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif.

Usage:

- paragraphs
- explanations
- descriptions
- supporting text

Purpose:

Clean, accessible readability with a more precise, contemporary tone than Arial. The system fallback keeps pages fast and dependency-free.

---

## Technical Font

Monospace font.

Preferred:

JetBrains Mono

Usage:

- code
- technical examples
- specifications
- terminal content

---

# Typography Rules

Create strong hierarchy.

Prefer:

- large titles
- short sections
- generous spacing
- clear contrast

Avoid:

- excessive font variations
- decorative typography
- dense text blocks

---

# Colour System

## Philosophy

Minimal colour.

A neutral foundation with a distinctive accent.

Colour should communicate meaning.

Never use colour only as decoration.

---

## Foundation

Use:

- white
- off-white
- charcoal
- grey tones

for backgrounds and text.

---

## Accent

Use one primary accent colour.

Purpose:

Highlight:

- important concepts
- key decisions
- actions
- relationships

Avoid multiple competing colours.

---

# Icon System

## Role of Icons

Icons are a core part of the Mentat identity.

They should help people understand concepts faster.

They are not decoration.

---

## Icon Style

Use:

- simple outline icons
- consistent stroke width
- geometric shapes
- minimal detail

---

## Icon Usage

Icons should represent:

- concepts
- frameworks
- system components
- processes
- categories

Prefer one meaningful icon over many decorative elements.

---

# Layout Principles

## Grid Based

Use consistent alignment.

Every element should have a reason for its position.

---

## Generous White Space

Whitespace creates:

- focus
- hierarchy
- calm

Avoid overcrowded layouts.

---

## One Main Idea Per View

Each page, slide or carousel frame should communicate one primary message.

---

# Component Library

## Knowledge Card

Used for:

- concepts
- principles
- frameworks

---

## Framework Block

Used for:

- models
- decision structures
- methodologies

---

## Architecture Diagram

Used for:

- systems
- workflows
- technical explanations

---

## Callout

Used for:

- key insights
- principles
- decisions

---

## Comparison Table

Used for:

- trade-offs
- options
- evaluations

---

## Timeline

Used for:

- evolution
- processes
- lifecycle explanations

---

# LinkedIn Carousel System

## Purpose

Transform knowledge assets into consistent social artefacts.

---

## Slide Structure

### Slide 1

Strong statement.

Large title.

Clear visual hook.

---

### Slides 2-N

One idea per slide.

Use:

- diagrams
- frameworks
- examples

Minimise paragraphs.

---

### Final Slide

Include:

- key takeaway
- reference to Mentat
- personal identity

---

# Website Design

The website should feel like a knowledge system.

Primary sections:

- Thinking
- Knowledge
- Building
- Projects
- Speaking
- About

---

# Diagram Style

Diagrams should be:

- simple
- structured
- clearly labelled
- consistent

Prefer:

- boxes
- arrows
- layers
- flows

Avoid unnecessary complexity.

---

# Accessibility

All artefacts should consider:

- readability
- contrast
- hierarchy
- responsive layouts

Good design improves access to knowledge.

---

# Design Principle

The purpose of design is not to attract attention.

The purpose of design is to make knowledge easier to understand, remember and reuse.

---

# Design Tokens

This section is the canonical source for all concrete brand values. Artefacts consume these values. The machine-readable version lives in `brand/assets/tokens.css` and must be kept in sync with the table below.

## Colour

Positioning: calm, precise, quiet confidence, with a bright electric signal. A warm neutral foundation with a single accent used in two tones.

| Token | Hex | Role |
|---|---|---|
| `--paper` | `#F7F6F2` | Page background, warm off-white |
| `--surface` | `#FFFFFF` | Cards and raised surfaces |
| `--ink` | `#1A1D21` | Primary text |
| `--charcoal` | `#22262B` | Headings |
| `--muted` | `#6B7178` | Secondary text, captions |
| `--line` | `#E3E1DB` | Borders and dividers |
| `--accent` | `#00A2FF` | Bright electric signal |
| `--accent-dark` | `#003E7A` | Deep companion for interactive and text |
| `--accent-tint` | `#E0F1FF` | Accent background wash |

One accent family only. Do not introduce competing colours.

The accent is a two-tone pair, split by function so the bright colour stays eye-catching while text stays legible.

- Bright `--accent`: logo mark, icon accents on white, highlight markers, focus states, decorative rules. Do not use it for small text or white-on-accent buttons, where it fails contrast.
- Deep `--accent-dark`: text links, buttons with white text, small labels and eyebrows, hover. Use this wherever the accent must be readable.
- `--accent-tint`: soft backgrounds for icon tiles and highlight chips, paired with a deep glyph.

## Typography Scale

Base size 16px. Display and headings use Georgia. Body uses Inter with a system fallback. Code uses JetBrains Mono with a monospace fallback.

| Token | Size | Line height | Weight | Use |
|---|---|---|---|---|
| `--text-display` | 3rem | 1.1 | 400 | Hero statements |
| `--text-h1` | 2.25rem | 1.15 | 600 | Page titles |
| `--text-h2` | 1.5rem | 1.25 | 600 | Section headings |
| `--text-h3` | 1.125rem | 1.3 | 600 | Sub headings |
| `--text-body` | 1rem | 1.6 | 400 | Paragraphs |
| `--text-small` | 0.875rem | 1.5 | 400 | Captions, meta |
| `--text-mono` | 0.9375rem | 1.5 | 400 | Code, technical |

## Spacing

4px base unit. Use only these steps.

| Token | Value |
|---|---|
| `--space-1` | 4px |
| `--space-2` | 8px |
| `--space-3` | 12px |
| `--space-4` | 16px |
| `--space-5` | 24px |
| `--space-6` | 32px |
| `--space-7` | 48px |
| `--space-8` | 64px |
| `--space-9` | 96px |

## Radius, Border and Elevation

| Token | Value | Use |
|---|---|---|
| `--radius-sm` | 4px | Buttons, tags |
| `--radius` | 6px | Cards, panels |
| `--border` | 1px solid `--line` | Default separation |
| `--shadow` | 0 1px 2px rgba(0,0,0,0.04) | Minimal elevation |

Prefer borders over shadows. Elevation is a last resort, not a default.

## Layout

| Token | Value | Use |
|---|---|---|
| `--container` | 1080px | Max page width |
| `--measure` | 68ch | Max text line length |

---

# Icon Library

Icons are a core part of the Mentat identity. They are outline, geometric and consistent. They label concepts, never decorate.

## Specification

- Canvas: 24 by 24 viewBox
- Style: outline only, no fills
- Stroke: 1.75px, round caps, round joins
- Colour: `currentColor`, so icons inherit text or accent colour. On light backgrounds render glyphs in `--accent-dark` for legibility.
- Detail: minimal, one clear idea per icon

## Assets

Individual SVG files live in `brand/assets/icons/`. A preview gallery is at `brand/assets/icons/index.html`.

| Icon | File | Represents |
|---|---|---|
| Thinking | `thinking.svg` | Frameworks, mental models, perspectives |
| Building | `building.svg` | Systems, implementations, experiments |
| Knowledge | `knowledge.svg` | Captured, structured knowledge |
| AI engineering | `ai.svg` | Intelligent systems |
| Governance | `governance.svg` | Reliability, responsibility, control |
| Framework | `framework.svg` | Models, decision structures |
| Concept | `concept.svg` | Single ideas and nodes |
| Principle | `principle.svg` | Direction and standards |
| Architecture | `architecture.svg` | Layered systems |
| Connect | `connect.svg` | Relationships between assets |
| Timeline | `timeline.svg` | Evolution, lifecycle, process |
| Reuse | `reuse.svg` | Transformation into many artefacts |
| Callout | `callout.svg` | Key insights and notes |
| Search | `search.svg` | Discovery and retrieval |

## Usage

Reference an icon inline and set its size and colour with CSS.

```html
<svg class="icon" width="24" height="24" aria-hidden="true">
  <use href="brand/assets/icons/icons.svg#thinking"></use>
</svg>
```

Or embed a single file directly. Keep stroke and viewBox unchanged so all icons stay visually consistent.
