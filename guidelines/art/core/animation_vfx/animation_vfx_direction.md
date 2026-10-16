---
title: Rune Mastery Animation and VFX Direction
status: Draft
summary: Shared motion language, effect hierarchy, animation-ready construction, accessibility rules, and review criteria for Rune Mastery.
---

# Animation and VFX Direction

## Purpose and Authority

This document is the source of truth for Rune Mastery's shared animation and visual-effects
direction. It defines how motion communicates cause, state, hierarchy, material, magic, and
celebration across the match, meta-game, cards, UI, characters, and environments.

It does not define gameplay timing, action legality, balance, component anatomy, exact token
values, sound behavior, engine architecture, or platform-specific implementation. Those decisions
belong to their owning design, component, audio, or technical documents.

## Motion Goal

Rune Mastery motion is responsive, soft, and materially grounded. It should make a deliberate
strategy game feel alive without turning every state change into spectacle.

- Functional feedback begins promptly and resolves clearly.
- Structural objects retain weight, alignment, and material integrity.
- Magical energy may breathe, gather, flow, discharge, or settle around a readable source.
- Motion explains cause and consequence before it adds personality or ornament.
- The final state remains understandable when the animation is skipped, interrupted, reduced, or
  missed.

The desired rhythm alternates calm decision space with short, legible moments of action. Constant
movement, equal emphasis, and overlapping celebration weaken the player's ability to read the
board and plan.

## Communication Priority

When multiple animations or effects compete, use this order:

1. **Blocking and corrective feedback:** errors, illegal targets, missing requirements, locks,
   warnings, and failed actions.
2. **Gameplay resolution and state change:** rune spending or restoration, card play, targeting,
   damage, healing, destruction, readiness, turn change, and confirmation.
3. **Interaction and navigation:** press, focus, selection, panel change, overlay transition, and
   spatial continuity.
4. **Progression and celebration:** rewards, unlocks, completion, claiming, and acquisition.
5. **Ambient presentation:** idle magic, environmental movement, decorative particles, and
   repeating background motion.

Higher-priority motion may suppress, shorten, simplify, or pause lower-priority motion. Ambient or
celebratory effects may never obscure required information, delay functional feedback, or block
input beyond the behavior defined by the owning game system.

## Motion Character by Material

| Subject | Motion character | Preserve | Avoid |
|---|---|---|---|
| Limestone and structural frames | Restrained, weighty, short travel, firm settle | Construction, joints, alignment, contact shadow | Rubber-like deformation, floating, excessive bounce |
| Gold and bronze accents | Small controlled highlight movement or rigid motion with their parent structure | Material edge, attachment point, restrained emphasis | Liquid-metal wobble, mirror-like streaking, independent drift |
| Cloth, foliage, banners, and organic detail | Soft follow-through and controlled asymmetry | Main silhouette and attachment point | Continuous agitation, high-frequency flutter, tangled silhouettes |
| Cards and crafted objects | Precise lift, tilt, slide, place, reveal, or settle with stable pivots | Identity, readable face, boundaries, layer order | Unmotivated spins, large elastic squash, text-distorting perspective |
| Elemental magic | Directional flow, local pulse, gathered energy, clear discharge and decay | Source, glyph, affected area, state meaning | Generic glow clouds, global color wash, effect without a source |
| Environmental ambience | Slow, sparse, subordinate loops | Composition, UI-safe areas, depth separation | Uniform motion across every layer, dense particles, false gameplay cues |

Structural and identity-bearing layers should move as rigid groups unless a subject-specific brief
defines an approved deformation. VFX may stretch and dissipate more freely, but must remain
visually attached to the event that caused it.

## Event Read

A complete effect communicates an event in a readable order. Use only the phases the event needs:

1. **Anticipation** identifies the source or pending action without implying that resolution has
   already happened.
2. **Action** shows release, movement, reveal, or transformation.
3. **Contact or confirmation** marks the affected target, value, zone, or state.
4. **Settle** removes temporary energy and leaves the authoritative final presentation.

Functional state changes are not held back for decorative anticipation. The visible confirmation
must agree with the resolved result, and temporary trails, flashes, particles, or displaced layers
must not survive after the event settles.

## Interaction and Transition Language

### Controls and Selection

- Pressed feedback is short, local, and directly attached to the activated control.
- Pointer hover may add polish but is never required to discover an action or understand its state.
- Focus and selection use a stable border, silhouette, symbol, or value cue; motion may reinforce
  the cue but may not replace it.
