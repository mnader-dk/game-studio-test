# Forge Presentation Reference v001

- **Asset ID:** `SCENE-FORGE`
- **Status:** Candidate concept reference; not a production-ready runtime asset
- **Created:** 2026-10-30
- **Generation mode:** Built-in ImageGen with reference-guided generation and constrained viewpoint edits
- **Canvas:** `1254 × 1254`, PNG, RGB

## Design Decision

The Forge is represented by one compact magical smithing station rather than a complete workshop or
deck-building interface. Its identity comes from a contained arched hearth, one central anvil, a
curved magical Rune Bar integrated into the anvil pedestal, and one enchanted smithing hammer.

The green-blue energy is the single shared magical language across hearth, Rune Bar, and hammer.
The inset blank card-frame emblem on the anvil connects the landmark to deck preparation without
introducing loose cards, card racks, crafting actions, or changing runtime information.

## Views

| File | View | Purpose |
| --- | --- | --- |
| `forge_presentation_reference_v001_left_three_quarter.png` | Left three-quarter hero view | Primary presentation, material, magic, and construction reference |
| `forge_presentation_reference_v001_front.png` | Straight front view | Strongest silhouette and primary source for a future compact game icon |
| `forge_presentation_reference_v001_right_three_quarter.png` | Right three-quarter view | Confirms hearth depth, anvil geometry, pedestal construction, and hammer placement |

## Visual Locks

- Preserve the compact three-part read of arched magical hearth, central anvil, and single hammer.
- Preserve the anvil as the dominant physical object with a planar top, squared heel, clean horn,
  dark forged-iron body, restrained bronze bands, and inset blank card-frame emblem.
- Preserve the warm cream limestone platform and hearth, slate-blue structural insets, restrained
  antique bronze, dark forged iron, and limited warm walnut.
- Keep the hearth energy green-blue: turquoise-green core, cyan and azure ribbons, emerald wisps,
  dense local dust, and controlled cool illumination on nearby materials.
- Keep the curved Rune Bar centered on the anvil pedestal with seven readable bronze socket rings.
  Its effect is an irregular field of green-blue glow, mist, and dust distributed across the full
  length rather than seven repeated symbols, stones, or identical states.
- Keep one classic rectangular smithing hammer on the right ledge. Its forged-iron head, walnut
  handle, slate-blue grip, bronze details, green-blue seams, and local dust must remain materially
  grounded and visually subordinate to the anvil.
- Keep the magic visibly sourced and local. It must not become a portal, elemental glyph, poison
  cloud, full-screen haze, or substitute for the readable physical construction.

## Icon Derivation

Use the front view as the starting silhouette for a future square icon. Retain the arched hearth,
central anvil, and luminous Rune Bar as the three primary reads. Reduce individual masonry joints,
socket rings, dust particles, bronze brackets, and the separate hammer before changing the outer
silhouette. The icon requires its own brief, native-size exports, background tests, and explicit
approval; these concept renders are not icon deliverables.

## Reference Basis

- Rune Mastery Core Art Direction and the primary concept overview.
- Rune Mastery Environment Concept for limestone construction, material weight, and lighting.
- Approved Forge feature specification for deck preparation and Rune Bar configuration.
- Approved Shrine, Archive, and Chronicles presentation references for the shared material,
  rendering, viewpoint, and studio-presentation language.
- Three user-supplied photographs of historical forge interiors for credible anvil placement,
  hearth separation, tool scale, and workshop construction only; no room, machine, layout, or
  architectural detail is reproduced as canonical Forge design.

## Production Limits

- The three images are presentation references, not verified turntable renders or 3D orthographic
  projections; minor perspective and construction differences require resolution during modeling.
- No transparent layers, source geometry, pivots, masks, effect layers, collision, topology, UV,
  animation rig, or runtime package exist.
- The seven visible Rune Bar rings are a presentation abstraction and do not replace the approved
  runtime rule that a configurable deck Rune Bar contains ten positions.
- Runtime card lists, Rune order, deck validity, readiness, ownership, counters, labels, and
  interaction feedback must remain code-native.
- Native-size, grayscale, representative-background, responsive, animation, performance, and
  in-engine validation remain unassessed.
