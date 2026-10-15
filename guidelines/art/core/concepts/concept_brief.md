---
title: Rune Mastery Core Concept Brief
status: Draft
summary: Cross-game concept targets, reference scope, review criteria, and provenance for Rune Mastery.
---

# Concept Brief

## Purpose

This brief defines what Rune Mastery's cross-game concept references should communicate and how
they are evaluated. It records the purpose, limits, technical facts, review status, and provenance
of the current overview image.

The brief supports visual discussion and later subject-specific work. It does not define gameplay,
lore, product behavior, runtime implementation, or final production assets.

## Scope Boundaries

This brief may establish:

- overall fantasy tone and visual cohesion;
- broad relationships between characters, environments, crafted objects, cards, and magic;
- observable rendering, palette, material, lighting, focus, and detail tendencies;
- subjects that require their own focused concept work; and
- the review role and status of the overview image.

This brief does not establish:

- canonical rune glyph geometry;
- faction symbols, palettes, costumes, or cultural identity;
- card anatomy, UI component anatomy, interaction states, or design tokens;
- exact character proportions, construction sheets, animation layers, or pivots;
- scene-specific composition, responsive behavior, or gameplay hierarchy; or
- production readiness, engine settings, runtime performance, or shipping approval.

## Concept Targets

| Target | Purpose | Current coverage | Follow-up |
|---|---|---|---|
| Cross-game overview | Communicate the overall fantasy tone, elemental emphasis, material family, and card-game context | Represented by the primary concept reference | Maintain as the common comparison image |
| Rune Master character | Establish player-facing silhouette, proportions, equipment language, and motion intent | Suggested by one character; not authoritative | Requires a character-specific concept brief |
| Rune and magic presentation | Explore how Fire, Air, and Forest read as distinct dimensional magic without obscuring stable glyphs | Represented at a high level; no state or production contract | Requires an owning rune-system concept brief |
| Card and interface context | Test whether cards, controls, and changing content remain readable within the world language | Broad blank surfaces are shown; no component anatomy or state system is approved | Requires owning component briefs |
| Environment key | Establish architectural scale, depth, palette balance, and calm space around gameplay content | Broadly represented; not validated in a gameplay viewport | Requires a scene-specific brief when needed |

## Primary Concept Reference

![Rune Mastery concept overview](images/concept_reference/concept_overview_v001.png)

| Image | Reference ID | Purpose | Status |
|---|---|---|---|
| [`concept_overview_v001.png`](images/concept_reference/concept_overview_v001.png) | `STYLE-REFERENCE-RUNE-MASTERY` | Evaluate rendering character, palette balance, material family, elemental emphasis, card-game context, and overall fantasy tone together | Concept reference |

The image is a shared comparison target. Its status does not approve every depicted character,
environment, rune glyph, card frame, composition, or production detail.

## Context

- **Presentation role:** Cross-game visual comparison target.
- **Screen ownership:** Not tied to one screen or feature.
- **View:** Landscape fantasy scene with perspective depth and a clear focal plane.
- **Native display size:** Not defined for gameplay review.
- **Background:** Limestone terrace, open sky, distant architecture, water, mountains, and controlled
  foliage.
- **Gameplay evidence:** The image is a standalone scene, not a gameplay capture.
- **Animation role:** None; this is a static reference.

## Concept Reading

| Area | What the reference communicates | What remains outside its authority |
|---|---|---|
| Shape and silhouette | Large readable masses, rounded modeled forms, stable silhouettes, and controlled organic asymmetry | Exact subject proportions and construction |
| Value and focus | Crisp focal forms against simplified, softer peripheral and distant content | Tested gameplay hierarchy at native size |
| Palette | Warm cream limestone, controlled blue, warm brown, restrained metal accents, natural green, and localized elemental color | Exact swatches and runtime color tokens |
| Materials | Smooth stylized stone, cloth, leather, wood, foliage, and dimensional elemental surfaces | Texture, shader, and material implementation |
| Lighting | Soft warm key from the upper left, cool ambient fill, contact shadows, and subordinate local elemental light | Scene-specific exposure and runtime lighting |
| Edge and detail | Clean anti-aliased silhouettes, soft modeled bevels, low surface noise, and detail concentrated near the focal area | Downscaled and in-engine behavior |
| Rune presentation | Fire, Air, and Forest remain visibly distinct through stable shapes and localized effects | Canonical glyph masters, carrier states, and runtime layers |
| Cards and UI | Calm framed surfaces reserve space for changing content | Component anatomy, text fit, states, tokens, and responsive behavior |