- Disabled and unavailable remain distinct from pressed, loading, locked, and selected.
- A state change may not resize the component's layout footprint or shift neighboring content.
- Repeated input must not queue decorative responses indefinitely.

### Navigation and Overlays

- Transitions preserve spatial continuity when that helps the player understand where content came
  from or where it went.
- Modal overlays establish their boundary and focus before secondary ornament animates.
- Required labels, actions, and error information become readable before decorative transition
  layers finish.
- Navigation animation is interruptible and settles into the newest correct destination.
- Full-screen fades and dissolves remain brief and do not conceal unexplained changes of state.

### Loading and Waiting

- Motion confirms that the application is responsive but does not imply progress that is not
  known.
- Determinate progress follows real progress data; indeterminate motion remains visibly distinct.
- A waiting loop uses restrained cadence and pauses when hidden, off-screen, or no longer relevant.
- Loading, success, warning, and error retain non-motion cues and code-native status text where
  required.

## Match and Card Feedback

Match effects must keep the board, card identities, rune costs, current values, legal targets, and
turn state readable throughout resolution.

| Event | Direction | Required final read |
|---|---|---|
| Playable card | Local emphasis connected to satisfied requirements | Card identity and playable state remain visible without motion |
| Card selection | Stable selection field or boundary with restrained lift | Selected card is distinct from focus and playability |
| Targeting | Clear source-to-target relationship and legal-target treatment | Source, legal targets, and rejected targets remain distinguishable |
| Card play | Deliberate movement from origin toward its resolved zone or action | The resulting zone and card lifecycle are unambiguous |
| Damage or healing | Short impact at the affected subject with readable value change | Current value and direction of change remain clear |
| Creature defeat or removal | Identity remains visible long enough to connect cause and outcome | Destination or removal state is understood without lingering clutter |
| Artifact activation | Source acknowledgement, effect release, and readiness change | Ready, delayed, used, and unaffordable remain distinct |
| Illegal action | Local rejection and understandable reason | No aggressive shake or flash is required to understand failure |
| Turn change | Clear change of active-player emphasis and available actions | Active player and current turn state remain continuously readable |

Effect magnitude follows gameplay consequence and presentation importance, not card rarity alone.
Routine actions use concise feedback so decisive actions and meaningful rewards retain headroom.
Particles, camera response, and glow do not substitute for values, labels, icons, boundaries, or
state surfaces.

## Rune Motion and State Effects

Fire, Air, and Forest are canonical gameplay identities. Their symbol and carrier treatment must
remain stable while animation communicates the rune's current state.

| State or event | Motion and VFX direction | Guardrail |
|---|---|---|
| Locked | Quiet, low-energy presentation with an unmistakable non-color lock cue | An opposing locked rune may not reveal its hidden type through color, particles, light, or motion |
| Unlock | Restrained lock acknowledgement, outward release, type reveal, then available-state energy | The rune identity does not redraw, morph, rotate, or arrive before the reveal is allowed |
| Available | Controlled inner energy and optional subtle aura pulse | Pulse affects effect layers, not the structural carrier or symbol geometry |
| Spend | Brief draw-down or transfer from rune to paying action, followed by immediate state confirmation | Complete payment remains one resolved action; effects may not imply a partial spend |
| Empty | Glow and active energy settle away while type identity remains readable where rules allow | Empty must not look locked, destroyed, or disabled by an error |
| Restore | Concise return of the active channel across eligible runes | Locked runes remain unchanged and are not visually included in the restoration |

The ten-position Rune Bar must remain readable as a sequence. Staggers may clarify ordered unlocks
or grouped restoration, but may not suggest a different rule order or make later positions appear
available early.

## Elemental VFX Language

Element effects share the same dimensional rendering, restrained bloom, local lighting, and
clean-edge discipline as the rest of Rune Mastery. The canonical symbol remains the primary
identity cue; motion and color support it.

| Affinity | Motion signature | Particle and light behavior | Avoid |
|---|---|---|---|
| Fire | Gathering heat, upward licking motion, decisive flare, ember decay | Warm local core, sparse embers, short-lived heat distortion where readable | Global orange cast, constant explosions, smoke that conceals cards or values |
| Air | Directed sweep, curved current, spiral release, light buoyant settle | Cool local channel, thin arcs or ribbons, sparse carried motes | Generic blue glow, opaque storm clouds, directionless noise |
| Forest | Branching growth, unfurling, rooted pulse, drifting natural settle | Local green life light, controlled leaf or seed accents, organic paths | Full-screen green wash, dense leaf storms, motion that resembles Air without a growth source |

