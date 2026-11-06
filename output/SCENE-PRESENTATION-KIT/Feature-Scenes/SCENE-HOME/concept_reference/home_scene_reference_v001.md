# Home Scene Presentation Reference v001

- **Asset ID:** `SCENE-HOME`
- **Status:** Approved concept reference; not a production-ready runtime asset
- **Created:** 2026-11-04
- **Generation mode:** Built-in ImageGen with reference-guided generation, constrained composition
  edits, and targeted UI repair
- **Canvas:** `1920 × 1080`, PNG, RGB

## Design Decision

The Home scene is represented as one bright magical academy courtyard that acts as the visual and
navigation hub for five destinations: Archive, Shrine, Forge, Chronicles, and Duel. Its identity
comes from a centered circular Duel platform, one floating horizontal card deck, and a layered
arrangement of limestone stairs and destination landmarks around the platform.

The central deck is the primary focal object and uses blue-and-gold covers, clearly separated card
layers, and one narrow brown leather strap with a crossed-swords badge. Each surrounding landmark
keeps its own magical color and physical silhouette while sharing the same cream limestone, royal
blue, antique gold, foliage, and warm-light material language.

## Views

| File | View | Purpose |
| --- | --- | --- |
| `home_scene_reference_v001.png` | Straight-on wide hub view | Primary composition, architecture, navigation, material, lighting, and UI-placement reference |

## Visual Locks

- Preserve the five-destination read of Archive, Shrine, Forge, Chronicles, and Duel.
- Preserve the centered circular Duel platform and the floating horizontal deck as the dominant
  focal hierarchy.
- Preserve the deck's blue-and-gold covers, readable stacked card contours, narrow brown leather
  strap, and crossed-swords badge.
- Preserve the broad stepped courtyard composition, continuous stair runs, coherent balustrades,
  and readable walkable routes to every destination.
- Keep the destination buttons integrated into low limestone plinths. Preserve open side paths at
  the Forge and Chronicles plinths and the stair-integrated Shrine placement.
- Preserve the corrected Chronicles stair transitions with matched tread and riser elevations and
  a subtly perspective-aligned plinth.
- Preserve continuous Forge stairs and the Forge plinth's optical centering on its stair run.
- Preserve the warm cream and ivory limestone, royal blue insets, restrained antique gold and
  bronze, chestnut leather and wood, deep green foliage, and warm lantern light.
- Keep each magical identity local and readable: blue Duel energy, violet Shrine energy, cyan and
  green-blue Forge energy, and blue Archive energy. Effects must not dissolve the architecture or
  deck contours into uncontrolled bloom or haze.
- Preserve crisp material separation, deep-focus readability, clear tread noses, stone joints,
  foliage silhouettes, paper layers, and prop contours.
- Preserve the visible UI composition, exact destination labels, player name `RUNKEEPER`, and the
  circular blue Rune Dust/swirl icon as placement references only.
- Keep the cyan diamond absent from the front of the Chronicles book display.

## Scene Derivation

Use this wide view as the binding visual target for a future engine-native Home scene. Reconstruct
the architecture, destination landmarks, deck, magic, lighting, and UI as separate assets and
systems while preserving the approved spatial hierarchy and screen-space balance. Reduce small
masonry joints, foliage leaves, particles, and distant landscape detail before changing landmark
silhouettes, stair geometry, walkable routes, or the central deck's proportions. Runtime UI and
interaction require their own responsive layouts, states, native-size exports, and explicit
in-engine approval; the baked presentation UI is not a runtime deliverable.

## Reference Basis

- Rune Mastery Core Art Direction and the primary concept overview.
- Rune Mastery Environment Concept for limestone construction, courtyard scale, palette, distant
  landscape, material weight, and daylight.
- Approved scene presentation references for landmark identity, shared materials, rendering
  clarity, magic language, and detail density:
  - [Archive Presentation Reference v001](../../SCENE-ARCHIVE/concept_reference/archive_presentation_reference_v001.md)
  - [Shrine Presentation Reference v001](../../SCENE-SHRINE/concept_reference/shrine_presentation_reference_v001.md)
  - [Forge Presentation Reference v001](../../SCENE-FORGE/concept_reference/forge_presentation_reference_v001.md)
  - [Chronicles Presentation Reference v001](../../SCENE-CHRONICLES/concept_reference/chronicles_presentation_reference_v001.md)
  - [Duel Presentation Reference v001](../../SCENE-DUEL/concept_reference/duel_presentation_reference_v001.md)
- The user-approved Home composition and iterative corrections for deck construction, stair
  continuity, plinth placement, walkable side paths, Chronicles perspective, UI labels, and final
  color and sharpness polish.

## Production Limits

- The image is a presentation reference, not verified 3D geometry, an orthographic projection, or
  a navigable level; perspective and construction details require resolution during implementation.
- No transparent layers, isolated sprites, source geometry, pivots, masks, effect layers,
  collision, topology, UV, animation rig, light setup, or runtime package exist.
- The player identity, currencies, timers, notification states, destination labels, navigation
  icons, and interaction feedback must remain code-native.
- The background landscape and architecture are not yet separated for parallax, responsive
  framing, localization-safe UI, or alternate aspect ratios.
- Walkability, collision clearance, camera motion, focus order, controller navigation, readability,
  accessibility, animation, performance, and in-engine validation remain unassessed.
