---
title: Rune Mastery Surfaces and Layout Asset Brief
summary: Visual and technical requirements for shared panels, dividers, collection slots, and structural UI decoration.
---

# Asset Brief — Surfaces and Layout

## Purpose

Define the reusable structural surfaces that group, separate, and organize Rune Mastery's UI
content without competing with gameplay information or introducing screen-specific meaning.

## Definition

| Field | Requirement |
|---|---|
| Asset ID and family | `UI-SYSTEM-KIT / Surfaces and Layout` |
| Role and player-facing outcome | Provide calm, materially grounded containers, separators, slots, and optional ornament so players can understand content hierarchy, grouping, and boundaries before reading individual labels or controls. |
| Target contexts | Login, Home, Duel, Forge, Shrine, Chronicles, Archive, Settings, overlays, collection grids, and Match support UI at `1920 × 1080`, `1280 × 960`, and `1280 × 800`; light, dark, neutral, and illustrated backgrounds. |
| Scope | `UI-SURFACE-PANEL-FAMILY`, `UI-SURFACE-DIVIDER-FAMILY`, `UI-COLLECTION-AND-SLOT-FAMILY`, and `UI-DECORATION-FAMILY`; Large, Medium, and Small size tiers. Runtime layout, text, icons, cards, portraits, values, focus, selection, warnings, tooltips, scroll behavior, and product-specific state cues remain separate. |
| Dependencies | Core Art Direction, Art Production Strategy, Animation and VFX Direction, the shared Button family, code-native typography and layout tokens, shared focus and selection treatments, and the owning screen or component specification. |

## Deliverables

| Asset or group | Required states or variants | Source master | Runtime outputs |
|---|---|---|---|
| `UI-SURFACE-PANEL-FAMILY` | Content, Inset, Floating; Large, Medium, Small | One layered `1536 × 768` RGBA master per variant | Transparent PNG at `768 × 384`, `512 × 256`, and `384 × 192` per variant |
| `UI-SURFACE-DIVIDER-FAMILY` | Horizontal and Vertical; Standard and Emphasis; Large, Medium, Small | Horizontal `2560 × 384`; Vertical `384 × 1536`; layered RGBA | Horizontal PNG at `1280 × 192`, `960 × 144`, and `640 × 96`; Vertical PNG at `192 × 768`, `144 × 576`, and `96 × 384` |
| `UI-COLLECTION-AND-SLOT-FAMILY` | Square Slot and Collection Boundary; neutral structural presentation; Large, Medium, Small | Slot `256 × 256`; Collection Boundary `1536 × 512`; layered RGBA | Slot PNG at `128 × 128`, `112 × 112`, and `96 × 96`; Collection Boundary PNG at `768 × 256`, `512 × 192`, and `384 × 160` |
| `UI-DECORATION-FAMILY` | Corner Bracket, Edge Clasp, Divider End Cap, and Junction; neutral and mirrored orientations where required; Large, Medium, Small | One centered `256 × 256` layered RGBA master per element | Transparent PNG at `128 × 128`, `112 × 112`, and `96 × 96`; mirrored derivatives are deterministic exports rather than separately redrawn art |

## Visual Contract

| Field | Requirement |
|---|---|
| Shape and readability | Use broad rounded rectangles, stable straight spans, softened fantasy shoulders, and shallow modeled relief. Content, Inset, and Floating panels must remain distinguishable through edge construction and elevation without relying on color. Dividers establish hierarchy without becoming visual bars; slots read as receptive spaces rather than buttons. |
| Color, material, and lighting | Use quiet warm-cream or pale-parchment content surfaces within controlled slate-blue structure and restrained antique-bronze accents. Materials read as clean stylized limestone, ceramic, and crafted metal with low surface noise. Use a soft warm upper-left key, cool fill, restrained contact shadow, and no broad glow. |
| View and composition | Straight-on orthographic UI presentation with no perspective distortion. Protect large calm center regions for code-native content. Keep the highest contrast at the structural edge nearest the contained content; outer shadows remain soft enough to preserve readability over illustrated backgrounds. |
| Fixed elements | External bounds, corner construction, bevel weight, light direction, content-safe regions, centered pivots, nine-slice boundaries, protected divider end pieces, and aligned layer coordinates remain stable across tiers and variants. Canonical icons, labels, values, cards, portraits, badges, and semantic state symbols are never baked into the artwork. |
| Avoid | Painterly texture, paper grain, photorealistic metal, mirror chrome, Gothic severity, sharp spikes, dense engraving, large gems, elemental or faction identity, rarity cues, broad bloom, opaque full-screen plates, ornamental frames around every item, baked labels, and decoration that implies an unavailable interaction. |

