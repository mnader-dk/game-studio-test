---
title: Gameplay Object Brief Template
status: Template
summary: Creation requirements for every gameplay object in one asset-kit family.
---

# Gameplay Object Brief

## Purpose

Copy this template once for each family in the Gameplay Object Asset Pipeline. Replace every
placeholder with a concrete value and add one gameplay-object subsection for every stable asset ID
owned by the family.

Do not remove fields that do not apply. Use `Not Applicable — <reason>` instead. Keep realized file
inventories, checksums, provenance, validation results, and approval history in the related asset
manifest or package record.

## Kit and Family Specifications

### `<KIT-ID>`

#### `<Family Name>`

##### Family Contract

| Field | Requirement |
|---|---|
| Purpose | `<shared production responsibility of this family>` |
| Current maturity | `<Draft, Candidate, Approved, or Production-ready; supporting revision or evidence>` |
| Kit dependencies | `<stable IDs of required kits, families, or gameplay objects>` |
| Product behavior | `<authoritative design documents and requirement IDs>` |
| Visual authority | `<shared and subject-specific art documents and approved references>` |
| State profile | `<required state profile or Not Applicable — reason>` |
| Target contexts | `<screens, scenes, viewports, backgrounds, camera, and neighboring content>` |
| Visual language | `<shared shape, silhouette, value, palette, material, lighting, edge, and detail rules>` |
| Runtime content | `<dynamic text, values, icons, identity, or other content that remains separate>` |
| Shared construction | `<canvas, coordinate system, scale, pivot, safe area, padding, and alignment rules>` |
| Shared technical frame | `<2D or 3D, master sizes, runtime size ladder, format, color space, alpha, filtering, compression, and target platforms>` |
| Required deliverables | `<source masters, runtime exports, layers, masks, guides, previews, reports, and manifest>` |
| Accessibility and gameplay read | `<non-color cues, native-size readability, reduced-motion, contrast, and alternative labeling>` |
| Input fit | `<hit area, spacing, focus, selection, hover, touch, or Not Applicable — reason>` |
| Performance limits | `<texture, geometry, material, animation, particle, memory, or overdraw budgets>` |
| Exclusions | `<content, meanings, styles, variants, and implementation concerns owned elsewhere>` |

Define the shared back-to-front layer or assembly order. Replace the example node names and add or
remove levels only when the family requires it.

```text
<family canvas or root>
└── <background, shadow, or base>
    └── <immutable structure>
        └── <identity or content surface>
            └── <runtime content>
                └── <state, feedback, or optional effects>
```

Record invariants that every gameplay object and state must preserve:

- `<external dimensions, bounds, scale, or silhouette invariant>`
- `<pivot, anchor, baseline, orientation, or coordinate invariant>`
- `<identity, material, lighting, or detail-density invariant>`
- `<runtime-content, state-layer, and accessibility invariant>`

##### `<GAMEPLAY-OBJECT-ID>`

Duplicate this subsection for every stable gameplay-object ID in the family.

| Field | Creation requirement |
|---|---|
| Role | `<gameplay, UI, presentation, or production responsibility>` |
| Player-facing outcome | `<what the player must recognize, understand, or feel>` |
| Priority and status | `<P0–P3; Draft, Candidate, Approved, or Production-ready>` |
| Product requirement | `<authoritative document or requirement ID>` |
| Dependencies | `<stable asset IDs required for composition; none if self-contained>` |
| Source master | `<exact dimensions, scale, topology, duration, or other source specification>` |
| Runtime outputs | `<exact size, format, variant, state, frame, LOD, or package set>` |
| Target contexts | `<native display sizes, backgrounds, camera, screen, or scene>` |
| View and orientation | `<orthographic, perspective, facing, angle, projection, or Not Applicable — reason>` |
| Geometry and silhouette | `<outer form, proportions, protected shapes, and smallest-size reading>` |
| Color, material, and lighting | `<semantic palette roles, surface treatment, light direction, and contrast>` |
| Required layers or parts | `<independent named groups and back-to-front or assembly order>` |
| Pivot, anchor, and bounds | `<exact pivot, anchor, baseline, visible bounds, safe area, and padding>` |
| States and variants | `<complete required set and composition rules>` |
| Content rules | `<dynamic content, localization, iconography, values, identity, and safe-area behavior>` |
| Alpha, masks, and transparency | `<opaque or transparent policy, masks, premultiplication, and edge requirements>` |
| Scaling and slicing | `<uniform, fixed-size, nine-slice, tileable, crop, reframe, or none>` |
| Color space and import | `<color space, filtering, mipmaps, compression, atlas, material, and shader expectations>` |
| Motion readiness | `<animation groups, frame or rig requirements, interruption result, loops, and reduced-motion equivalent>` |
| Accessibility and gameplay read | `<required non-color cues, contrast, text equivalent, and native-scale checks>` |
| Performance limits | `<asset-specific texture, mesh, material, animation, particle, memory, or overdraw limits>` |
| Required evidence | `<contact sheet, turntable, state matrix, native-scale capture, technical report, or runtime proof>` |
| Do not | `<forbidden geometry, style drift, meanings, baked content, artifacts, or implementation shortcuts>` |

Use this table when the gameplay object has visual states, variants, or events. Otherwise replace
the row with `Not Applicable — <reason>`.

| State, variant, or event | Player-facing meaning | Required presentation | Non-color cue | Motion or VFX | Interruption result | Reduced-motion equivalent |
|---|---|---|---|---|---|---|
| `<name>` | `<meaning>` | `<visual construction>` | `<shape, value, symbol, label, or structure>` | `<behavior or none>` | `<deterministic final state>` | `<equivalent or Not Applicable — reason>` |

Acceptance requires:

- `<identity and silhouette criterion at every required native size>`
- `<technical dimensions, bounds, pivot, layer, alpha, and export criterion>`
- `<state, variant, accessibility, and reduced-motion criterion>`
- `<context, runtime, and performance criterion>`
- `<provenance, manifest, and approval evidence criterion>`

##### `<Family Name>` Family Acceptance Gates

Use `Pass`, `Fail`, `Not Assessed`, or `Not Applicable — <reason>`.

| Gate | Result | Evidence |
|---|---|---|
| Every stable gameplay-object ID in the family has one complete creation subsection | `Not Assessed` | `<brief sections>` |
| Every gameplay object has one manifest entry and complete requirement-to-evidence traceability | `Not Assessed` | `<manifest or traceability record>` |
| Shared construction, visual language, scale, lighting, edge treatment, and detail density remain cohesive | `Not Assessed` | `<family comparison>` |
| Required identities, silhouettes, content, and states read at every native size and context | `Not Assessed` | `<native-scale evidence>` |
| State and gameplay meaning remain clear without color, glow, motion, sound, or hover alone | `Not Assessed` | `<accessibility and state review>` |
| Canvases, bounds, padding, pivots, layers, masks, alpha, formats, and exports match this brief | `Not Assessed` | `<technical report>` |
| Motion, interruption, loops, and reduced-motion equivalents behave as specified | `Not Assessed` | `<capture or Not Applicable — reason>` |
| Runtime composition, target-platform behavior, and performance limits pass | `Not Assessed` | `<runtime evidence>` |
| Source, creator or tool, license, restrictions, edit history, and approval are recorded | `Not Assessed` | `<provenance and approval record>` |
