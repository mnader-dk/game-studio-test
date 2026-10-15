---
title: Rune Mastery Visual Design
status: Living
summary: Authoritative visual language, asset catalog, production rules, and approval state for Rune Mastery.
---

# Rune Mastery Visual Design

This directory is the authoritative living visual-design document for Rune Mastery. It connects
the approved rendering language, reusable visual foundations, canonical assets, production rules,
animation architecture, quality gates, and approval state.

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
## How to navigate

| Area | Purpose |
| --- | --- |
| `framework/` | The `framework/` directory contains reusable rules, templates and guides used to create various markdown files  |
| `guidelines/` | The `guidelines/` directory contains all relevant guardrails and references for creating Art, Assets, UI/UX, etc. for Rune Mastery.|
| `output/` | The `output/` directory contains all production results based on the guardrails defined in `guidelines/` and acts as the only working directory for creating output. |


## Authority boundaries

- This workspace owns visual intent, art direction, asset identity, reusable source assets, and
  visual acceptance evidence.

## Working rules

- Inspect the approved reference and existing assets before inventing a new direction.
- Use stable catalog IDs and never silently replace an approved identity.
- Keep optional effects and independently animated parts on separate aligned layers.
- Validate at native game scale and in motion before production signoff.