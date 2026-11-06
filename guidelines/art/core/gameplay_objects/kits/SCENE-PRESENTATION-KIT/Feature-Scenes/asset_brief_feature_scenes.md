---
title: Rune Mastery Feature Scenes Asset Brief
status: Approved
approved: 2026-11-06
summary: Visual and technical production contract for feature-scene asset packages, beginning with the Home scene.
---

# Asset Brief — Feature Scenes

## Purpose

Define the visual form, layer separation, runtime outputs, responsive behavior, and acceptance
criteria for Rune Mastery's feature scenes. This initial production revision covers `SCENE-HOME`
only. Archive, Shrine, Forge, Chronicles, Duel, and all other feature-scene runtime packages remain
outside this brief's current production scope.

## Definition

| Field | Requirement |
|---|---|
| Asset ID and family | `SCENE-PRESENTATION-KIT / Feature Scenes / SCENE-HOME` |
| Role and player-facing outcome | Provide the persistent meta-game hub where the player immediately recognizes Archive, Shrine, Forge, Chronicles, and Duel; sees relevant status; and can choose the next activity without losing Duel as the central action. |
| Target contexts | Fixed-camera layered 2D/2.5D Home scene for desktop, browser, and landscape tablet. Composition master at `1920 × 1080`; responsive validation at `1280 × 960` and `1280 × 800`. Neighboring content includes code-native player identity, resource displays, notifications, navigation controls, focus treatment, and contextual prompts. |
| Scope | Background depth layers; static courtyard architecture; foreground framing; five physical destination landmarks; central Duel platform; central card deck; local magic, light, and ambient VFX layers; contact shadows and emission masks; responsive anchors and crop-safe rules; composite preview and validation evidence. |
| Explicit exclusions | Runtime text, numbers, timers, localization, player data, notification logic, semantic availability, focus order, input handling, audio, screen transitions, gameplay rules, and client-specific scene or shader files. The concept image is not shipped as one flattened interactive screen. |
| Dependencies | Approved [Home Scene Presentation Reference v001](../../../../../../../output/SCENE-PRESENTATION-KIT/Feature-Scenes/SCENE-HOME/concept_reference/home_scene_reference_v001.md); Core Art Direction; Environment Concept; Animation and VFX Direction; Art Production Strategy; shared Button, Navigation, Player Identity, Resource Display, Notification, Rune Dust, and Rested Bonus families; approved Archive, Shrine, Forge, Chronicles, and Duel presentation references. |

## Production Strategy

`SCENE-HOME` uses a fixed-camera layered 2D/2.5D construction. Physical architecture, props,
foreground framing, local magic, and code-native UI remain independently controllable. A complete
3D environment, free camera, character navigation, and reconstructed off-screen world are not part
of this revision.

The approved concept reference defines composition and appearance but does not contain usable
layers. Hidden surfaces and clean plates must be deliberately reconstructed; they may not be
inferred by cutting overlapping pixels from the flattened image.

## Deliverables

