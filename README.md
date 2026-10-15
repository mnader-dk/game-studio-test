---
title: Rune Mastery Visual Design
status: Living
summary: Authoritative visual language, asset catalog, production rules, and approval state for Rune Mastery.
---

# Rune Mastery Visual Design

This directory is the authoritative living visual-design document for Rune Mastery. It connects
the approved rendering language, reusable visual foundations, canonical assets, production rules,
animation architecture, quality gates, and approval state.

Screen composition now follows the approved first-session journey scene by scene. The current
working scene is [01 · Splash Screen](Screens.md#01-splash-screen).

![Approved Rune Mastery rendering reference](../output/style-reference/rune_mastery_approved_rendering_reference.png)

## Purpose

- Keep the approved visual language easy to find and hard to reinterpret accidentally.
- Show the current approved asset rather than only describing it.
- Separate canonical identity, reusable carriers, optional effects, and runtime state layers.
- Record status, provenance, technical constraints, and acceptance evidence beside each family.
- Make animation readiness a design input rather than a late implementation repair.

## Visual system at a glance

This map describes the intended documentation flow. It does not approve new visual rules or
implementation choices.

```text
Game vision and player experience
  -> visual foundations
  -> reusable visual language
  -> product visual systems
  -> responsive screen compositions
  -> components and asset families
  -> production and runtime packages
  -> native-scale and in-engine validation
```

The [Product Visual Systems](Product_Systems.md) area provides the system-level bridge
between the shared visual language and individual screens or assets. Card Anatomy, Faction
Identity, Progression Presentation, and Live-Service Theming are approved semantic contracts;
concrete implementing assets retain their own approval and validation status.

## Current system status

| Area | Status | Current authority |
| --- | --- | --- |
| Rendering language | Approved | `output/style-reference/` |
| Game logo family | Approved identity; icon derivative candidate | `output/brand/logo/v008/` |
| Simplified Mage Tower Splash | Static composition approved at 16:9, 4:3, and 16:10; startup indicator pending | `output/splash-screen/v006/` |
| Fire, Air, Forest glyph identities | Approved | `output/rune-kit/v001/approved/glyphs/` |
| Element-colored carrier language | Approved | `output/rune-kit/v001/state-carriers/concepts/v002/` |
| Runtime carrier layers | Approved | `output/rune-kit/v001/state-carriers/layers/v001/` |
| In-engine unlock and glow motion | Not validated | Pending runtime test |
| Standard button frame v002 | Approved | `output/ui-kit/v001/frames/standard/concepts/v002/` |
| Compact horizontal button frame v002 | Approved | `output/ui-kit/v001/frames/compact/concepts/v002/` |
| Square icon-button frame v002 | Approved | `output/ui-kit/v001/frames/icon-square/concepts/v002/` |
| Shared Quiet, Focus Emphasis, and Raised panel family v001 | Approved | `output/ui-kit/v001/surfaces/panel-family/concepts/v001/` |
| Quiet and Ceremonial divider family v002 | Approved | `output/ui-kit/v001/surfaces/divider-family/concepts/v002/` |
| Shared input surface family v001 | Approved | `output/ui-kit/v001/surfaces/input-surface-family/concepts/v001/` |
| Navigation open-rail frame v003 | Approved | `output/ui-kit/v001/frames/navigation-row/concepts/v003/` |
| Navigation open-rail state layers v002 | Approved | `output/ui-kit/v001/frames/navigation-row/states/v002/` |
| Shared neutral button surface v002 | Approved | `output/ui-kit/v001/surfaces/button-neutral/concepts/v002/` |
| Shared button interaction states v002 | Approved | `output/ui-kit/v001/states/button-interaction/concepts/v002/` |
| Core action icon family v003 | Approved | `output/ui-kit/v001/icons/action-core/concepts/v003/` |

## How to navigate

| Area | Purpose |
| --- | --- |
| `Foundations.md` | Rendering reference, tokens, accessibility, and documentation principles |
| `Visual_System.md` | Shape, material, lighting, detail, state, and motion language |
| `Product_Systems.md` | Card, faction, progression, and live-service visual-system specifications |
| `Screens.md` | First-session flow, screen compositions, HUDs, overlays, and per-scene element inventories |
| `Asset_Catalog.md` | Stable asset identities, approved sources, variants, and runtime packages |
| `Production.md` | Lifecycle, naming, manifests, layer contracts, and animation-ready construction |
| `Quality.md` | Acceptance gates, native-scale checks, motion validation, and style-drift control |
| `Templates.md` | Repeatable briefs for new asset families |

## Authority boundaries

- This workspace owns visual intent, art direction, asset identity, reusable source assets, and
  visual acceptance evidence.
- Game rules and player-facing product behavior belong in `GameDesign/`.
- Engine scene structure, runtime code, shaders, and import implementation belong with the game
  client, while their visual contracts are linked from here.
- Generated candidates are evidence, not authority. Only explicitly approved stable paths are
  canonical.

## Working rules

- Inspect the approved reference and existing assets before inventing a new direction.
- Use stable catalog IDs and never silently replace an approved identity.
- Keep optional effects and independently animated parts on separate aligned layers.
- Publish a family in `VisualDesign/` only after explicit user approval; keep review-stage material in `output/` until then.
- Validate at native game scale and in motion before production signoff.
- Link to source files and manifests instead of copying hidden derivatives into documentation.

## Maintaining the reader

Edit the Markdown documents and, when visual evidence changes, `asset_evidence.json`, then
regenerate the self-contained reader:

```bash
python3 scripts/generate_visual_design_html.py
```

Do not edit `VisualDesign.html` by hand. The generated file is the local browsing surface; the
Markdown files, catalog, asset manifests, and approved images remain the source of truth.
