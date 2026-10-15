---
title: Rune Mastery Core Art Direction
status: Draft
summary: Shared visual language for Rune Mastery across environments, characters, cards, UI art, and effects.
---

# Core Art Direction

## Purpose and Authority

This document is the source of truth for Rune Mastery's shared visual language. It defines the
qualities that must remain consistent across environments, characters, cards, UI art, icons, and
effects.

It does not define gameplay meaning, faction identity, component anatomy, exact design-token
values, or technical asset specifications. Those decisions belong to their owning design,
faction, component, or production documents. See the [Art Guidelines](../../README.md) for
ownership and workflow rules.

## Visual Goal

Rune Mastery presents an inviting, tangible fantasy world in which ancient stonework, crafted
objects, and elemental magic feel like parts of the same place. The image should feel polished and
magical without becoming noisy, grim, photorealistic, or visually overwhelming.

Strategic information remains easy to read. Magic supplies focused energy and identity; the
surrounding world supplies calm structure, material weight, and depth.

## Rendering Language

- Use clean, stylized 3D rendering with smooth modeled forms and coherent color planes.
- Build detail through geometry, silhouette, material separation, and lighting rather than surface
  noise.
- Keep silhouettes clean and anti-aliased, with soft modeled bevels instead of drawn outlines.
- Favor clear midtones, moderate saturation, gentle contrast, and controlled highlight rolloff.
- Use contact shadows and restrained ambient occlusion to separate overlapping forms.
- Keep the focal plane crisp while simplifying and softening peripheral or distant content.

Avoid watercolor or painterly surface treatment, visible brushwork, paper or canvas texture, flat
cel shading, photorealism, dense scratches, crunchy sharpening, edge halos, excessive bloom,
global fog, and a pervasive orange or pink color cast.

## Shape and Silhouette

| Area | Direction | Avoid |
|---|---|---|
| Characters and creatures | Friendly stylized proportions, large readable masses, expressive poses, controlled organic asymmetry | Fragile micro-shapes, visually merged limbs or equipment, detail that only reads in close-up |
| Environments and props | Broad architectural masses, rounded wear, stable construction, clear foreground-to-background separation | Uniform detail density, dense engraving, accidental spikes, noisy rubble silhouettes |
| Cards and UI art | Compact repeatable outer geometry, generous content areas, strong grouping, unmistakable primary symbols | Decorative framing that competes with content, irregular padding, baked text or changing data |
| Runes and magic | Stable glyph silhouettes surrounded by controlled energy and local effects | Redrawing identity through effects, effects that conceal the glyph, undifferentiated glow clouds |

The essential identity of an object or state must survive at its smallest intended display size.
Preserve the outer silhouette and primary internal symbol before secondary decoration.

## Value and Focus

Use value contrast deliberately to establish a clear reading order:

1. Active gameplay information, focal characters, and primary interaction targets.
2. Supporting objects, structural frames, and nearby environment forms.
3. Atmospheric depth, distant architecture, foliage, and decorative motion.

Do not distribute equal contrast and detail across the whole image. Backgrounds should support the
play space rather than compete with cards, controls, rune states, or effects. Every important state
must remain distinguishable in grayscale and may not depend on glow or color alone.

## Color Language

The shared world palette uses warm cream limestone, controlled slate and royal blues, warm brown
leather and wood, restrained antique gold or bronze, natural greens, and a clean blue sky fill.

Color has distinct responsibilities:

| Role | Direction |
|---|---|
| World and structure | Calm, materially grounded color planes that provide a neutral stage |
| Rune affinity | Localized elemental color paired with a stable glyph and material treatment |
| Interaction state | A combination of value, silhouette, border, symbol, or motion; never hue alone |
| Reward and celebration | Concentrated emphasis used sparingly so ordinary content remains calm |
| Faction identity | Defined by the owning faction guidance; it must not be reduced to an affinity recolor |

