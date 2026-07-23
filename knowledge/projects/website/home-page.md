# Mentat Website: Home Page

## Status

Canonical source. Version 2.0, Marginalia (Ascetic) direction.

The generated artefact is `artefacts/published/index.html`. When this file changes, regenerate the artefact. Do not edit the HTML as the source of truth.

---

# Purpose

Introduce Mentat as a personal knowledge operating system and demonstrate a way of thinking, not a brand around technology. A first-time visitor should understand in one screen what Mentat is: knowledge is created once, artefacts are generated many times.

---

# Audience

Primary: AI leaders, technology executives, architects, engineers, consultants, builders.

Secondary: professionals interested in structured thinking, and organisations adopting AI.

---

# Design Reference

Built in the Marginalia direction. See `brand/03-Design-System.md`.

- Tokens: `brand/assets/tokens.css`
- Type: Archivo (loaded from Google Fonts), JetBrains Mono for code
- Accent: `--pen` ultramarine, used only for the tick, links, focus and the active nav item
- No cards, no marketing buttons, no shadows, radius 0. Hierarchy from space, scale and one rule line.
- Theme: defaults to the operating system preference. A visible Light/Dark toggle sits in the header (top of page) and remembers the choice (localStorage, degrades gracefully).
- Measure: v2.0 site decision. The hero and body fill the 720px content column, loosening the tight measure in design system sections 3 and 9. The empty right side is not used on this page.

The tokens used on the page are inlined into the HTML so the deployed artefact is self-contained. The canonical source remains in `brand/`.

---

# Structure

Left-aligned to the 720px content column. The rail carries the tick and the descriptor. The empty right side of the hero is intentional and must not be filled.

## Header

- Wordmark: the Mentat long logo (`brand/assets/logo/MENTAT-long-light.png` on light grounds, `MENTAT-long-dark.png` on dark), inlined as a base64 data URI in the header at ~20px tall, swapped by theme. Replaces the plain Archivo text wordmark.
- Right slot: an "AI vocabulary" link (to the sister page `ai-concepts-wordcloud.html`), the "About" link, and a Light/Dark theme toggle (a two-option control, active state marked). This overrides the design system's "single link right" for this page.

## Rail

- The tick at the top: a 16 by 2px ultramarine bar.
- Descriptor in caption style: "Personal knowledge operating system".
- Meta line: "Markdown-first. One source.".

## Hero

- Display line (display-l, weight 200), with "generated many times" stepped to weight 500: "Knowledge is created once. Artefacts are generated many times."
- Standfirst (body-l): "A system for thinking, building and sharing reusable knowledge. It turns ideas into structured knowledge assets, and structured knowledge into practical systems."
- Actions: primary text link "Explore the system"; secondary text "About Mentat".

## Guiding statement

One line, ink: "Think clearly. Build systematically. Share knowledge. Create systems that compound."

## Content pillars

Section rule above. Opener "Content pillars". Five pillars as ruled text, each a name and one line, separated by faint rules. No cards.

1. Thinking. Frameworks, mental models and perspectives that make complexity understandable.
2. Building. Systems, architectures, experiments and implementations that put ideas to work.
3. Knowledge systems. Methods for capturing, structuring and evolving knowledge that lasts.
4. AI engineering. Practical approaches to building intelligent systems that are reliable in use.
5. Governance. Making technology reliable, scalable and responsible as it grows.

## The Mentat flow

Section rule above. Opener "The Mentat flow". Four steps as ruled text: Idea, Knowledge asset, Artefacts, Published. No boxes.

## Selected artefact

Section rule above. Opener "Selected artefact". One row linking to the Enterprise AI vocabulary sister page (`ai-concepts-wordcloud.html`): a reviewed C-level map of the 79 concepts leaders need, sized by importance and grouped into five families. The copy makes the case for keeping the AI vocabulary current: when the language drifts, so does the ability to question and govern decisions framed in it. Generated from `knowledge/projects/enterprise-ai-concepts/enterprise-ai-concepts-curated.md`. Demonstrates the one-source-many-artefacts thesis in place.
