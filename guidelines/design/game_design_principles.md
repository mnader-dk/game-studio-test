# Game Design Principles

## Purpose

This document defines the design rules that guide every Rune Mastery feature decision. The
principles protect the game's promise of readable strategic duels, deliberate player agency, and
meaningful collection growth.

## Principles

| Principle | Meaning | Production Test |
|---|---|---|
| Make the next decision readable | Players should understand the current state, available actions, costs, targets, restrictions, and likely consequences before committing. Gameplay clarity takes priority over ornament, spectacle, and information density. | Can a player identify what they may do, why an action is unavailable, and what changed without guessing or opening an unrelated screen? |
| Create depth through combinations, not rule clutter | Strategic depth should emerge from rune costs, the three card types, faction relationships, deck composition, timing, and battlefield interaction. Individual cards stay focused: a Creature has at most one effect, while a Spell or Artifact has exactly one effect; cards have no gameplay subtypes. | Does the feature create new decisions through interaction with established systems rather than by adding another exception, subtype, resource, or effect channel? |
| Keep player actions deliberate | Important progression actions remain explicit. Completing Scroll knowledge, crafting a card, claiming a reward, selecting a deck, and starting a duel are distinct decisions and must not silently trigger one another. | Can the player predict and confirm the exact permanent result before resources, rewards, or collection state change? |
| Keep the duel at the center | Home, Forge, Shrine, Chronicles, Archive, rewards, and collection systems should prepare for play, explain progress, or give the player a meaningful reason to return. They must not bury the one-versus-one card duel beneath mandatory administration. | Does the feature strengthen preparation, play, understanding, or post-match motivation without adding an unnecessary barrier before the next duel? |
| Preserve distinct meanings | Rune affinity, faction, card type, rarity, edition, ownership, readiness, and interaction state are separate concepts. One must not be used as a substitute for another, and temporary context must not overwrite permanent identity. | Can each relevant property still be understood independently when color, animation, event theming, or decorative treatment is removed? |
| Design accessibility into the rules | Meaning must never depend on color, motion, pointer hover, or decorative imagery alone. All required actions and states need clear text, symbols, structure, or equivalent cues and must support pointer, keyboard, and controller interaction. | Can the player understand and operate the feature without relying on one sensory cue or one input method? |
| Let progression support mastery | Progression should communicate knowledge, readiness, ownership, and earned rewards without disguising what the player receives. Rune Dust is the spendable resource; Dragon Relics grant Rune Dust; Scrolls and fragments represent card-specific knowledge rather than cards or random packs. | Does the reward state exactly what was earned, what remains incomplete, and which deliberate action is available next? |
| Keep the core stable and extend it additively | Events, seasons, editions, and future modes may add content and context, but they must not redefine permanent rules, controls, identities, or state meanings. The base game remains complete when temporary content is absent. | If the temporary layer expires or fails to load, is the underlying feature still understandable, playable, and consistent? |

## Supporting Rules

### First-session focus

- The player reaches the first AI duel through a short, understandable path.
- Shrine and Forge may be introduced after the match but are not mandatory before it.
- Post-Match summarizes the outcome, essential rewards, and progress, then provides one clear return
  to Home.
- Contextual guidance is optional, dismissible, and sequenced so several prompts do not compete.

### Honest progression

- Completed and Claimed are different states.
- Receiving a Complete Scroll does not grant or craft its related card.
- Completing Scroll knowledge is a deliberate Shrine action and the knowledge remains after
  crafting.
- Dragon Relic tiers communicate increasing reward value without presenting lower tiers as broken,
  defective, or worthless.
- Rarity identifies a card tier but does not promise greater gameplay strength.

### Focused scope

- Casual and AI play define the current mode scope.
- Ranked and Adventure remain outside the current scope until the core experience supports them.
- New currencies, card types, card subtypes, progression objects, or Match Formats require an
  explicit game-design need; presentation alone is not sufficient justification.

## Non-Goals

- Maximizing the number of mechanics, currencies, modes, or card classifications.
- Using hidden information, ambiguous feedback, or decorative complexity as a substitute for
  strategic depth.
- Forcing collection management, crafting, or reward chores before the player can reach the first
  duel.
- Treating rarity, faction, affinity, or visual intensity as an automatic measure of gameplay power.
- Allowing events or seasonal content to alter the permanent interaction model or obscure core
  state information.
- Inventing balance values, combat rules, victory conditions, or economy quantities without their
  owning design specification.

## Decision Rule

When two options conflict, choose the option that creates the clearest meaningful player decision
while preserving deliberate agency and the shortest coherent path back to the core duel.

Resolve priorities in this order:

1. Gameplay state, safety, and accessibility.
2. Player agency and predictable outcomes.
3. Strategic depth and interaction with established systems.
4. Persistent identity, progression, and collection meaning.
5. Theme, celebration, and decorative novelty.

If an option only improves a lower priority by weakening a higher one, reject it.
