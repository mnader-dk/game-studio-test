---
title: Rune Mastery Art Production Strategy
status: Draft
summary: Shared lifecycle, approval, normalization, traceability, handoff, and validation rules for Rune Mastery art assets.
---

# Art Production Strategy

## Purpose and Authority

This document is the source of truth for how Rune Mastery turns visual intent into cohesive,
traceable, runtime-ready art packages. It defines the shared production lifecycle, status model,
versioning rules, evidence requirements, handoff contract, and production-readiness gates.

It does not define gameplay behavior, final visual identity, balance, engine architecture, or the
contents of a particular asset family. Product rules come from the
[Game Design Document](../../../design/game_design_document.md) and its owning specifications.
Shared visual intent comes from the [Core Art Direction](../direction/art_direction.md) and the
relevant subject-specific art document. A concrete family begins with a completed family brief
based on the [Asset Brief Template](../../../../framework/templates/asset_brief.template.md).

The [Art Guidelines](../../README.md) own directory responsibilities, reference stages, and the
distinction between visual approval and production readiness.

## Core Production Rule

A concept, generated image, purchased source, model, texture, or design-file preview is source
material. It is not proof that an asset is ready for the game.

Dimensions, color space, alpha, content bounds, pivots, layer separation, state coverage, naming,
compression, import settings, performance, native-scale readability, motion, and runtime behavior
must be established and verified deliberately.

## Production Principles

1. Start from an owning product requirement and an approved or reviewable visual authority.
2. Define the technical frame and motion needs before producing the asset family.
3. Approve one representative visual target before producing many related assets.
4. Produce related assets as a family with shared invariants rather than as unrelated one-offs.
5. Normalize dimensions, alpha, pivots, layers, names, and exports deterministically.
6. Keep dynamic text, values, labels, and player data code-native.
7. Preserve identity, state meaning, and accessibility through every derivative and runtime form.
8. Validate at native size, on representative backgrounds, and in the game client.
9. Record source, rights, edits, approval, and validation evidence beside the package.
10. Change an owning source or rule instead of hiding a defect in a downstream override.

## Authority Boundaries

| Concern | Owning authority |
|---|---|
| Player outcome, behavior, rules, and feature scope | Owning Game Design specification |
| Shared rendering, material, lighting, color, detail, and motion language | Core and subject-specific art guidance |
| Shared viewports, size profiles, canvas rules, export constraints, and quality baselines | Art Production Strategy |
| Purpose, deliverables, applicable profile, concrete technical values, variants, and acceptance criteria | Asset-family brief |
| Stable identity, version, files, states, layers, provenance, and validation results | Asset-family manifest and package record |
| Engine imports, resources, scenes, shaders, runtime code, and platform implementation | Game client and its technical documentation |
| Visual approval | Recorded review decision against the owning visual authority |
| Production readiness | Evidence that every applicable quality and runtime gate passes |

No downstream export, import setting, shader, scene override, or screen composition may silently
redefine an upstream gameplay rule, approved identity, state meaning, or visual source.

## Shared Asset Production Frame

These constraints are the project baseline for asset briefs, source masters, runtime exports, and
validation. Every asset brief selects the applicable family profile and records exact values.
A different value requires a documented reason and explicit approval; absence of a value is not an
exception.

### Reference Viewports and Responsive Behavior

| Viewport | Role | Required behavior |
|---|---|---|
| `1920 × 1080` | Desktop and browser composition master | Establish the primary full-screen composition and anchor relationships |
| `1280 × 960` | `4:3` landscape-tablet validation | Reframe or crop while keeping focal content, controls, and feedback inside safe regions |
| `1280 × 800` | `16:10` compact desktop and landscape validation | Reduce decorative vertical content before shrinking required information |

Full-screen and composition-dependent assets are checked at all three viewports without browser
zoom. Responsive layouts recompose, re-anchor, or use intentional cover crops; they do not stretch
a flattened desktop image. Background, brand, feedback, and optional atmosphere remain separable
when their crop, visibility, timing, or scale differs. Each brief records focal-safe regions,
responsive anchors, and crop tolerance.