| Asset or group | Required states or variants | Source master | Runtime outputs |
|---|---|---|---|
| `BG-HOME-SKY` | Daylight default | Aligned `1920 × 1080` opaque PNG master | Opaque PNG, full composition canvas |
| `BG-HOME-CLOUDS` | Static base; optional restrained drift layer | Aligned `1920 × 1080` RGBA PNG master with overlap beyond visible bounds | Transparent PNG layer or engine-native equivalent |
| `BG-HOME-DISTANT-LANDSCAPE` | Mountains, valley, distant city | Aligned `1920 × 1080` RGBA PNG master with completed hidden edges | Transparent PNG layer, independently reframeable |
| `ENV-HOME-COURTYARD-BASE` | Clean architecture without landmark magic, UI, labels, or dynamic light | Aligned `1920 × 1080` RGBA PNG master | Transparent or opaque PNG according to final stacking plan |
| `ENV-HOME-FOREGROUND-FRAMING` | Left and right stone-and-foliage groups | Separate aligned RGBA masters | Two content-trimmed transparent PNGs with manifest-recorded offsets |
| `LANDMARK-HOME-ARCHIVE` | Physical architecture and props; magic excluded | Aligned RGBA master with completed occluded edges | Content-trimmed transparent PNG plus anchor metadata |
| `LANDMARK-HOME-SHRINE` | Portal frame, bowls, stairs, and plinth; magic excluded | Aligned RGBA master with completed occluded edges | Content-trimmed transparent PNG plus anchor metadata |
| `LANDMARK-HOME-FORGE` | Pavilion, anvil, tools, stairs, and plinth; magic excluded | Aligned RGBA master with completed occluded edges | Content-trimmed transparent PNG plus anchor metadata |
| `LANDMARK-HOME-CHRONICLES` | Pavilion, book display, stairs, and plinth; magic excluded | Aligned RGBA master with completed occluded edges | Content-trimmed transparent PNG plus anchor metadata |
| `LANDMARK-HOME-DUEL-PLATFORM` | Circular platform, front stairs, and plinth; deck and magic excluded | Aligned RGBA master | Content-trimmed transparent PNG plus anchor metadata |
| `PROP-HOME-DUEL-DECK` | Blue-and-gold deck, readable card layers, leather strap, crossed-swords badge | Layered RGBA master separating body, strap and badge, contact shadow, and emission mask | One physical transparent PNG plus optional independent strap/badge layer, shadow, and emission mask |
| `FX-HOME-ARCHIVE-MAGIC` | Idle loop and reduced-motion still | Aligned effect master or loop source with source mask | Transparent sequence, sprite sheet, shader mask, or particle textures selected during implementation |
| `FX-HOME-SHRINE-MAGIC` | Portal idle, bowl magic, reduced-motion still | Aligned effect master or loop source with source mask | Transparent sequence, sprite sheet, shader mask, or particle textures selected during implementation |
| `FX-HOME-FORGE-MAGIC` | Hearth idle and reduced-motion still | Aligned effect master or loop source with source mask | Transparent sequence, sprite sheet, shader mask, or particle textures selected during implementation |
| `FX-HOME-DUEL-AURA` | Deck aura, localized ribbons, platform glow, reduced-motion still | Aligned effect master separating glow, ribbons, and particles | Transparent sequences or masks; no baked deck or platform pixels |
| `FX-HOME-LANTERN-AND-AMBIENT` | Lantern flicker, sparse motes, optional foliage/cloud motion, reduced-motion still | Small coherent effect family on aligned or asset-local canvases | Reusable transparent sequences, masks, or engine-native particle inputs |
| `SCENE-HOME-LAYER-MAP` | Design master and responsive annotations | Annotated `1920 × 1080` image plus machine-readable layer list | Production evidence; not shipped at runtime |
| `SCENE-HOME-COMPOSITE-PREVIEW` | Default, reduced motion, `1920 × 1080`, `1280 × 960`, `1280 × 800` | Deterministic assembly from accepted layers | Review captures; not shipped as the interactive scene |

Content-trimmed runtime dimensions are derived from the approved Layer Map on the `4 px` grid and
recorded in the manifest. They are not chosen independently during generation.

## Visual Contract

| Field | Requirement |
|---|---|
| Shape and readability | Preserve the five-destination read, centered Duel platform, floating horizontal deck, broad stair rhythm, continuous balustrades, and open routes around stair-integrated plinths. Destination silhouettes remain recognizable without their text labels or magic. The deck remains the primary foreground focal object. |
| Color, material, and lighting | Warm cream and ivory limestone; royal and slate blue structural planes; restrained antique gold and bronze; chestnut leather and wood; natural deep greens; warm lantern light; blue Duel and Archive magic; violet Shrine magic; cyan and green-blue Forge magic. Use a soft warm upper-left key, cool fill, grounded contact shadows, and controlled local illumination. |
| View and composition | Straight-on fixed wide view matching the approved `1920 × 1080` reference. Keep the Duel platform near the horizontal center and the destination hierarchy intact. Responsive layouts re-anchor or recompose independent layers; they never stretch the full scene or flatten all content into one cover crop. |
| Fixed elements | Five destinations and their relative hierarchy; central deck proportions and leather crossed-swords restraint; corrected Chronicles tread and riser transitions; open side paths at Forge and Chronicles; stair-integrated Shrine plinth; continuous Forge stairs; absent cyan diamond at the Chronicles book; crisp modeled edge treatment; exact landmark identity from the linked concept references. |
| Avoid | Watercolor softness, painterly smearing, global haze, uncontrolled bloom, noisy stone, pervasive orange cast, disconnected magic clouds, baked labels or values, duplicated architecture, false walkable edges, non-uniform scaling, flattened UI, and attractive isolated assets that no longer belong to the approved Home composition. |

## Technical Contract