Fire, Air, and Forest are gameplay identities defined by the owning design documentation. This art
direction governs their shared presentation principles but does not replace their canonical glyphs
or state specifications. Exact color values belong in the future token source rather than this
document.

## Material Language

- Limestone is warm cream, opaque, softly worn, and never crystalline.
- Gold and bronze are controlled structural accents, not large mirror-chrome surfaces.
- Cloth uses broad readable folds; leather and wood use sparse, deliberate highlights.
- Foliage is grouped into simple masses before individual leaves are introduced.
- Elemental surfaces may emit light but must still read as dimensional material.
- Wear and texture should reinforce form, age, and scale without becoming visual noise.

Material choice does not imply rarity, power, ownership, availability, or faction by itself. Such
meanings require the cues defined by the owning system.

## Lighting

The default shared lighting character is:

1. a soft warm key light from the upper left;
2. a clean cool ambient fill that preserves readable shadow color;
3. controlled contact shadows that ground objects and separate layers; and
4. local, color-matched elemental light subordinate to the main form.

Bloom remains restrained and may not erase glyph geometry, card boundaries, or interaction cues.
Limestone, neutral surfaces, and skin tones must remain neutral enough to avoid a global warm cast.
Individual scenes may adapt exposure and mood while preserving form readability and material
identity.

## Detail and Edge Treatment

- Concentrate crisp detail around the current focal area.
- Simplify distant and peripheral forms before lowering foreground clarity.
- Use consistent bevel weight and clean modeled edges across related asset families.
- Keep texture frequency low enough that deterministic downscaling preserves the intended form.
- Treat particles, sparks, leaves, and magical trails as supporting accents, not as substitutes for
  a readable base asset.

## Camera and Composition

Rune Mastery is a screen-based card game, so shared art must serve the game view and its information
hierarchy rather than imply one universal world camera.

- Use perspective and depth to support fantasy scenes and card illustration without obscuring the
  subject silhouette.
- Reserve calm visual space around cards, controls, labels, and changing runtime content.
- Keep important subjects clear of crops, tangencies, and high-contrast background clutter.
- Treat rune glyphs, icons, and UI symbols as stable graphic forms; do not distort them to match
  scene perspective.
- Validate final composition inside the representative game viewport, not as an isolated image.

## Motion Character

Motion is responsive, soft, and materially grounded. Structural objects retain weight; magical
energy may breathe, pulse, or flow. Motion clarifies cause, focus, and state change before it adds
spectacle.

Functional feedback takes priority over navigation, celebration, and ambient motion in that order.
Lower-priority motion must yield when it competes with gameplay information. Every animated state
requires the same understandable final state without motion, and decorative loops must not become
the sole identity or status cue.

Exact timings, easing curves, animation layers, and interruption behavior belong to the relevant
motion or component specification.

## Primary Concept Reference

![Rune Mastery concept overview](../concepts/images/concept_reference/concept_overview_v001.png)

| Reference | Use | Status |
|---|---|---|
| [`concept_overview_v001.png`](../concepts/images/concept_reference/concept_overview_v001.png) | Evaluate the overall rendering character, palette balance, material family, elemental emphasis, and fantasy tone together | Concept reference |

Use the image as evidence for the shared direction described in this document. It does not approve
every depicted character design, environment, rune glyph, card frame, composition, or production
detail. More specific approved guidance takes precedence for the subject it owns.

## Review Checklist

A candidate fits the core art direction when:

- its surfaces read as modeled materials rather than painted or noisy patches;
- its major color planes remain calm and coherent;
- its silhouette and primary symbol read at the intended game scale;
- its detail comes from form, material separation, and controlled lighting;
- warm key light, cool fill, and local magic remain visually distinct;
- glow and decoration preserve gameplay information and component boundaries;
- state and identity remain understandable without relying on color or motion alone; and
- the candidate belongs beside the primary concept reference without introducing a conflicting
  rendering style.

Reject or revise a candidate when it fails more than one of these checks or when it conflicts with
an approved subject-specific authority.