## Technical Contract

| Field | Requirement |
|---|---|
| Canvas and layout | Use the exact canvases above on the `4 px` grid with centered pivots. Panel nine-slice insets are Large `96 / 80 px`, Medium `64 / 52 px`, and Small `48 / 40 px` for horizontal/vertical edges, yielding minimum calm content areas of `576 × 224`, `384 × 152`, and `288 × 112`. Collection Boundary insets are Large `64 / 48 px`, Medium `48 / 40 px`, and Small `40 / 32 px`. Slot content-safe squares are `80`, `72`, and `64 px`. Horizontal divider end caps protect `128`, `96`, and `64 px` at each end; Vertical dividers protect the same values at top and bottom. Decoration stays outside content-safe regions and at least `16 px` from code-native text or icons. |
| Files and rendering | Source layers use lossless `16-bit RGBA`, `sRGB`, and straight alpha. Runtime exports use `PNG RGBA8`, `sRGB`, straight alpha, bilinear filtering, and no mipmaps. Transparent edge colors match the adjacent material. Atlas packing, when used, keeps at least `4 px` padding and preserves each nine-slice or divider guide exactly. |
| Scaling and assembly | Panels and Collection Boundaries use nine-slice scaling; only documented straight center spans may stretch. Dividers preserve their cross-axis thickness and aspect of end caps while only the central rail extends. Slots and decorations scale uniformly and are never non-uniformly stretched. Assemble back to front as `contact shadow → panel surface → divider or slot structure → optional decoration → code-native content → interaction or semantic state treatment`. |
| Motion and accessibility | Base assets are static. Runtime panel or overlay transitions may animate position, opacity, and contact shadow while keeping the final boundary readable without motion. Focus, selection, warning, and invalid states belong to separate shared layers and must use a structural, value, or symbol cue in addition to color. Interruption resolves immediately to the newest valid layout; reduced motion uses a direct swap. Decorative elements may be removed at compact widths without changing meaning. |
| Platforms and performance | Shared 2D UI assets target desktop/browser and landscape tablet. Reuse the family across screens and pack compatible outputs into texture pages no larger than `2048 × 2048`. Avoid overlapping full-panel alpha layers, screen-specific texture copies, continuous shaders, particles, and decorative animation. Keep hidden or clipped panels out of draw submission where the client supports it. |

## States and Events

| State or event | Meaning | Required presentation and non-color cue | Motion or VFX | Final and reduced-motion result |
|---|---|---|---|---|
| Content panel | Primary structural grouping for related information or controls. | Complete raised boundary, broad calm center, and stable spacing around contained content. | None by default. | Stable Content panel composition. |
| Inset panel | Subordinate region nested inside a larger surface. | Recessed inner edge, reduced elevation, and interrupted outer shadow distinguish it from Content and Floating panels. | None by default. | Stable Inset panel composition. |
| Floating panel | Temporary overlay, modal, popover, or elevated support region; blocking behavior remains code-owned. | Strongest family elevation and complete outer boundary without warning color or excessive contrast. | Optional short runtime fade and shallow travel. | Stable Floating panel; direct appearance for reduced motion. |
| Standard divider | Separates peers or sections without creating a new container. | Continuous low-contrast rail with protected end pieces and clear orientation. | None. | Stable divider. |
| Emphasis divider | Marks a stronger hierarchy break without implying warning or selection. | Additional central bridge, clasp, or value step; thickness and end-cap language remain in-family. | None. | Stable emphasis divider. |
| Empty slot | A collection position exists and contains no runtime item. | Receptive inset well with an unobstructed content-safe square; no baked icon or plus sign. | None. | Stable empty slot. |
| Occupied slot | Runtime content is present in the slot. | The same structural slot remains visible around separately rendered content; no geometry shift or recolored base is required. | Content motion, if any, is owned by the containing component. | Stable slot and content assembly. |
| Focused, selected, targeted, invalid, or unavailable | An owning component applies interaction or product meaning to a surface or slot. | Preserve the structural base and add the shared code-native border, symbol, value, or mask treatment; do not encode meaning through a decoration-family swap. | Short local transition only when defined by the owning component. | Deterministic newest state; direct swap for reduced motion. |
| Responsive reflow | Layout recomposes for `1280 × 960` or `1280 × 800`. | Re-anchor or reassemble surfaces and dividers; omit optional decoration before shrinking required content below the Small tier. | Optional short runtime layout transition. | Same grouping and reading order with decoration reduced or absent. |