### Native-Scale and Interaction Baselines

| Use | Required sizes or limit |
|---|---|
| Standard Rune and HUD presentation | `64 × 64` |
| Large Rune and HUD presentation | `128 × 128` |
| Compact card-cost glyph | `32 × 32` |
| Minimum interactive target | `44 × 44` |

The smallest size is a design constraint, not only a downscaled export. Preserve the essential
silhouette and primary symbol before secondary detail. Validate each size in its real screen
context and against representative light, dark, neutral, and illustrated backgrounds. Visible art
may be smaller than its interaction bounds, but the interactive target may not fall below the
minimum.

### Reference and Brand Raster Profiles

| Family or use | Master or source | Required exports and rules |
|---|---|---|
| Canonical rendering comparison | `1672 × 941`, opaque | Review reference only; it does not define a runtime asset size |
| Full logo, web | `1254 × 1254` native transparent raster | `1024`, `512`, `256`, `128`, and `64` px square PNG; verify wordmark readability at final scale |
| Full logo, merchandise | `1254 × 1254` native transparent raster | `1254`, `2048`, and `4096` px square PNG; the larger two are raster upscales and require intended-print-size inspection |
| Text-free app icon master | `1254 × 1254` transparent PNG | Shared deterministic source for all icon derivatives |
| App Store | Text-free icon master | `1024 × 1024`; the final delivery file requires an approved opaque background |
| Google Play | Text-free icon master | `512 × 512` presentation and listing export |
| Apple device icons | Text-free icon master | `180`, `167`, `152`, `120`, `87`, `80`, `76`, `60`, `58`, `40`, `29`, and `20` px square |
| Android launcher icons | Text-free icon master | `192`, `144`, `96`, `72`, and `48` px square |
| Web and PWA icons | Text-free icon master | `512`, `192`, `64`, `48`, `32`, and `16` px square |

Use the largest practical approved source and create derivatives deterministically. Do not edit
individual export sizes independently. If an identity fails at a small size, define and approve a
simplified derivative rather than changing only that export. Pixel dimensions do not imply a
physical print resolution; merchandise output also requires the vendor-specific print check.

### Screen and Rune Profiles

| Family | Master or canvas | Runtime sizes and constraints |
|---|---|---|
| Splash background and composition | `1920 × 1080` master composition | Validate dedicated `1920 × 1080`, `1280 × 960`, and `1280 × 800` layouts; preserve safe regions through reframing or crop |
| Canonical Rune glyphs | `1254 × 1254` transparent masters | Deterministic `512`, `128`, `64`, and `32` px square exports |
| Rune carriers and state layers | `512 × 512` shared canvas | Center pivot `(256, 256)`; nominal carrier content `448 × 448`; all elements and states retain the same coordinates |

Canonical glyphs are resized uniformly and are never redrawn, reconnected, cropped, rotated,
mirrored, or structurally simplified. Carrier, state, lock, shadow, glow, and identity layers remain
separate where runtime visibility or motion differs.

### Shared UI Size Profiles

| Family | Master | Large | Medium | Small |
|---|---|---|---|---|
| Standard button and navigation rail | Family source | `384 × 128` | `320 × 112` | `256 × 96` |
| Compact button | Family source | `256 × 128` | `224 × 112` | `192 × 96` |
| Square icon button | Family source | `128 × 128` | `112 × 112` | `96 × 96` |
| Control icon | `256 × 256` | `128 × 128` | `112 × 112` | `96 × 96` |
| Content panel | `1536 × 768` | `768 × 384` | `512 × 256` | `384 × 192` |
| Horizontal divider | Family source | `1280 × 192` | `960 × 144` | `640 × 96` |
| Vertical divider | Family source | `192 × 768` | `144 × 576` | `96 × 384` |
| Input surface | Family source | `768 × 168` | `640 × 140` | `512 × 112` |
| Input content safe area | Matches input tier | `588 × 74` | `490 × 62` | `392 × 50` |

