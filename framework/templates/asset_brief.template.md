---
title: Asset Brief Template
status: Template
summary: Concrete requirements for one visual asset family.
---

# Asset Brief

## Purpose

Complete this brief before producing an asset family. Use the shared constraints in the project
[Art Production Strategy](../../guidelines/art/core/production/art_production_strategy.md), then
record the exact values required for this family.

Every production-frame row below must contain a concrete value or `Not Applicable — <reason>`.
Keep realized file inventories, checksums, import results, and revision history in the asset
manifest or package record.

## Identity and Authorities

| Field | Entry |
|---|---|
| Brief ID | `<stable identifier>` |
| Asset family | `<name>` |
| Owner | `<person or discipline>` |
| Priority and status | `<P0–P3; Draft, Candidate, Approved, or Production-ready>` |
| Product requirement | `<document or requirement ID>` |
| Art direction | `<shared and subject-specific documents>` |
| Production profile | `<strategy section and applicable family baseline>` |
| Runtime target | `<client, scene, component, or technical specification>` |
| Related manifest | `<path or planned location>` |

## Scope

- **Gameplay or presentation role:** `<responsibility>`
- **Player-facing outcome:** `<what must be understood or felt>`
- **Required contexts:** `<screens, scenes, backgrounds, and neighboring content>`
- **Included:** `<assets, variants, states, and evidence>`
- **Excluded:** `<related work owned elsewhere>`

## Deliverables

| Asset or group | Purpose | Required states or variants | Source and runtime outputs |
|---|---|---|---|
| `<asset>` | `<role>` | `<states or variants>` | `<master plus exact export set>` |

## Production Frame

| Constraint | Shared baseline | Concrete requirement for this family |
|---|---|---|
| Target viewports | `<applicable strategy viewports>` | `<exact viewports and contexts>` |
| Native display sizes | `<applicable size tier or family>` | `<exact pixel sizes>` |
| Master or source size | `<applicable family baseline>` | `<exact dimensions>` |
| Runtime exports | `<applicable export ladder>` | `<exact dimensions and variants>` |
| Aspect and responsive behavior | `<crop, reframe, fixed aspect, or scalable rule>` | `<exact behavior>` |
| Canvas and content bounds | `<shared-canvas rule>` | `<canvas and visible bounds>` |
| Safe area and padding | `<strategy rule>` | `<exact insets or bounds>` |
| `4 px` grid | `Required for author-controlled layout geometry` | `<component dimensions, spacing, padding, insets, offsets, and any permitted exceptions>` |
| Pivot, anchor, and orientation | `<family default>` | `<exact coordinates and facing>` |
| Source and runtime formats | `<project or family baseline>` | `<formats and bit depth>` |
| Alpha and masks | `<project or family baseline>` | `<transparent, opaque, premultiplication, and masks>` |
| Color space | `<project or runtime baseline>` | `<exact color space>` |
| Scaling and slicing | `<uniform, nine-slice, fixed-piece, tile, or none>` | `<insets and protected geometry>` |
| Filtering, mipmaps, and compression | `<runtime baseline>` | `<exact import requirements>` |
| Layers and assembly | `<strategy layer rule>` | `<independent groups and order>` |
| Performance limits | `<target profile>` | `<texture, geometry, material, particle, or overdraw limits>` |

Any deviation from the shared baseline requires a recorded reason and approval:

- **Deviation:** `<none or exact difference>`
- **Reason:** `<why the baseline cannot satisfy the asset>`
- **Approver:** `<name or role>`

## References and Visual Requirements

| Topic | Requirement |
|---|---|
| Reference assets | `<paths or stable IDs and the properties each reference controls>` |
| Visual goal | `<intended result and reading order>` |
| Shape and silhouette | `<forms that must remain readable at the smallest native size>` |
| Color, material, and lighting | `<palette roles and surface treatment>` |
| Camera and composition | `<view, facing, framing, and focal-safe regions>` |
| Identity locks | `<symbols, geometry, proportions, or details that may not change>` |
| Avoid | `<conflicting styles, meanings, or baked-in dynamic content>` |

## States and Motion

| State or event | Meaning | Required non-color cue | Motion or VFX | Interruption result | Reduced-motion equivalent |
|---|---|---|---|---|---|
| `<state or trigger>` | `<player-facing meaning>` | `<shape, value, symbol, or structure>` | `<behavior or none>` | `<correct final state>` | `<equivalent or not applicable>` |

## Source and Rights

| Field | Record |
|---|---|
| Source and creator | `<authored, generated, purchased, or derived; creator or tool>` |
| Source record | `<URL, repository path, order, or generation record>` |
| Date | `<YYYY-MM-DD>` |
| License and restrictions | `<commercial use, modification, attribution, and redistribution terms>` |

## Acceptance

Use `Pass`, `Fail`, `Not Assessed`, or `Not Applicable`.

| Gate | Result | Evidence |
|---|---|---|
| Scope and exact deliverables are complete | `Not Assessed` | `<link>` |
| Strategy baselines are applied or approved deviations are recorded | `Not Assessed` | `<brief section>` |
| Visual identity reads at every required native size and background | `Not Assessed` | `<contact sheet or comparison>` |
| Required states remain clear without color, motion, or sound alone | `Not Assessed` | `<state review>` |
| Canvas, `4 px` grid, bounds, padding, alpha, pivot, layers, and exports match this brief | `Not Assessed` | `<technical report>` |
| Motion, interruption, and reduced-motion behavior work as specified | `Not Assessed` | `<capture or not-applicable reason>` |
| Required viewport, runtime, and performance checks pass | `Not Assessed` | `<in-engine evidence>` |
| Source and usage rights are recorded and compatible with the project | `Not Assessed` | `<record>` |

## Approval

| Field | Record |
|---|---|
| Decision | `<Approved, Revision required, or Rejected>` |
| Reviewed asset or revision | `<path, version, or manifest>` |
| Reviewer and date | `<name or role, YYYY-MM-DD>` |
| Conditions | `<remaining conditions or none>` |
