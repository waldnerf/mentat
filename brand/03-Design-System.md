# Mentat Design System v2.0

Direction 05 · Ascetic. Internal name for the design language: Marginalia.

Source: this file is the canonical brand and design source. Artefacts are generated from it. The machine-readable tokens live in `brand/assets/tokens.css` and must be kept in sync with section 10.

---

# 1. Brand idea

Mentat is mental discipline applied to knowledge. A mentat is a human trained to think without instruments. The brand should look like that: no ornament, no apparatus, nothing on the page that is not load-bearing.

Governing principle: hierarchy comes from space, scale and one rule line. Not from boxes, fills, shadows or colour.

The consequence: this system has no margin for sloppiness. There is no card, gradient or illustration to hide a spacing error behind. Every decision below is tight on purpose, and loosening any of them costs more here than it would in a busier system.

Three tests before anything ships:

1. If I remove this element, is meaning lost? If not, remove it.
2. Is this blue marking the one live thing on the screen? If it is marking a second, one of them is wrong.
3. Would this page still read correctly printed in one colour? It should.

---

# 2. Colour

Palette is stone, ink and a single pigment. The ground is deliberately cool. Ultramarine is a cold hue, and putting it on a warm cream ground is the exact failure mode this direction was built to avoid.

## Core tokens

| Token | Hex | Role |
|---|---|---|
| `--stone` | `#E6E8E6` | Page ground. The default surface. |
| `--stone-raised` | `#EFF0EE` | Rare. Inset blocks, code, table headers. |
| `--ink` | `#1F2124` | Display type, body headings, primary text. |
| `--ink-70` | `#3E4145` | Secondary body copy. |
| `--ink-55` | `#55585C` | Small text 14px or below, captions, rail copy. |
| `--ink-40` | `#6C6F73` | Type 16px and above only. Never below. |
| `--ink-20` | `#B7B9B7` | Disabled, placeholder. |
| `--rule` | `rgba(31,33,36,0.16)` | All divider and rail lines. |
| `--rule-faint` | `rgba(31,33,36,0.08)` | Table row separators. |
| `--pen` | `#26418F` | The accent. Ultramarine. |
| `--pen-hover` | `#1B3070` | Link hover only. |

## Accent rules, non-negotiable

`--pen` never fills an area larger than the tick mark. It exists in exactly four places:

1. The tick (section 7), once per page, at the head of the rail.
2. Link text and its 1px underline.
3. Focus rings.
4. Active nav item.

It is never a button fill, never a background, never a border on a container, never a heading colour, never used at partial opacity to make a tint. There is no secondary accent. If a state needs to be signalled and blue is taken, use weight or a rule, not another hue.

## Semantic states

Keep these desaturated so they never compete with `--pen`.

| Token | Hex | Notes |
|---|---|---|
| `--error` | `#8C2F2A` | Text and 1px rule only, never a filled banner. |
| `--success` | `#2E5D45` | Text only. |
| `--warn` | `#7A5A1E` | Text only. |

## Contrast

Verified against `--stone`:

- `--ink` 12.9:1, AAA
- `--ink-70` 8.4:1, AAA
- `--ink-55` 5.5:1, AA all sizes
- `--ink-40` 4.1:1, large text only (16px, or 14px bold)
- `--pen` 7.6:1, AAA normal text

`--ink-40` is the one trap in this palette. It is the tone that looks right in a mockup and fails on an 11px rail label. Use `--ink-55` for anything small.

## Dark mode

Not a required deliverable, but if built: invert to charcoal, and lift the accent. `#26418F` fails on a dark ground.

| Token | Hex |
|---|---|
| `--stone` | `#1C1E1C` |
| `--stone-raised` | `#252725` |
| `--ink` | `#E6E8E6` |
| `--ink-55` | `#9DA0A2` |
| `--rule` | `rgba(230,232,230,0.16)` |
| `--pen` | `#7B9AE8` |

---

# 3. Typography

One family. The personality comes from the weight range, not from a pairing.

Display and UI: Archivo (variable, 100 to 900). Google Fonts, Open Font License.

Utility mono: Commit Mono, fallback `ui-monospace, "JetBrains Mono", monospace`. Used only for file paths, code, frontmatter and data. Never for headings, eyebrows or decoration. Markdown is the product's substrate; mono should look like the substrate, not like styling.

Fallback stack: `Archivo, "Helvetica Neue", Inter, system-ui, sans-serif`

