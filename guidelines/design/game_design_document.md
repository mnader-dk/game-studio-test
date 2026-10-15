# Game Design Document

## Purpose and Authority

This document is a concise overview and navigation layer for Rune Mastery. It does not redefine or
duplicate detailed game rules.

The single source of truth for player-facing behavior is the authoritative
[Rune Mastery Game Design](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/README.md)
workspace. Each detailed rule belongs only in its owning specification there. If this overview and
an owning specification differ, the owning specification takes precedence.

The product concept and decision principles for work in this repository are summarized in:

- [Game Concept](game_concept.md)
- [Game Design Principles](game_design_principles.md)

## Overview

Rune Mastery is a digital fantasy strategy card game built around one-versus-one matches,
faction-aligned deck construction, elemental rune management, and persistent collection growth.
Players prepare a deck, make card and board decisions during a match, understand the outcome, and
choose how to continue progressing afterward.

Product vision, audience, design pillars, supported platforms, and pacing are owned by
[Game Vision](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/00_Vision/Game_Vision.md),
[Design Pillars](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/00_Vision/Design_Pillars.md),
[Target Audience](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/00_Vision/Target_Audience.md),
and [Platforms](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/00_Vision/Platforms.md).

## Controls

Supported input methods, interaction requirements, touch targets, and hover behavior are defined in
[Input](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/90_CrossCutting/Input.md).
Supported layouts and reference sizes are defined in
[Supported Viewports](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/90_CrossCutting/Supported_Viewports.md).

Features must follow those specifications rather than maintaining separate input or viewport rules
in this document.

## Core Loop

At the highest level, the player chooses an activity and deck, enters a match, makes card, rune,
board, and combat decisions, understands the result and rewards, and then adjusts the deck or
chooses the next activity.

The authoritative loop, mode variations, and post-match behavior are defined in
[Core Loop](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/10_CoreExperience/Core_Loop.md).
Long-term progression is defined in
[Meta Loop](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/10_CoreExperience/Meta_Loop.md).

## Player Goals

| Goal | Type | Authority |
|---|---|---|
| Complete and understand matches | Primary | [Match](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Match/Epic_Match.md) and [Match Formats](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/MatchFormats/Epic_MatchFormats.md) |
| Build and select a valid deck | Preparation | [Decks](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Decks/Epic_Decks.md) and [Runes](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Runes/Epic_Runes.md) |
| Make meaningful card and combat decisions | Mastery | [Cards](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Cards/Epic_Cards.md), [Card Abilities](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/CardAbilities/Epic_CardAbilities.md), and [Combat](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Combat/Epic_Combat.md) |
| Grow the collection and craft cards | Long-term | [Shrine](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/20_Features/Shrine/Epic_Shrine.md), [Rune Dust](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/RuneDust/Epic_RuneDust.md), and [Rewards](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/Rewards/Epic_Rewards.md) |
| Follow activities and events | Supporting | [Chronicles](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/20_Features/Chronicles/Epic_Chronicles.md) and [Live Operations](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/80_LiveOperations/README.md) |
| Explore cards, factions, and lore | Supporting | [Archive](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/20_Features/Archive/Epic_Archive.md) and [World and Content](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/70_WorldAndContent/README.md) |

## System Map

| Area | Responsibility | Source of truth |
|---|---|---|
| Core experience | Player loop, meta loop, journey, and navigation | [Core Experience](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/10_CoreExperience/README.md) |
| Feature experiences | Home, Duel, Forge, Shrine, Chronicles, Archive, Login, Splash, and Asset Loading | [Features](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/20_Features/README.md) |
| Match | Participants, match lifecycle, outcomes, surrender, and recovery | [Match](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Match/Epic_Match.md) |
| Match configuration | Participants, conditions, restrictions, availability, and rewards | [Match Formats](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/MatchFormats/Epic_MatchFormats.md) |
| Turns | Phase order, legal timing, and automatic steps | [Turns](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Turns/Epic_Turns.md) |
| Cards and abilities | Card types, lifecycle, properties, targeting, effects, and resolution | [Cards](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Cards/Epic_Cards.md) and [Card Abilities](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/CardAbilities/Epic_CardAbilities.md) |
| Board and combat | Zones, public information, card movement, attacks, damage, and death | [Board](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Board/Epic_Board.md) and [Combat](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Combat/Epic_Combat.md) |
| Decks and runes | Deck validity, card copies, Rune Bar configuration, unlocking, and spending | [Decks](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Decks/Epic_Decks.md) and [Runes](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Runes/Epic_Runes.md) |
| Modes and matchmaking | Selectable play contexts and human opponent matching | [Game Modes](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/50_GameModes/README.md) and [Matchmaking](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/60_OnlineAndSocial/Matchmaking/Epic_Matchmaking.md) |
| Progression and economy | Rewards, Rune Dust, crafting, balancing, and collection growth | [Progression and Economy](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/README.md) |
| World and content | Factions, editions, lore, characters, places, and authored content | [World and Content](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/70_WorldAndContent/README.md) |
| Live content | Events, seasons, notifications, and ongoing operations | [Live Operations](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/80_LiveOperations/README.md) |
| Cross-cutting rules | Accessibility, localization, input, UI states, and supported viewports | [Cross-Cutting Requirements](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/90_CrossCutting/README.md) |

## First Session

The first-session sequence, starter-deck context, early feature availability, and returning-player
behavior are owned by
[Player Journey](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/10_CoreExperience/Player_Journey.md).
Individual screen behavior belongs to the corresponding feature epic under
[Features](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/20_Features/README.md).

This document intentionally does not repeat the sequence or its unlock rules.

## Win / Fail Conditions

Match victory, defeat, draw, surrender, and connection-loss outcomes are defined by
[Match](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Match/Epic_Match.md)
and configured through
[Match Formats](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/MatchFormats/Epic_MatchFormats.md).

Action legality and failure reasons are owned by the relevant system specification:

- card play and targeting: [Cards](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Cards/Epic_Cards.md);
- rune payment: [Runes](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Runes/Epic_Runes.md);
- turn timing: [Turns](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Turns/Epic_Turns.md);
- combat: [Combat](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Combat/Epic_Combat.md); and
- deck eligibility: [Decks](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/30_GameplaySystems/Decks/Epic_Decks.md).

## Configuration and Balance

Format-specific values belong to the active Match Format. Economy values and tuning belong to
[Rune Dust](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/RuneDust/Epic_RuneDust.md),
[Rewards](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/Rewards/Epic_Rewards.md),
and [Balancing](/Users/mnader/Documents/MyGitFolder/BattleRunes/GameDesign/40_ProgressionAndEconomy/Balancing/Epic_Balancing.md).

Numbers, limits, formulas, timers, and reward tables are intentionally not copied into this
overview.

## Validation Questions

- Can a player understand the immediate goal and next meaningful action?
- Does each feature support the core match and progression experience described by the concept?
- Is every detailed rule defined in exactly one owning Game Design specification?
- Does each feature link to its dependencies instead of restating shared rules?
- Are format-specific and balance-specific values read from their owning configuration or design
  authority?
- Are failures and unavailable actions understandable from the player's point of view?
- Do input, accessibility, localization, and viewport behavior follow the cross-cutting authorities?

## Maintenance Rule

When a detailed rule changes, update only its owning Game Design specification. Update this document
only when the high-level overview, system ownership, or navigation paths change.
