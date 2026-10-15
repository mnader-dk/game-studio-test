# Game Concept

## Working Title

Rune Mastery

## One-Line Pitch

Rune Mastery is a fantasy strategy card game in which players build faction-aligned decks, master
Fire, Air, and Forest runes, and use Creatures, Spells, and Artifacts to outplay an AI or human
opponent while expanding their card knowledge and collection.

## Player Fantasy

The player becomes a Rune Master: a knowledgeable deck builder and battlefield tactician who
channels elemental runes, commands cards from distinct magical factions, and turns discovered
knowledge into new strategic possibilities.

The experience should make the player feel that they are:

- assembling a deliberate deck rather than collecting disconnected cards;
- reading the battlefield and making clear, consequential decisions;
- combining rune affinities, faction identity, and card effects into a personal strategy;
- growing their knowledge and collection through play; and
- returning from each duel with visible progress and a meaningful next choice.

## Target Experience

| Topic | Decision |
|---|---|
| Genre | Digital fantasy strategy card game with deck construction, collection progression, and one-versus-one duels |
| Camera / perspective | Screen-based card-board presentation with a dedicated Match HUD and separate meta-game screens |
| Session length | TBD; the first-session and match flows are defined, but no target duration is established |
| Main input style | Pointer, keyboard, and controller input with explicit focus states and responsive landscape layouts |
| Primary emotion | Deliberate mastery: understanding the available systems, forming a plan, and outplaying the opponent |

## Core Promise

Rune Mastery gives players readable, strategically meaningful card duels in which elemental rune
costs, card types, factions, and battlefield states remain clear at a glance. Every match should
connect to persistent growth without obscuring the decisions that define play.

## Core Experience

The primary play experience follows this rhythm:

1. Return to Home and choose the next activity.
2. Select a valid deck and a supported Match Format.
3. Enter a one-versus-one duel against an AI or human opponent.
4. Use available runes to play Creatures, Spells, and Artifacts.
5. Read and respond to turn state, card costs, legal actions, targets, battlefield values, and
   Artifact readiness.
6. Resolve the match and review the outcome, rewards, and progression.
7. Improve decks, complete card knowledge, craft cards, or explore the collection before playing
   again.

The current mode scope covers Casual and AI play. Ranked and Adventure are later possibilities and
are not part of the current concept scope.

## Cards and Runes

Fire, Air, and Forest are the three canonical rune affinities. Cards use exact rune costs, which
may be zero, single-affinity, or mixed-affinity.

Every card has a stable identity consisting of a name, description, rune cost, card type, rarity,
faction, edition, and artwork. The three card types define their core battlefield role:

| Card type | Conceptual role |
|---|---|
| Creature | A battlefield card with Strength and current Health; it may have one effect or no effect |
| Spell | A non-persistent card with exactly one effect |
| Artifact | A persistent object with one passive or activated effect; activated Artifacts may have their own rune cost and readiness state |

Card rarity uses the tiers Common, Rare, Epic, and Legendary. Rarity identifies content tier but
does not by itself imply gameplay strength.

## Factions

Rune affinity and faction identity are related but distinct. Runes describe elemental traditions;
factions describe culture, values, history, and authored content. The six established factions are:

| Faction | Rune affinity | Concept identity |
|---|---|---|
| Ancientflame | Fire | A severe, hierarchical mage cult pursuing conquest, forbidden knowledge, sacrifice, destructive purification, and rebirth through flame |
| Stormspears | Air | Honorable paladin-artificers shaped by discipline, precision, guarded invention, storms, and powerful but temporary rune technology |
| Circle of Prophecy | Forest | A reclusive druidic circle centered on harmony, prophecy, spirituality, healing, protection, ancient memory, and nature's wrath when balance is threatened |
| Dragon Sisterhood | Fire and Forest | A mystical and military dragon order combining destructive flame with growth, renewal, living sanctuaries, discipline, dominance, and rebirth |
| Flamebound | Fire and Air | A religious and military paladin-sorcerer order combining controlled destruction, storms, ancient artifacts, faith, judgment, and disciplined authority |
| Storm Circle | Air and Forest | A druidic artisan order combining storms, regeneration, natural craftsmanship, cooperation, adaptation, and balance between creation and destruction |

Dual-affinity factions are independent cultures rather than alliances or simple combinations of two
starting factions.

## Meta-Game Structure

| Area | Player purpose |
|---|---|
| Home | Re-enter the game, see relevant status and recommendations, and choose the next activity |
| Duel | Select a supported Match Format and a valid deck |
| Forge | Construct decks, inspect card-copy availability, and validate deck readiness |
| Shrine | Complete Scroll knowledge and craft cards through deliberate player actions |
| Chronicles | Follow activities, daily tasks, events, progress, and rewards |
| Archive | Browse cards and lore through search, filters, collection views, and details |

Home provides the persistent meta-game shell. The active match replaces it with a dedicated
gameplay HUD centered on the board, player and opponent status, hand and card zones, Rune Bar,
available actions, turn state, and match feedback.

## Progression and Collection

Progression is based on collection growth, card knowledge, crafting readiness, and earned rewards.
Its established objects are:

- **Rune Dust:** the currently defined spendable player resource.
- **Dragon Relics:** reward containers that grant Rune Dust only; they are not a second currency or
  random card packs.
- **Complete Scrolls:** permanent knowledge progress tied to one specific card. Receiving a Scroll
  does not automatically grant or craft that card.
- **Scroll Fragments:** numbered pieces tied to one specific card and its Complete Scroll.
- **Completed Scroll knowledge:** permanent card knowledge finalized through a deliberate Shrine
  action; it is not consumed when the related card is crafted.

Progress and reward states distinguish in-progress, claimable, claimed, completed, missing,
upcoming, and expired content. Completing an objective and claiming its reward are separate player
actions where both states apply.

## First-Session Experience

The intended first-session path is:

```text
Splash
  -> Login when authentication is required
  -> Asset Loading
  -> Home: First Arrival
  -> First AI Duel handoff with a selected starter deck
  -> Match
  -> Post-Match result, reward, and progress summary
  -> Home: Return State
  -> optional Chronicles, daily altar, Shrine, or Forge prompts
```

The first playable duel should be reachable without forcing the player through Shrine or Forge.
After the match, the player returns to the same Home structure with updated rewards, progress, and
next-step opportunities.

## Reference Boundaries

The concept draws on genre-level patterns from digital strategy card games:

- deck construction and one-versus-one card duels;
- elemental costs and faction-aligned card identities;
- persistent collection and knowledge progression;
- crafting and deck-readiness workflows; and
- optional activities, events, and time-limited reward contexts around a stable core game.

Specific balance values, deck rules, turn timing, combat resolution, victory conditions, target
session duration, economy quantities, and final narrative relationships require their own design
documents. Visual presentation must support these rules but must not invent or redefine them.