## Scale

| Style | Size / line-height | Weight | Tracking | Use |
|---|---|---|---|---|
| `display-xl` | 76 / 0.98 | 200 | -0.038em | Homepage hero only. One per site. |
| `display-l` | 60 / 1.02 | 200 | -0.035em | Section openers, key pages. |
| `display-m` | 40 / 1.08 | 200 | -0.030em | Sub-openers. Floor for weight 200. |
| `h1` | 32 / 1.15 | 300 | -0.025em | Article titles. |
| `h2` | 24 / 1.25 | 400 | -0.020em | |
| `h3` | 18 / 1.35 | 500 | -0.010em | |
| `body-l` | 17 / 1.70 | 300 | 0 | Standfirsts, hero sub. |
| `body` | 15 / 1.70 | 300 | 0 | Default. |
| `small` | 13 / 1.60 | 400 | 0 | Notes, metadata. |
| `caption` | 11 / 1.70 | 500 | +0.04em, uppercase | Rail labels only. |
| `mono` | 13 / 1.70 | 400 | 0 | Code, paths, frontmatter. |

## Weight rules

Weight is the primary hierarchy device in this system, so it is governed strictly:

- 200 only at 40px and above. Below that it disintegrates on low-DPI screens.
- 300 for 15 to 32px running text and headings.
- 400 to 500 for 14px and below and all UI labels.
- 600 and above for the wordmark only.
- No italics. Archivo's obliques are weak at 200 and the register is wrong for this brand. Emphasis is carried by weight 500 inside a 200-weight line. See the hero, where "generated many times" steps from 200 to 500.

## Measure

- Display: max 13ch. The hero must break across 2 to 3 lines; a single-line hero loses the gesture.
- Body: max 40ch in the content column, 62ch on long-form article pages.
- Rail: max 22ch.

## Manual line breaks

The hero and section openers use hard breaks, not auto-wrap. Balance the rag by hand. With three lines of 60px type and nothing else on the page, an ugly rag is the whole design.

---

# 4. Layout

## The rail

The signature structural device. A fixed left column separated from content by a single vertical `--rule` line, carrying the tick, the descriptor and any metadata. It is not a sidebar; it never contains navigation, actions or images. It holds only things that annotate the main column.

```
+------------------------------------------------------+
| Mentat                                     Enter ->   |   header, 22px top pad
+------------------------------------------------------+
|           |                                          |
| | tick    |  Knowledge is created                    |
|           |  once. Artefacts are                     |
| Personal  |  generated many times.                   |
| knowledge |                                          |
| operating |                                          |
| system    |  A system for thinking, building         |
|           |  and sharing reusable knowledge.         |
| Markdown- |                                          |
| first.    |  Explore the system      About Mentat    |
| One       |                                          |
| source.   |                                          |
|           |                                          |
+-----------+------------------------------------------+
  150px  38px           max 720px
  rail   gutter         content
```

## Grid

- Page max width 1180px, centred.
- Two tracks: rail 150px plus content 1fr, gutter 38px, rule on the rail's right edge.
- Content column max 720px. Do not let it stretch to fill 1180. The unused right side is the whitespace, and it is intentional.
- Horizontal page padding: 52px desktop, 24px mobile.

## Spacing scale

Coarser than a typical 4px scale, because this system spends its budget on air.

`4 · 8 · 12 · 16 · 24 · 38 · 64 · 96 · 152`

- Hero top padding: 78px. Hero bottom: 96px.
- Between display and standfirst: 40px.
- Between standfirst and actions: 44px.
- Between major page sections: 96px, or 152px at the fold.

## Breakpoints

| | Width | Behaviour |
|---|---|---|
| `sm` | below 640 | Rail collapses above content, vertical rule becomes a bottom rule. Display drops to 40px. |
| `md` | 640 to 900 | Rail 120px, display 48px. |
| `lg` | 900 and above | Full spec. |

At `sm` the tick stays. It is the one element that must survive every breakpoint.

---

# 5. Components

## Header

Wordmark left, single link right. No nav bar, no underline beneath the header, no background change. Height comes from 22px top padding, not a fixed value. On interior pages the right slot holds section links at `small`, active item in `--pen`.

## Links and actions

There are no buttons on marketing pages. Primary and secondary actions are both text; hierarchy comes from the underline.