The panel master uses `192 px` left and right and `160 px` top and bottom nine-slice insets.
Panel, input, button, and navigation families use their documented masks and protected geometry.
Corners, clasps, end pieces, center bridges, symbols, and ornament are not stretched. Dividers
preserve aspect ratio: only documented straight rail spans may extend. Square buttons and their
icons remain `1:1` and scale uniformly.

Exact card canvas, aspect ratio, native pixel sizes, and responsive breakpoints do not yet have a
shared baseline. The owning card brief must define and approve them before card-frame or
illustration production.

### Canvas, Grid, Layer, and Assembly Constraints

- Author-controlled layout geometry uses a `4 px` base grid. Component dimensions, spacing,
  padding, safe areas, insets, and offsets use multiples of `4 px`.
- Externally mandated delivery dimensions and established approved source canvases are exempt from
  the grid. Their internal content remains aligned to the `4 px` grid where practical.
- Every other grid deviation requires an exact reason and explicit approval in the asset brief.
- Related states, variants, and independently controlled layers use one canvas, coordinate system,
  pivot, scale, orientation, and naming convention.
- Centered pivots are the default for the established Rune and shared UI profiles. A different pivot
  is recorded in the asset brief and manifest.
- Record canvas, visible content bounds, focal-safe or content-safe area, crop tolerance, and
  transparent padding separately.
- Reserve enough transparent padding for shadow, bloom, particle falloff, travel, rotation, hover,
  tilt, and pulse scale at their maximum intended extent.
- Keep immutable structure, canonical identity, state treatment, contact shadow, glow, particles,
  focus treatment, and optional effects separate when runtime control differs.
- Keep localized text, values, counts, timers, player data, cursors, spinners, and accessibility
  labels code-native.
- State changes retain their external layout footprint unless the owning requirement explicitly
  defines a layout change.
- Runtime assembly must not use undocumented offsets, non-uniform scaling, recoloring, clipping, or
  masks to repair a defective source package.

### File, Alpha, Scaling, and Import Constraints

- Record source and runtime format, bit depth, color space, alpha behavior, masks, filtering,
  mipmaps, repeat, compression, atlas padding, material, shader, and import target in the brief and
  manifest where applicable.
- Use transparent output for separable raster layers; verify edge color, alpha coverage,
  premultiplication behavior, and background removal rather than inferring them from a preview.
- Derive runtime sizes from the approved master with a repeatable resize, crop, slice, or conversion
  step. Preserve aspect ratio unless an approved nine-slice or fixed-piece assembly defines the
  scalable regions.
- Verify exact dimensions, content bounds, safe areas, pivot, alignment, and source-pixel integrity
  after normalization.
- Generated grids, transparent backgrounds, seams, frame counts, topology, dimensions, and file
  formats are untrusted until inspected.
- A family may use PNG, vector, model, texture, or another runtime-appropriate format; there is no
  universal format override. The brief records the selected format and the runtime owner confirms
  its import behavior.

### Required Quality Evidence

Every applicable asset family provides:

1. a comparison with its approved visual authority at the same display size;
2. a native-size contact sheet or equivalent review for every required size and state;
3. context captures on representative backgrounds and beside neighboring content;
4. exact-dimension, bounds, alpha, color-space, pivot, layer, and naming checks;
5. responsive evidence at every required reference viewport for composition-dependent assets;
6. in-engine evidence for import, scaling, slicing, seams, masks, materials, and shaders;
7. motion evidence for clipping, pivot drift, interruption, rapid repetition, simultaneous effects,
   hidden or off-screen behavior, and reduced-motion equivalence;
8. accessibility evidence showing that required meaning survives without color, glow, motion,
   sound, or pointer hover alone;
9. performance evidence for the recorded texture, memory, material, geometry, particle, overdraw,
   and animation budget; and
10. provenance and rights evidence for every shipped source and derivative.

A full-size isolated preview does not replace native-scale, responsive, or in-engine evidence.


## Required Production Flow

