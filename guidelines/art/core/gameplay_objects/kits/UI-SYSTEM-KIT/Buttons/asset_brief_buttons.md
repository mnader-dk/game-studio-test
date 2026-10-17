---
title: Rune Mastery Buttons Asset Brief
summary: Visual and technical requirements for the shared Rune Mastery button family.
---

# Asset Brief — Buttons

## Purpose

Define the reusable frames, neutral surface, interaction layers, runtime outputs, and technical
construction of Rune Mastery's shared button family.

## Definition

| Field | Requirement |
|---|---|
| Asset ID and family | `UI-SYSTEM-KIT / Buttons` |
| Role and player-facing outcome | Provide tactile, readable action carriers that players can recognize and operate reliably with pointer or touch without confusing controls with decorative frames. |
| Target contexts | Login, Home, Duel, Forge, Shrine, Chronicles, Archive, Settings, overlays, and Match support UI at `1920 × 1080`, `1280 × 960`, and `1280 × 800`; light, dark, neutral, and illustrated backgrounds. |
| Scope | `UI-BUTTON-FRAME-STANDARD`, `UI-BUTTON-FRAME-COMPACT`, `UI-BUTTON-FRAME-ICON-SQUARE`, `UI-BUTTON-SURFACE-NEUTRAL`, and `UI-BUTTON-INTERACTION-STATES`; Large, Medium, and Small size tiers; `Default`, `Hover`, `Pressed`, `Focused`, `Disabled`, and `Loading` interaction states. Runtime text, icons, semantic action roles, tooltips, and product-specific state cues remain separate. |
| Dependencies | Core Art Direction, Art Production Strategy, Animation and VFX Direction, `UI-SP-ACTION`, shared Input and Accessibility rules, code-native typography, `UI-ICON-ACTION-CORE`, and the runtime loading indicator. |

## Deliverables

| Asset or group | Required states or variants | Source master | Runtime outputs |
|---|---|---|---|
| `UI-BUTTON-FRAME-STANDARD` | Large, Medium, Small | `768 × 256` layered RGBA master | Transparent PNG at `384 × 128`, `320 × 112`, and `256 × 96` |
| `UI-BUTTON-FRAME-COMPACT` | Large, Medium, Small | `512 × 256` layered RGBA master | Transparent PNG at `256 × 128`, `224 × 112`, and `192 × 96` |
| `UI-BUTTON-FRAME-ICON-SQUARE` | Large, Medium, Small | `256 × 256` layered RGBA master | Transparent PNG at `128 × 128`, `112 × 112`, and `96 × 96` |
| `UI-BUTTON-SURFACE-NEUTRAL` | Standard, Compact, Icon Square; Large, Medium, Small | Aligned surface masters at `768 × 256`, `512 × 256`, and `256 × 256` | One transparent surface layer aligned to every frame output |
| `UI-BUTTON-INTERACTION-STATES` | Hover, Pressed, Focused, Disabled, Loading for every frame and size; Default uses no overlay | State layers aligned to each corresponding frame master | One transparent PNG per state, frame type, and runtime size; loading symbol and text remain code-native |

## Visual Contract

| Field | Requirement |
|---|---|
| Shape and readability | Use substantial rounded rectangles with broad calm centers, softened fantasy shoulders, and clearly modeled edge depth. Standard and Compact share one construction language but remain distinguishable by proportion; Icon Square remains unmistakably `1:1`. Preserve the outer silhouette and state cue at the Small tier. |
| Color, material, and lighting | Use a quiet warm-cream or pale-parchment surface inside a controlled slate-blue structure with restrained antique-bronze accents. Materials read as clean stylized stone, ceramic, and crafted metal with low surface noise. Light with a soft warm upper-left key, cool fill, restrained contact shadow, and no broad glow. |
| View and composition | Straight-on orthographic UI presentation with shallow dimensional relief and no perspective distortion. Keep the center visually calm for code-native German or English labels and optional icons. Protect corners, end caps, bevels, and state markers from scaling. |
| Fixed elements | External bounds, corner geometry, bevel weight, light direction, content-safe region, centered pivot, nine-slice boundaries, and layer alignment remain identical across states. Text, icons, values, badges, semantic warnings, and loading indicators are never baked into the artwork. |
| Avoid | Painterly texture, photorealistic metal, mirror chrome, Gothic severity, sharp spikes, dense engraving, oversized gems, global bloom, elemental or faction identity, rarity cues, dominant warning colors, baked labels, and ornament that competes with the action. |