- Primary: `--pen`, 14px/500, 1px solid `--pen` underline, 3px offset.
- Secondary: `--ink-40`, 14px/500, no underline, 26px to the left of primary.
- Hover: colour to `--pen-hover`, underline thickens to 2px. 160ms ease-out. No movement, no background.

Exception, application UI only. Forms and the product interface may use one filled action: `--ink` background, `--stone` text, radius 0, padding 11px 20px. Never `--pen` as a fill.

## Rules

- Vertical rail rule: 1px `--rule`, full height of the content block.
- Horizontal section rule: 1px `--rule`, full content width, 64px clearance above and below.
- Radius is 0 everywhere. No exceptions, including images and code blocks.
- No shadows. No borders on containers. No cards.

## Code and file paths

The one place mono appears. Inset block on `--stone-raised`, 16px padding, no border, no radius, no traffic-light chrome. Inline paths get `--stone-raised` background with 2px horizontal padding and no radius.

## Tables

Header row in `caption` style, `--ink-55`. 1px `--rule` under the header, `--rule-faint` between rows. No zebra striping, no outer border, no cell padding beyond 10px vertical.

## Forms

Fields are a single bottom rule, not a box: 1px `--rule`, no top, left or right border, no fill, no radius. Label above in `caption`. On focus the bottom rule becomes 1px `--pen`, plus the standard focus ring.

## Focus

`outline: 2px solid var(--pen); outline-offset: 3px;` on every interactive element. Never removed, never replaced with a subtle alternative. This is also the fourth and last sanctioned use of the accent.

---

# 6. Motion

Almost none. Motion in this system reads as decoration unless it is doing work.

Sanctioned: link underline weight, 160ms ease-out. Focus ring, instant. Page-load fade-in on the display line only, 240ms ease-out, no translate.

Not sanctioned: scroll reveals, parallax, hover lifts, staggered entrances, counters, ambient background motion.

Respect `prefers-reduced-motion: reduce` by disabling the load fade entirely.

---

# 7. Mark

There is no icon. No rounded square, no monogram, no glyph. Adding one reintroduces exactly the problem this direction solves.

## Wordmark

`Mentat`, Archivo 600, 14px, uppercase, tracking +0.02em, `--ink`. Clear space on all sides equals the cap height. Never set in another weight, never coloured, never locked to a symbol, never placed on a photographic background.

## The tick

A 16 by 2px bar in `--pen`, sitting at the top of the rail with 12px below it.

This is the brand's only mark. It reads as a pen stroke in a margin, a reader's annotation, which is the whole thesis of the product. It appears once per page, always in the rail, always the same size. It does not scale with the display type, it does not repeat as a bullet, it does not become a divider, it is never rendered in any other colour.

Favicon: the same 16 by 2 bar, centred on `--stone`, at whatever size the format requires.

---

# 8. Voice

Plain, declarative, unhurried. The type is doing the persuading; the copy should not try.

- Sentence case everywhere except `caption` and the wordmark.
- Short declaratives. Full stops. The hero is two sentences and should stay that way.
- No exclamation marks. No "unlock", "supercharge", "seamlessly", "powerful", "revolutionise".
- Name things by what the reader controls, not by how the system is built.
- An action keeps the same verb through its whole flow. "Explore the system" leads to a page that says "The system".
- British spelling: artefacts, organise, recognise. Already established in the hero; keep it consistent.
- Errors state what happened and what to do, in the interface's voice: "That file has no frontmatter. Add a `type` key to index it." No apology, no vagueness.
- Empty states are invitations, not decoration: "No assets yet. Write one."

---

# 9. Misuse

Do not:

- Add a second accent colour, or a tint of `--pen`.
- Use `--pen` as a background, container border or heading colour.
- Set display type below 40px at weight 200.
- Centre the display type. Everything is left-aligned to the content column.
- Introduce a card, shadow, gradient, or any radius above 0.
- Put navigation, buttons or images in the rail.
- Warm the ground back toward cream. The accent stops working immediately.
- Add a logo icon.
- Fill the empty right side of the hero. It is the design.

---

# 10. Implementation

## CSS custom properties