```text
product requirement
  -> subject-specific visual rule
  -> asset brief
  -> representative visual target
  -> explicit visual approval
  -> asset family and aligned source layers
  -> deterministic normalization and manifest
  -> runtime package and engine mapping
  -> native-scale and in-engine validation
  -> production signoff
```

### 1. Requirement Intake

- Link the owning Game Design specification or stable requirement identifier.
- Define the player-facing or presentation outcome.
- Separate required functionality from decorative opportunity.
- Identify which information must remain readable without color, glow, motion, or sound.
- Confirm whether an existing asset family, component, or approved reference already owns the need.

Production does not begin from an attractive image alone. It begins from a defined responsibility.

### 2. Asset Brief

Use the [Asset Brief Template](../../../../framework/templates/asset_brief.template.md) to define
each concrete family when its production begins. Select the applicable production profile, fill
every shared constraint with an exact asset-specific value or a reasoned `Not Applicable`, and
record any approved deviation. Complete scope, context, deliverables, visual locks, states,
variants, animation plan, provenance needs, and acceptance evidence before generating or
authoring a large batch.

The brief remains the production contract for the family. It links to owning rules rather than
copying them, and it is updated when an approved decision changes the family contract.

### 3. Representative Visual Target

- Inspect existing references and related runtime assets before proposing a direction.
- Produce or select one representative asset, state set, or small style board.
- Compare it with the applicable visual references at the same display size.
- Review it on representative light, dark, neutral, and illustrated backgrounds where relevant.
- Reject an attractive candidate when it belongs to a different visual system.

The target proves visual intent only. It does not prove slicing, alpha, dimensions, pivots,
animation, import behavior, or runtime performance.

### 4. Visual Approval

Visual approval requires an explicit recorded decision. The accepted source, revision, reviewer,
date, applicable reference comparison, and remaining conditions are recorded together.

Approval locks the accepted identity and visual intent. It does not imply that the asset is
production-ready or that untested derivatives share the approval automatically.

### 5. Family Production

- Reuse the accepted target as the visual seed for related states and variants.
- Keep view, scale, silhouette logic, palette roles, material treatment, light direction, edge
  treatment, and detail density invariant unless the brief defines a change.
- Produce small coherent batches and compare each batch with the same target.
- Change one controlled variable per revision where practical.
- Keep placeholders visibly distinct from candidate and approved sources.

### 6. Deterministic Normalization

Normalize outside any generative or preview tool:

- crop, canvas, dimensions, aspect ratio, content bounds, padding, and safe areas;
- alpha edges, masks, premultiplication behavior, and background removal;
- shared pivot, anchor, baseline, scale, orientation, and facing;
- frame slicing, atlas regions, tile edges, nine-slice insets, and collision-related geometry;
- color space, bit depth, filtering, mipmaps, repeat, compression, and export format;
- layer names, file names, variant names, version identifiers, and package paths; and
- checksums or equivalent identity evidence for stable masters where appropriate.

Generated grids, transparent backgrounds, seams, frame counts, topology, and dimensions are never
accepted without inspection.

### 7. Runtime Package and Handoff

The runtime package is derived from the accepted source and contains only the files required by the
client. It includes or links to the family manifest, import expectations, state recipes, aligned
layers, and validation targets.

The handoff identifies:

- stable asset ID, family, revision, status, and owning brief;
- exact source master, runtime exports, and evidence paths;
- canvas, content bounds, alpha, pivot, layer order, states, and variants;
- animation groups, reduced-motion behavior, and interruption requirements;
- filtering, mipmaps, compression, repeat, atlas, shader, and material expectations;
- engine resource or import target when known; and
- remaining gates that prevent production signoff.

Implementation preserves the accepted appearance. It does not compensate for a defective source
package with undocumented screen-specific offsets, scaling, recoloring, masks, or timing changes.

### 8. Runtime Validation

Test the assembled asset in the contexts named by the brief:

- at every required native display size;
- at `1920x1080`, `1280x960`, and `1280x800` where the asset participates in a full composition;
- against representative backgrounds and neighboring content;
- in all required interaction, gameplay, product-semantic, and error states;
- in representative motion, interruption, and reduced-motion presentations;
- under realistic simultaneous-effect and content-density conditions; and
- on every target platform or rendering path that can materially change the result.

Isolated full-size previews support review but do not replace native-scale or in-engine evidence.

### 9. Production Signoff

Production signoff occurs only when every applicable gate passes and the manifest, package, owning
brief, runtime mapping, and evidence agree. A failed or unassessed applicable gate prevents the
`Production-ready` status without automatically revoking the accepted visual direction.

## Status Model

| Status | Meaning | Minimum evidence |
|---|---|---|
| `Draft` | The responsibility or solution is still being defined | Owning requirement and initial brief |
| `Candidate` | A reviewable solution exists | Inspectable output, defined context, technical frame, and comparison target |
| `Approved` | Visual identity and intent are explicitly accepted | Recorded approval, reference comparison, readability review, and provenance |
| `Production-ready` | The normalized runtime package satisfies the accepted intent | All applicable visual, technical, accessibility, motion, provenance, native-scale, and runtime gates pass |

Status belongs to a specific source or package revision. Approval of a concept reference does not
approve a runtime asset, and approval of one state does not approve an unreviewed family.

## Quality Result Vocabulary

| Result | Meaning |
|---|---|
| `Pass` | Required evidence exists and satisfies the gate |
| `Fail` | Evidence shows that the asset does not satisfy the gate |
| `Not Assessed` | The gate applies, but evidence has not been produced or reviewed |
| `Not Applicable` | The gate does not apply and the reason is recorded |

`Not Assessed` is not a pass. Every applicable gate must be `Pass` before production signoff.

## Acceptance Gates

### Visual Cohesion

- Matches the applicable shared and subject-specific direction.
- Preserves shape, palette roles, materials, lighting, edge treatment, and detail density.
- Introduces no painterly drift, random noise, sharpening halos, uncontrolled bloom, or global
  color cast.

### Identity and Gameplay Read

- Required silhouette, symbols, disconnected parts, and identity marks remain unchanged.
- State, selection, availability, warning, and result are not communicated by color or motion alone.
- Focal details survive the smallest intended display size and representative background.
- The asset does not reveal hidden information or imply unsupported gameplay meaning.

### Technical Fit

- Dimensions, bounds, alpha, color space, naming, pivots, layers, and export settings are verified.
- Related layers share one canvas, coordinate system, pivot, scale, and orientation.
- Glow, travel, rotation, scale, particles, and shadows remain inside reserved bounds.
- Dynamic copy and changing values are not baked into raster art.

### Accessibility

- Meaning remains understandable without color, glow, animation, sound, or pointer hover alone.
- Contrast, focus, selection, warning, disabled, and success cues are checked in context.
- Motion-capable states have an equivalent low-motion presentation.
- Meaningful documentation images include useful alternative text.

### Motion and VFX

- Identity, volume, anchor, baseline, layer order, and final state remain stable.
- Effects have a readable source, affected area, and controlled falloff.
- Interruption produces one deterministic correct state.
- Decorative loops stop when hidden, irrelevant, or overridden by higher-priority feedback.

### Performance and Runtime

- Import settings preserve the accepted appearance.
- Memory, texture, material, particle, overdraw, geometry, and animation costs fit the recorded
  budget or target profile.
- Platform derivatives preserve visible identity and information hierarchy.
- Runtime output matches the accepted source at native scale.

### Provenance and Rights

- Source, creator or tool, date, license or generation record, attribution, restrictions, edits,
  approval, and reviewer are recorded.
- Rights are verified at the original source rather than inferred from availability or price.
- Attribution and restrictions survive renaming, conversion, atlas packing, and derivative work.
- Sensitive purchase or account evidence is stored outside public project content.

## Animation-Ready Construction

Identify all parts that may move, rotate, scale, pulse, glow, fade, unlock, break, fill, or change
state before producing the family.

