# Decision: enable functional icons in the brand kit

Date: 2026-07-24
Status: adopted
Affects: brand/03-Design-System.md (v2.0 to v2.1), brand/01-Brand-Book.md, brand/assets/tokens.css

## Decision

Permit functional interface icons in the Mentat visual system, under a monoline, ink-only constraint. The brand mark is unchanged: there is still no logo icon, and the tick remains the only mark that carries the pen colour.

## Context

Marginalia (Direction 05, Ascetic) forbade icons outright (design system sections 7 and 9). Producing the process readiness illustration required one icon per dimension to aid scanning, which was done as a documented brand override. The owner chose to make icons a sanctioned part of the system rather than a repeated exception.

## Alternatives

1. Keep the total ban and treat every icon as a per-artefact override. Rejected: repeated overrides erode the rule and leave icon usage ungoverned.
2. Permit icons freely. Rejected: unconstrained icons reintroduce the ornament the direction removes, and colour would compete with the single accent.
3. Permit a constrained functional set. Adopted.

## Rationale

A tightly governed set keeps the ascetic discipline while allowing icons to do real work in lists and cards. The binding constraints, single stroke weight, no fill, ink only, never the accent, size ceiling 24px, one per row, schematic not illustrative, preserve the core principle that the pen colour marks the one live thing on the page.

## Consequences

- Icons are now defined in design system section 5 (Icons), with tokens `--icon-stroke` and `--icon-size` added to section 10 and `brand/assets/tokens.css`.
- Section 7 (Mark) reworded to govern the mark only. Section 9 (Misuse) now bans coloured, filled or multi-weight icons instead of banning icons outright.
- The process readiness illustration is now compliant with the system rather than an override.
- Any generated artefact using icons must follow the section 5 constraints.