```css
:root {
  /* colour */
  --stone:        #E6E8E6;
  --stone-raised: #EFF0EE;
  --ink:          #1F2124;
  --ink-70:       #3E4145;
  --ink-55:       #55585C;
  --ink-40:       #6C6F73;
  --ink-20:       #B7B9B7;
  --rule:         rgba(31,33,36,0.16);
  --rule-faint:   rgba(31,33,36,0.08);
  --pen:          #26418F;
  --pen-hover:    #1B3070;
  --error:        #8C2F2A;
  --success:      #2E5D45;
  --warn:         #7A5A1E;

  /* type */
  --font-sans: Archivo, "Helvetica Neue", Inter, system-ui, sans-serif;
  --font-mono: "Commit Mono", ui-monospace, "JetBrains Mono", monospace;

  /* space */
  --s-1: 4px;   --s-2: 8px;   --s-3: 12px;  --s-4: 16px;
  --s-5: 24px;  --s-6: 38px;  --s-7: 64px;  --s-8: 96px;  --s-9: 152px;

  /* layout */
  --rail:      150px;
  --gutter:    38px;
  --content:   720px;
  --page-max:  1180px;
  --page-pad:  52px;

  --radius: 0;
  --ease:   cubic-bezier(0.22, 0.61, 0.36, 1);
}

@media (prefers-color-scheme: dark) {
  :root {
    --stone:        #1C1E1C;
    --stone-raised: #252725;
    --ink:          #E6E8E6;
    --ink-70:       #C2C5C3;
    --ink-55:       #9DA0A2;
    --ink-40:       #7E8183;
    --rule:         rgba(230,232,230,0.16);
    --rule-faint:   rgba(230,232,230,0.08);
    --pen:          #7B9AE8;
    --pen-hover:    #9DB4EE;
  }
}
```

## Type utilities

```css
.display-xl { font-size:76px; line-height:.98; font-weight:200; letter-spacing:-.038em; }
.display-l  { font-size:60px; line-height:1.02; font-weight:200; letter-spacing:-.035em; }
.display-m  { font-size:40px; line-height:1.08; font-weight:200; letter-spacing:-.030em; }
.h1         { font-size:32px; line-height:1.15; font-weight:300; letter-spacing:-.025em; }
.h2         { font-size:24px; line-height:1.25; font-weight:400; letter-spacing:-.020em; }
.h3         { font-size:18px; line-height:1.35; font-weight:500; letter-spacing:-.010em; }
.body-l     { font-size:17px; line-height:1.70; font-weight:300; }
.body       { font-size:15px; line-height:1.70; font-weight:300; }
.small      { font-size:13px; line-height:1.60; font-weight:400; }
.caption    { font-size:11px; line-height:1.70; font-weight:500;
              letter-spacing:.04em; text-transform:uppercase; }

.display-xl strong, .display-l strong, .display-m strong { font-weight:500; }

@media (max-width:900px){ .display-xl,.display-l{ font-size:48px; letter-spacing:-.03em; } }
@media (max-width:640px){ .display-xl,.display-l{ font-size:40px; } .display-m{ font-size:32px; } }
```

## Tailwind v4

```css
@theme {
  --color-stone:  #E6E8E6;
  --color-raised: #EFF0EE;
  --color-ink:    #1F2124;
  --color-ink-70: #3E4145;
  --color-ink-55: #55585C;
  --color-ink-40: #6C6F73;
  --color-pen:    #26418F;
  --font-sans:    Archivo, "Helvetica Neue", system-ui, sans-serif;
  --font-mono:    "Commit Mono", ui-monospace, monospace;
  --radius-none:  0;
}
```

---

# 11. Open decisions

Flagged rather than settled. These are the places where this guide is a draft:

1. Mono face. Commit Mono is specified for neutrality against Archivo. IBM Plex Mono is warmer and more characterful if the Markdown substrate should feel more present. Worth a side-by-side on a real code block before committing. The published site currently loads JetBrains Mono, the named fallback, since Commit Mono is not on Google Fonts.
2. Dark mode. Resolved for the published site: it defaults to the operating system preference, with a text toggle in the footer to switch and remember the choice. The palette is still lightly tested; revisit if it proves distracting.
3. Long-form article template. The rail works for a hero. Whether it holds for a 2,000-word article, as a running metadata column, a footnote gutter, or nothing, is unresolved and is the next thing to design.
4. `display-xl` at 76px. Currently unused; the hero is set at `display-l`. Either commit to it on the homepage or delete the step, since an unused scale step is a guide that lies.

5. Measure on the home page. The published v2.0 home page loosens the tight measure in sections 3 and 9: the hero and body fill the content column rather than leaving the right side empty. This is a deliberate site-level override, not a change to the default measure for other artefacts. Whether to fold it back into the core spec is open.