- Keep independently controlled parts on separate transparent layers.
- Keep structural bases separate from canonical identity, state, glow, particles, highlights,
  locks, shadows, and optional effects.
- Preserve identity marks as unchanged layers and animate them as a whole only.
- Give aligned layers one canvas, coordinate system, pivot, scale, and naming convention.
- Reserve transparent padding for all intended travel, rotation, bloom, and pulse.
- Record back-to-front layer order, state recipes, default opacity, animation groups, and reduced-
  motion behavior in the manifest.

Use the [Animation and VFX Direction](../animation_vfx/animation_vfx_direction.md) for motion
priority, elemental behavior, interruption, accessibility, and validation.

## Stable Identity, Naming, and Versioning

### Stable IDs

Use an uppercase, domain-oriented stable ID that names responsibility rather than a temporary file
location, for example `CARD-FRAME-CREATURE` or `FX-SCREEN-TRANSITION`.

The stable ID remains the same while the responsibility remains the same. A visible source or
runtime-package revision receives an explicit version such as `v001`, `v002`, or later.

### Files and Packages

- Use descriptive filenames containing responsibility, variant, state, layer, and size where
  relevant.
- Keep candidate and approved revisions in distinct versioned locations.
- Do not overwrite an accepted stable source with an unapproved descendant.
- Keep source masters, normalized runtime exports, and validation evidence distinguishable.
- Record exact repository paths in the manifest instead of relying on folder convention alone.

### Replacement

Create a versioned sibling for a proposed replacement. Compare it with the accepted source, review
all affected states and contexts, and update stable references only after explicit approval.

When a stable source changes, update its brief, manifest, owning art documentation, runtime mapping,
and affected validation evidence together.

## Manifest Contract

Every produced family has a machine-readable or equivalently structured record containing:

| Field | Required content |
|---|---|
| Identity | Stable ID, family name, version, status, owner, and brief path |
| Product link | Owning design document or requirement ID |
| Visual authority | Applicable art documents and accepted source path |
| Technical frame | Dimensions, format, alpha, color space, bounds, pivot, scale, and orientation |
| Files | Source masters, runtime exports, layers, variants, and evidence |
| States | Required states, layer visibility, opacity, and assembly recipe |
| Motion | Animation groups, padding, interruption, loops, and reduced-motion behavior |
| Import | Filtering, mipmaps, compression, repeat, atlas, material, and shader expectations |
| Provenance | Origin, creator or tool, date, license, attribution, restrictions, and edit history |
| Validation | Contexts, native sizes, result per gate, evidence paths, failures, and required follow-up |
| Approval | Reviewer, decision, date, accepted revision, and production signoff when achieved |

The brief explains intent; the manifest describes the produced package. Do not maintain two
conflicting copies of the same technical fact.

## Traceability Contract

Every family must be traceable in both directions:

```text
requirement -> visual rule -> brief -> accepted source -> manifest -> runtime resource -> evidence
evidence -> runtime resource -> manifest -> accepted source -> brief -> visual rule -> requirement
```

Minimum traceability includes exact links for the product requirement, visual authority, brief,
accepted source, package record, runtime mapping, and validation evidence.

## Change and Failure Handling

- A visual-identity failure returns the proposed direction to `Candidate`.
- A technical or runtime failure may leave the visual source `Approved`, but the package is not
  `Production-ready`.
- Fix the source, export, import, or runtime layer responsible for the failure rather than hiding
  it with an unrelated compensation.
- Re-run every gate affected by a changed source, export setting, layer recipe, shader, material,
  animation, or runtime composition.
- Record `Not Applicable` with a reason instead of omitting a gate silently.
- Preserve enough version history and provenance to explain which source produced each runtime
  package.

## Review and Maintenance

Review this strategy when project-wide status meanings, directory ownership, handoff
responsibilities, target platforms, reference viewports, or production-readiness gates change.
Subject-specific visual changes belong in their owning art documents. Shared production baselines
belong here, required values for one family belong in its brief, and realized file properties and
validation results belong in its manifest.