Mixed-affinity and faction effects require their own authored identity. They may combine compatible
behaviors, but must not become two colors layered together or obscure which gameplay affinity paid
for an action. Faction motion extends the shared system and does not replace canonical rune cues.

## Primary Animation and VFX Reference

![Rune Mastery elemental animation and VFX reference](images/concept_reference/animation_vfx_overview_v001.png)

| Image | Purpose | Status |
|---|---|---|
| [`animation_vfx_overview_v001.png`](images/concept_reference/animation_vfx_overview_v001.png) | Evaluate shared material weight, effect-source clarity, directional flow, particle restraint, local elemental lighting, and controlled falloff across Fire, Air, and Forest | Concept reference |

The reference demonstrates three effect families on one stable limestone-and-bronze stage:

- Fire gathers from a readable source, rises into a concise flare, and breaks into sparse embers.
- Air follows an open directional spiral with thin translucent ribbons and a light particulate
  settle.
- Forest grows through a branching path with local life light, leaves, and seed-like accents.
- Structural carriers remain rigid and readable while the surrounding effect layers provide motion.
- Element light stays local; the environment preserves its neutral material and lighting character.

The neutral review backdrop is intentional. Environmental scenery is excluded so effect sources,
silhouettes, directional flow, particle density, contact shadows, and local light falloff can be
compared without unrelated visual competition.

The image establishes shared VFX character, not a simultaneous gameplay event or a mandatory
three-column composition. The blank carriers are presentation supports, not approved rune-carrier
geometry. The image does not define canonical glyphs, faction effects, exact particles, shaders,
timings, easing, layer packages, or runtime performance. Those require their own approved sources
and in-engine evidence.

## VFX Composition and Lighting

- Give every effect a visible source, affected area, and controlled falloff.
- Preserve silhouettes, glyph geometry, card boundaries, controls, and code-native text beneath
  the effect.
- Keep the brightest value and densest particles near the event that owns them.
- Let elemental light affect nearby surfaces locally without recoloring the entire scene.
- Use restrained bloom; the unbloomed core must remain readable.
- Keep foreground particles sparse enough that they do not create false targets or cover input
  regions.
- Separate depth layers deliberately. Background ambience stays behind gameplay information;
  target, impact, and confirmation effects remain attached to their subjects.
- Do not use persistent full-screen haze, vignette, blur, chromatic separation, or distortion as a
  default sign of magic.

Camera motion is optional supporting feedback. Avoid strong screen shake, rapid zoom, repeated
recoil, or parallax that changes the apparent location of interactive targets. Any camera response
must yield to readable selection, targeting, text, and touch interaction.

## Animation-Ready Construction

Identify every part that may move, rotate, scale, pulse, glow, fade, fill, unlock, break, or change
state before the asset family is produced.

### Layer Contract

- Keep independently controlled parts on separate transparent layers.
- Keep the immutable structural base separate from identity, state, glow, particles, highlights,
  shadows, and transition treatments.
- Preserve approved symbols and identity marks as unchanged layers; animate them as a whole only.
- Give aligned layers one canvas, coordinate system, pivot, scale, and naming convention.
- Reserve transparent padding for travel, rotation, pulse, bloom, and decay without clipping.
- Keep dynamic text, numbers, labels, costs, values, and localized copy code-native.
- Record the back-to-front layer order and default visibility for every assembled state.

A typical runtime stack is:

```text
contact shadow
structural base
content or material surface
canonical identity
product-semantic state
interaction, focus, selection, or targeting feedback
local glow and lighting
particles, trails, and impact accents
code-native full-screen transition or accessibility treatment
```

The exact stack is asset-specific. Optional effects must never be baked into an immutable base when
they need to pause, disappear, change state, or support a reduced-motion presentation.

## Timing, Easing, and Interruption

Exact durations, delays, travel distances, pulse amplitudes, and easing curves belong in the future
motion-token source and the owning component or effect specification. Until those values are
approved, use these semantic rules:

- Direct manipulation and functional acknowledgement feel immediate.
- Small UI state changes are concise and settle without overshoot.
- Heavy structural movement accelerates and settles with visible weight.
- Magical release may use soft anticipation and decay, while confirmation stays crisp.
- Celebration may breathe longer than functional feedback but remains skippable or non-blocking.
- Ambient loops are slow, phase-varied, and free of obvious synchronized repetition.