| Field | Requirement |
|---|---|
| Canvas and layout | Source alignment uses the `1920 × 1080` composition canvas and `4 px` grid. Full-canvas layer origin is top-left `(0, 0)`. Trimmed runtime sprites retain manifest-recorded source bounds, pivot, and composition offset. UI-safe inset is `64 px` at `1920 × 1080` and `48 px` at both validation viewports. Interactive targets remain at least `44 × 44 px`. |
| Files and rendering | Aligned source layers use lossless PNG, `RGBA8` or `RGB8` as applicable, `sRGB`, and straight alpha. Runtime raster exports use PNG `RGBA8`/`RGB8`, `sRGB`, transparent edge colors matched to adjacent materials, bilinear filtering, no repeat, and at least `4 px` atlas padding. Mipmaps are enabled only where the runtime asset is materially downscaled. Client-specific compression remains unapproved until a client exists. |
| Scaling and assembly | Preserve aspect ratio and use uniform scale only. Assemble back to front as `sky → clouds → distant landscape → courtyard base → physical landmarks → local shadows → physical deck → emission/glow → particles → foreground framing → code-native UI`. Responsive layouts re-anchor landmark groups and UI; protected architecture, deck, and destination silhouettes may not be repaired with undocumented offsets or masks. |
| Motion and accessibility | Magic remains locally sourced and optional ambience stays subordinate. Hover and focus use shared UI states plus an optional restrained local landmark response; motion is never the sole interaction cue. Reduced motion uses static illuminated states with no looping ribbons, drifting particles, pulsing scale, or required animation. Interrupted transitions resolve directly to the newest valid scene or state. |
| Platforms and performance | Target desktop, browser, and landscape tablet. Use independently culled layers and reuse lantern, particle, and UI families. Final texture-memory, draw-call, shader, particle, and atlas budgets are `Not Applicable — no runtime client or rendering path exists in this repository`; production-ready status is blocked until those budgets and import behavior are validated in the target client. |

## States and Events

| State or event | Meaning | Required presentation and non-color cue | Motion or VFX | Final and reduced-motion result |
|---|---|---|---|---|
| Default / Return Home | Player can review status and choose the next activity | All five physical landmarks and code-native labels remain readable; Duel retains central scale and position | Restrained local idle magic and lantern ambience | Stable full composition; reduced motion uses static magic stills |
| First Arrival | Player reaches Home before the first guided Duel | Same physical scene; guidance belongs to separate contextual-prompt and focus systems | Optional single entrance emphasis on Duel; no mandatory full-screen animation | Resolves to Default; reduced motion applies immediate focus and prompt |
| Landmark hover | Pointer targets one destination | Shared hover treatment and optional local value lift; silhouette and label remain stable | Short local fade or light response; no geometry travel | Returns to Default on exit; reduced motion uses direct state swap |
| Landmark focus | Keyboard or controller focus targets one destination | Persistent shared focus outline or structural marker in addition to any color response | Optional single fade-in; no looping pulse required | Remains until focus moves; direct appearance for reduced motion |
| Landmark pressed / activated | Player confirms a destination | Pressed UI relief and a brief source-local response; destination identity does not move or deform | Short local contraction or light response followed by the shared screen transition | Resolves to the destination scene or restored Home state if cancelled |
| Contextual prompt or notification | Home presents relevant status or next-step information | Separate code-native panel, symbol, text, and focus order; environment never carries the meaning alone | Optional UI-owned entrance motion | Stable readable UI; direct appearance for reduced motion |

## Reference Authority

- [Home Scene Presentation Reference v001](../../../../../../../output/SCENE-PRESENTATION-KIT/Feature-Scenes/SCENE-HOME/concept_reference/home_scene_reference_v001.md) is the approved scene-level visual target.
- The linked Archive, Shrine, Forge, Chronicles, and Duel references own their landmark identity and
  take precedence when a small Home depiction is ambiguous.
- [Art Production Strategy](../../../../production/art_production_strategy.md) owns shared
  production, normalization, validation, and status rules.
- [Core Art Direction](../../../../direction/art_direction.md),
  [Environment Concept](../../../../environment/environment_concept.md), and
  [Animation and VFX Direction](../../../../animation_vfx/animation_vfx_direction.md) own shared
  rendering, environment, and motion language.
- Shared UI and progression families own their runtime frames, states, icons, text, and semantic
  behavior. The Home concept's baked HUD is placement guidance only.

## Acceptance Evidence

Step 1 approves this production contract only. Later production approval requires:

1. an approved `SCENE-HOME-LAYER-MAP` and complete asset manifest;
2. exact layer bounds, pivots, alpha, file format, naming, and source checks;
3. same-size comparison with the approved concept reference;
4. native-size contact sheets for landmarks, deck, and effects;
5. deterministic composite previews at `1920 × 1080`, `1280 × 960`, and `1280 × 800`;
6. proof that UI text, values, and interaction states remain code-native;
7. reduced-motion and non-color interaction evidence;
8. runtime import, responsive layout, performance, and interaction validation in the target client;
9. provenance records for every generated, edited, sourced, and derived file; and
10. explicit production signoff after all applicable gates pass.

## Next Step

After approval of this brief, create the `SCENE-HOME` asset manifest. The manifest assigns one
stable record to every deliverable above and fixes its source path, runtime path, status, bounds,
pivot, layer order, dependencies, provenance, and remaining validation gates. No production image
family should be generated before that manifest is reviewed.