## Technical Contract

| Field | Requirement |
|---|---|
| Canvas and layout | Use the exact runtime canvases listed above on the `4 px` grid with centered pivots. Centered content-safe areas are Standard `256 × 80`, `208 × 72`, `160 × 64`; Compact `160 × 80`, `136 × 72`, `112 × 64`; Icon Square `64 × 64`, `56 × 56`, `48 × 48` for Large, Medium, Small. Every visual control remains within a hit area of at least `44 × 44`; adjacent targets use `8 px` spacing where possible. |
| Files and rendering | Source layers use lossless `16-bit RGBA`, `sRGB`, and straight alpha. Runtime exports use `PNG RGBA8`, `sRGB`, straight alpha, bilinear filtering, and no mipmaps. Transparent edge colors must match the adjacent material; atlas packing, when used, keeps at least `4 px` padding. |
| Scaling and assembly | Standard and Compact use nine-slice scaling with protected insets of `48 px` at Large, `40 px` at Medium, and `32 px` at Small; only the straight center spans may stretch. Icon Square scales uniformly and is never sliced or stretched. Assemble back to front as `contact shadow → neutral surface → structural frame → code-native icon/text → interaction-state layer`. |
| Motion and accessibility | State assets are static aligned layers; runtime transitions may use short opacity, value, or inset-depth changes. Hover is supplemental. Focus uses a persistent structural outline, Pressed changes relief, and Disabled reduces relief and interrupts the inner highlight so meaning does not rely on hue. Loading preserves the frame and uses a separate labeled activity indicator. Interruption resolves immediately to the newest valid state; reduced motion uses a direct state swap. |
| Platforms and performance | Shared 2D UI assets target desktop/browser and landscape tablet. Reuse one family texture set across all screens. Limit each button to frame, surface, and one interaction layer plus code-native content; use no particles, continuous decorative loop, per-button texture copy, or full-screen effect. |

## States and Events

| State or event | Meaning | Required presentation and non-color cue | Motion or VFX | Final and reduced-motion result |
|---|---|---|---|---|
| Default | The control is present and not currently targeted or manipulated; product availability remains a separate meaning. | Raised neutral surface, complete inner highlight, stable frame, and readable content area. | None. | Stable default composition. |
| Hover | A pointer is over the action. | Slight value lift and a narrow inner-edge response without changing bounds. | Short local fade; no pulse or travel. | Hover layer while targeted; direct swap for reduced motion. |
| Pressed | The player is actively pressing the action. | Surface appears inset, upper highlight contracts, and contact shadow shortens without moving the outer frame. | Short compression and release; repeated input does not queue decoration. | Resolve to Hover or Default after release; direct inset swap for reduced motion. |
| Focused | Input focus is on the action. | Persistent double-edge or corner-bracket outline with clear value contrast beyond the normal frame. | Optional single soft fade-in; no looping pulse required. | Focus marker remains until focus moves; direct appearance for reduced motion. |
| Disabled | The control is visible but cannot be operated. | Flatter relief, reduced contrast, and interrupted inner highlight; code-native copy or explanation remains available. | None; ignores activation feedback. | Stable disabled composition. |
| Loading | The action is waiting for completion and cannot be triggered again. | Base frame remains stable; a separate activity symbol and accessible status replace or accompany the normal content. | Restrained runtime rotation or pulse on the activity symbol only. | Resolve to the resulting state; reduced motion uses a static activity symbol and status. |
