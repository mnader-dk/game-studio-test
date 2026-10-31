# Duel Presentation Reference v001

- **Asset ID:** `SCENE-DUEL`
- **Status:** Candidate concept reference; not a production-ready runtime asset
- **Created:** 2026-10-31
- **Generation mode:** Built-in ImageGen with reference-guided generation and constrained viewpoint edits
- **Canvas:** `1254 × 1254`, PNG, RGB

## Design Decision

The start of a duel is represented by one substantial upright deck made from many individually
readable cards. It levitates slightly above the floor in a shallow field of blue-white and
pale-gold magical dust, avoiding another table, pedestal, altar, or architectural support.

A centered leather-and-bronze securing strap gives the deck physical weight and carries a compact
crossed-swords emblem. The swords remain a small physical mark on the clasp rather than separate
floating weapons, so the deck and its cards stay visually dominant. The composition communicates
readiness and imminent activation without depicting a battlefield, match HUD, opponent, or game
mode.

## Views

| File | View | Purpose |
| --- | --- | --- |
| `duel_presentation_reference_v001_left_three_quarter.png` | Left three-quarter hero view | Primary presentation, card-layer construction, materials, clasp, and magic reference |
| `duel_presentation_reference_v001_front.png` | Straight front view | Strongest silhouette and primary source for a future compact game icon |
| `duel_presentation_reference_v001_right_three_quarter.png` | Right three-quarter view | Confirms deck thickness, strap wrapping, clasp depth, and opposite-side construction |

## Visual Locks

- Preserve the upright, closed deck as the single dominant object and keep its many individual
  card layers clearly readable from both three-quarter views.
- Preserve the tall rounded-rectangle silhouette, substantial deck thickness, warm cream card
  edges, royal-blue padded card back, restrained gold corner ornament, and antique-bronze frame.
- Keep the brown leather-and-bronze strap centered across the deck. Its upper and lower edges must
  follow the deck's local perspective, and the strap must wrap believably around the visible card
  thickness.
- Keep the bronze clasp centered on the broad front face with one cyan diamond accent and one dark
  shield inset carrying two compact crossed silver swords.
- Keep the crossed swords subordinate to the deck. They are a physical readiness emblem, not
  separate weapons, elemental characters, or the primary silhouette.
- Keep the deck free of a physical support. It levitates only slightly above a smooth ivory floor
  on an irregular, shallow dust cushion with a soft shadow and restrained reflection.
- Keep the magical language blue-white and pale gold: fine dust, small motes, soft glow, and a few
  loose wisps rising around the deck. Avoid a solid magic disc, portal, dense cloud, or large
  effects that obscure the card construction.
- Preserve the warm studio background, soft directional lighting, rounded stylized geometry,
  clean material separation, and presentation scale shared by the approved feature-scene family.

## Icon Derivation

Use the front view as the starting silhouette for a future square game-start icon. Retain the
upright deck, centered strap, crossed-swords clasp, blue card back, and concentrated lower dust
glow. Reduce individual card layers, quilt seams, corner ornament, small studs, dust particles,
and long wisps before changing the outer silhouette or enlarging the sword emblem. The icon
requires its own brief, native-size exports, background tests, and explicit approval; these
concept renders are not icon deliverables.

## Reference Basis

- Rune Mastery Core Art Direction and the primary concept overview.
- Rune Mastery Gameplay Object Concepts for card-back and deck readability.
- Approved Duel feature specification for deck selection, match-format selection, and starting a
  valid AI or human match.
- Approved Shrine, Archive, Chronicles, and Forge presentation references for the shared material,
  rendering, viewpoint, and studio-presentation language.
- User-directed iteration establishing the upright deck, centered perspective-correct strap,
  compact crossed-swords clasp, magical dust support, and removal of floating weapons and a
  physical pedestal.

## Production Limits

- The three images are presentation references, not verified turntable renders or 3D orthographic
  projections; minor perspective, card-count, ornament, and construction differences require
  resolution during modeling.
- No transparent layers, source geometry, pivots, masks, effect layers, collision, topology, UV,
  animation rig, or runtime package exist.
- The visible deck is a symbolic presentation object and does not define an exact runtime card
  count, card order, deck thickness, or legal deck composition.
- Match format, selected deck, validity, readiness, game mode, opponent, rewards, locks, labels,
  counters, matchmaking state, and interaction feedback must remain code-native.
- Native-size, grayscale, representative-background, responsive, animation, performance, and
  in-engine validation remain unassessed.
