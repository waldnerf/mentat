# Mentat Website: Home Page

## Status

Canonical source. Version 1.0.

The generated artefact is `artefacts/published/index.html`. When this file changes, regenerate the artefact. Do not edit the HTML as the source of truth.

---

# Purpose

Introduce Mentat as a personal knowledge operating system and demonstrate a way of thinking, not a brand around technology.

The home page should make a first-time visitor understand, in one screen, what Mentat is and why it is different: knowledge is created once, artefacts are generated many times.

---

# Audience

Primary: AI leaders, technology executives, architects, engineers, consultants, builders.

Secondary: professionals interested in structured thinking, and organisations adopting AI.

---

# Key Message

Knowledge is created once. Artefacts are generated many times.

The canonical Markdown knowledge asset is the source of truth. Derived outputs are generated from that source.

---

# Design Reference

The page consumes the Mentat design tokens.

- Tokens: `brand/assets/tokens.css` (canonical values in `brand/03-Design-System.md`)
- Icons: `brand/assets/icons/`
- Voice: `brand/02-Writing-Standards.md`

For a self-contained deployed artefact, the tokens and the icons used on the page are inlined into the HTML. The canonical source remains in `brand/`.

---

# Structure

The page presents one primary message per view, top-down, with generous white space and a single accent colour.

## 1. Header

- Wordmark: Mentat, with the M mark.
- Navigation: Thinking, Knowledge, Building, About. Anchors to sections on this page in version 1.0.

## 2. Hero

- Eyebrow: Personal knowledge operating system.
- Heading: Knowledge is created once. Artefacts are generated many times.
- Supporting line: Mentat is a Markdown-first system for thinking, building and sharing reusable knowledge. It turns ideas into structured knowledge assets, and structured knowledge into practical systems.
- Actions: Explore the system (primary), About Mentat (secondary).

## 3. Guiding Statement Strip

Think clearly. Build systematically. Share knowledge. Create systems that compound.

## 4. Content Pillars

Section intro: Five areas of a single body of work. Every artefact belongs to one system. Consistency compounds recognition over time.

Cards, each with one icon:

1. Thinking. Frameworks, mental models and perspectives that make complexity understandable.
2. Building. Systems, architectures, experiments and implementations that put ideas to work.
3. Knowledge systems. Methods for capturing, structuring and evolving knowledge that lasts.
4. AI engineering. Practical approaches to building intelligent systems that are reliable in use.
5. Governance. Making technology reliable, scalable and responsible as it grows.

## 5. The Mentat Flow

Section intro: One deliberate path from idea to reuse. Not every thought becomes an asset. Every published idea originates from a deliberate thinking process.

Steps:

1. Idea. Capture the thought without forcing structure.
2. Knowledge asset. Structure it into a reusable, canonical Markdown source.
3. Artefacts. Generate many expressions from one source of truth.
4. Published. Share, gather feedback, and improve the system.

## 6. About

Heading: A way of thinking, not a brand around technology.

Body: Mentat optimises for clarity over volume, systems over isolated outputs, and reuse over reinvention. The canonical Markdown knowledge asset is the source of truth. Derived outputs, from websites to presentations to talks, are generated from that source and regenerated as it improves.

Values as tags: Clarity, Structure, Practicality, Craftsmanship, Reusability, Consistency.

## 7. Footer

- Mentat, a knowledge operating system.
- Built Markdown-first. Version 1.0.

---

# Regeneration Notes

When this source changes:

1. Update the copy or structure here first.
2. Regenerate `artefacts/published/index.html` to match, keeping the design tokens and icon style unchanged.
3. Commit the source and the regenerated artefact together.

---

# Future Sections

Version 1.0 is a single page. Planned expansion, when the underlying knowledge exists to support it:

- Thinking: published frameworks and models.
- Knowledge: selected canonical assets.
- Building: projects and systems.
- Speaking: talks and workshops.

These should be added only when real knowledge assets exist to link to.