Navigation, ambience, and celebration are interruptible. An interruption resolves to one
deterministic visual state and leaves no partial layers, stale glow, displaced pivots, detached
particles, or ambiguous availability. Where many equivalent events occur together, combine or
stagger them within a bounded presentation instead of building an unbounded queue.

## Reduced Motion and Accessibility

Every motion-capable state has an understandable low-motion presentation even though a global
motion-reduction setting is not required for the first release.

- Replace large travel, rotation, stagger, parallax, shake, and repeated scale pulses with a short
  opacity or value transition.
- Preserve the identical final state, information order, and interaction result.
- Never encode identity, availability, focus, selection, warning, success, or error through motion
  or color alone.
- Avoid rapid flashing, repeated high-contrast luminance changes, and aggressive full-screen
  effects.
- Keep long reward, opening, and screen-transition sequences short, skippable, or non-blocking.
- Ensure the interface remains understandable when animation is minimal, interrupted, hidden by
  another surface, or missed entirely.
- Pause decorative loops when off-screen, covered, irrelevant, or likely to compete with an active
  decision.

## Runtime Budget and Degradation

Effect complexity must scale without changing gameplay meaning.

1. Preserve state surfaces, symbols, target relationships, and impact confirmation.
2. Preserve the primary local light or glow needed for the intended read.
3. Reduce secondary trails, particle counts, distortion, and residual duration.
4. Remove ambient and tertiary celebration layers first.

Cap simultaneous emitters and transparent overdraw in effect-heavy scenes. Pool repeatable runtime
effects where appropriate, stop hidden systems, and avoid large transparent layers whose visible
content occupies only a small area. Platform-specific implementations may simplify technique, but
their visible result must preserve hierarchy, identity, timing intent, and final state.

## Handoff Record

Each motion-capable asset or effect family records:

- purpose, owning gameplay event or presentation role, and stable identity;
- source, target, trigger, authoritative final state, and interruption behavior;
- supported states, variants, and required non-motion cues;
- canvas, content bounds, pivot, alpha, color space, and reserved padding;
- files, aligned layers, back-to-front order, default opacity, and animation groups;
- timing-token names, dependencies, concurrency priority, and loop conditions;
- particle, trail, light, distortion, and camera-response responsibilities;
- standard and reduced-motion recipes;
- import, filtering, mipmap, compression, and runtime resource expectations; and
- provenance, approval state, native-scale evidence, and remaining validation gates.

Approval of a visual direction and production readiness are separate. A motion-capable package is
not production-ready until its relevant static, motion, accessibility, technical, and in-engine
checks pass.

## Validation

Review motion in representative gameplay and feature contexts at the supported reference
viewports:

| Viewport | Review purpose |
|---|---|
| `1920x1080` | Desktop and browser design master |
| `1280x960` | `4:3` landscape-tablet validation |
| `1280x800` | `16:10` landscape-tablet validation |

For each applicable family:

1. Inspect every authoritative static state without animation.
2. Preview the full sequence at native game scale on representative backgrounds.
3. Confirm source, target, cause, result, and final state remain readable throughout.
4. Check pivots, anchors, baselines, masks, layer order, seams, padding, and clipping.
5. Test interruption, rapid repeated input, scene exit, hidden/off-screen behavior, and restoration
   of the correct final state.
6. Test multiple simultaneous effects and confirm that priority suppresses lower-value clutter.
7. Compare the standard and reduced-motion presentations for final-state equivalence.
8. Check meaning in grayscale and without glow, particles, or sound.
9. Confirm that touch targets and interactive content do not move unpredictably during feedback.
10. Record runtime evidence and any failed or unassessed gates beside the owning asset family.

## Review Checklist

Animation and VFX fit this direction when:

- functional state and causality read before spectacle;
- motion matches the weight and material of the subject;
- the effect has a clear source, target or affected area, and controlled falloff;
- canonical identities, card information, values, and component boundaries remain intact;
- state meaning does not rely on color, glow, particles, sound, or motion alone;
- higher-priority feedback remains clear during overlap;
- interruption leaves one correct and unambiguous final state;
- reduced motion preserves the same result without large travel or flashing;
- layers share stable canvases, pivots, scale, and documented order; and
- native-scale, representative-background, and in-engine checks support the claimed status.

Reject or revise a candidate when it obscures gameplay information, reveals hidden information,
introduces a conflicting motion language, depends on an effect to explain state, or succeeds only
as an isolated full-size preview.
