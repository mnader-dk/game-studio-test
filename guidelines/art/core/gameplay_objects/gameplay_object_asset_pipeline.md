# Gameplay Object Asset Pipeline


## Purpose

This document defines and inventories the visual gameplay objects required for Rune Mastery.

It organizes every stable asset responsibility into production kits and identifies the asset
families and gameplay objects owned by each kit. The inventory provides shared scope for later
kit briefs, production packages, manifests, and validation without prescribing an engine or
implementation technology.

Faction-specific identities, artwork, and production assets are out of scope. They belong to a
separate faction production pipeline.

## Sources

- Production strategy: `../production/art_production_strategy.md`
- Art concept: `../concepts/concept_brief.md` 
- Art direction: `../direction/art_direction.md`
- Environment concept: `../environment/environment_concept.md`
- Animation VFX direction: `../animation_vfx/animation_vfx_direction.md`
- Object concepts: `gameplay_object_concepts.md`

## References

- Art concept reference: `../concepts/images/concept_reference/concept_overview_v001.png`
- Gameplay objects reference: `../images/concept_reference/core_objects_v001.png`
- Environment reference: `../environment/images/concept_reference/environment_overview_v001.png`
- Animation VFX reference: `../animation_vfx/images/concept_reference/animation_vfx_overview_v001.png`

## Gameplay Object Kit Tree

```text
Rune Mastery Core Asset Kits
├── FOUNDATION-AND-BRAND-KIT
│   ├── Visual Foundation
│   │   └── STYLE-REFERENCE-RUNE-MASTERY
│   └── Brand Identity
│       └── BRAND-GAME-LOGO
├── UI-SYSTEM-KIT
│   ├── Buttons
│   │   ├── UI-BUTTON-FRAME-STANDARD
│   │   ├── UI-BUTTON-FRAME-COMPACT
│   │   ├── UI-BUTTON-FRAME-ICON-SQUARE
│   │   ├── UI-BUTTON-SURFACE-NEUTRAL
│   │   └── UI-BUTTON-INTERACTION-STATES
│   ├── Navigation
│   │   ├── UI-NAVIGATION-FRAME-OPEN-RAIL
│   │   ├── UI-NAVIGATION-OPEN-RAIL-STATES
│   │   ├── UI-ICON-META-NAVIGATION-FAMILY
│   │   └── HUD-META-NAVIGATION
│   ├── Action & Utility Icons
│   │   ├── UI-ICON-ACTION-CORE
│   │   └── UI-ICON-GLOBAL-UTILITY-FAMILY
│   ├── Player Identity
│   │   └── UI-PLAYER-IDENTITY-FAMILY
│   ├── Surfaces & Layout
│   │   ├── UI-SURFACE-PANEL-FAMILY
│   │   ├── UI-SURFACE-DIVIDER-FAMILY
│   │   ├── UI-COLLECTION-AND-SLOT-FAMILY
│   │   └── UI-DECORATION-FAMILY
│   ├── Inputs & Controls
│   │   ├── UI-INPUT-SURFACE-FAMILY
│   │   ├── UI-TOGGLE-AND-VALUE-CONTROL-FAMILY
│   │   └── UI-SCROLL-AND-OVERFLOW-FAMILY
│   ├── Feedback & Progress
│   │   ├── UI-PROGRESS-VISUAL-FAMILY
│   │   ├── UI-FEEDBACK-AND-OVERLAY-FAMILY
│   │   └── UI-PROGRESS
│   ├── Content Utilities
│   │   └── UI-SEARCH-FILTER
│   └── Screen-specific UI
│       ├── UI-STARTUP-INDICATOR-RUNE
│       ├── UI-SPLASH-STATUS-REGION
│       ├── UI-SPLASH-ERROR-FEEDBACK
│       ├── UI-HOME-CONTEXTUAL-PROMPT
│       └── UI-NOTIFICATION-FAMILY
├── RUNE-KIT
│   ├── Glyphs
│   │   ├── GLYPH-RUNE-FIRE
│   │   ├── GLYPH-RUNE-AIR
│   │   └── GLYPH-RUNE-FOREST
│   ├── Icons
│   │   ├── ICON-RUNE-FIRE
│   │   ├── ICON-RUNE-AIR
│   │   ├── ICON-RUNE-FOREST
│   │   ├── ICON-RUNE-AVAILABLE
│   │   ├── ICON-RUNE-EMPTY
│   │   └── ICON-RUNE-LOCKED
│   └── Runtime Carriers
│       ├── RUNE-CARRIER-ELEMENT-STATE-FAMILY
│       └── RUNE-CARRIER-RUNTIME-LAYERS
├── CARD-FRAME-KIT
│   ├── Type Frames
│   │   ├── CARD-FRAME-CREATURE
│   │   ├── CARD-FRAME-SPELL
│   │   └── CARD-FRAME-ARTIFACT
│   ├── Structure & Metadata
│   │   ├── CARD-BACK
│   │   ├── CARD-RARITY
│   │   ├── CARD-TYPE-AND-VALUE-ANCHORS
│   │   ├── CARD-RUNE-COST-PRESENTATION
│   │   └── CARD-METADATA-MARK-FAMILY
│   ├── States & Presentations
│   │   ├── CARD-STATE-OVERLAY-FAMILY
│   │   ├── CARD-PRESENTATION-COMPACT
│   │   └── CARD-PRESENTATION-BATTLEFIELD
│   └── Detail & Fallback
│       ├── UI-CARD-DETAIL
│       └── CARD-ART-MISSING-FALLBACK
├── CARD-CONTENT-KIT
│   └── Card-specific Content
│       ├── CARD-ILLUSTRATIONS
│       └── CARD-SCROLL-SYMBOLS
├── PROGRESSION-AND-REWARDS-KIT
│   ├── Resources & Rewards
│   │   ├── ICON-RUNE-DUST
│   │   ├── ICON-DRAGON-RELIC-MINOR
│   │   ├── ICON-DRAGON-RELIC
│   │   ├── ICON-DRAGON-RELIC-ANCIENT
│   │   ├── ICON-SCROLL
│   │   ├── ICON-SCROLL-FRAGMENT-SET-2
│   │   ├── ICON-SCROLL-FRAGMENT-SET-3
│   │   ├── ICON-SCROLL-FRAGMENT-SET-4
│   │   ├── ICON-SCROLL-READY
│   │   ├── ICON-CARD-CRAFTED
│   │   ├── ICON-CARD-RESERVED
│   │   ├── ICON-REWARD-CLAIMABLE
│   │   └── ICON-ACTIVITY-LOCKED
│   ├── Progression Objects
│   │   ├── OBJECT-DAILY-ALTAR
│   │   ├── ICON-RESTED-BONUS
│   │   └── ICON-LORE-UNLOCK
│   └── UI Components
│       ├── UI-RESOURCE-DISPLAY-FAMILY
│       ├── UI-REWARD-TILE
│       └── UI-ACTIVITY-TILE
├── MATCH-AND-HUD-KIT
│   ├── Decks
│   │   ├── ICON-DECK-DRAFT
│   │   └── ICON-DECK-READY
│   ├── Game Modes
│   │   ├── ICON-GAME-MODE-CASUAL
│   │   ├── ICON-GAME-MODE-AI
│   │   ├── ICON-GAME-MODE-RANKED
│   │   └── ICON-GAME-MODE-ADVENTURE
│   ├── Match Formats & Outcomes
│   │   ├── ICON-MATCH-AI
│   │   ├── ICON-MATCH-PVP
│   │   ├── ICON-MATCH-EVENT
│   │   └── MATCH-OUTCOME-PRESENTATION-FAMILY
│   ├── Selection UI
│   │   ├── UI-DECK-TILE
│   │   ├── UI-GAME-MODE-TILE
│   │   └── UI-MATCH-FORMAT-TILE
│   └── Match HUD
│       ├── HUD-TOP-STATUS
│       ├── HUD-MATCH
│       ├── HUD-RUNE-BAR
│       ├── HUD-CARD-ZONES
│       ├── HUD-PLAYER-STATUS
│       └── HUD-CONNECTION
├── SOCIAL-AND-ACCOUNT-KIT
│   ├── Online & Social UI
│   │   ├── UI-MATCHMAKING-STATUS
│   │   ├── UI-MATCH-INVITATION
│   │   ├── UI-FRIEND-ENTRY
│   │   ├── UI-PRESENCE-STATUS
│   │   ├── UI-MESSAGE-ENTRY
│   │   └── UI-LEADERBOARD-ENTRY
│   └── Account & Social Scenes
│       ├── SCENE-ACCOUNT
│       ├── SCENE-MATCHMAKING
│       ├── SCENE-SOCIAL
│       ├── SCENE-MESSAGES
│       └── SCENE-LEADERBOARDS
├── LORE-AND-ARCHIVE-KIT
│   ├── Lore Objects
│   │   └── LORE-WORLD-DISC-ILLUSTRATION
│   ├── Lore Views
│   │   ├── UI-LORE-ENTRY
│   │   ├── UI-LORE-DETAIL
│   │   └── UI-WORLD-TIMELINE
│   └── Lore Scenes
│       ├── SCENE-CHRONICLES
│       └── SCENE-ARCHIVE
├── GAMEPLAY-VFX-KIT
│   ├── Rune Feedback
│   │   ├── FX-RUNE-UNLOCK
│   │   ├── FX-RUNE-SPEND
│   │   └── FX-RUNE-RESTORE
│   ├── Card Feedback
│   │   ├── FX-CARD-SELECT
│   │   ├── FX-TARGETING
│   │   ├── FX-CARD-PLAY
│   │   └── FX-CARD-ZONE-TRANSFER-FAMILY
│   ├── Combat Feedback
│   │   ├── FX-CREATURE-ATTACK
│   │   ├── FX-CREATURE-BLOCK
│   │   ├── FX-DAMAGE-AND-HEAL
│   │   └── FX-CREATURE-DEFEAT
│   ├── Artifact Feedback
│   │   └── FX-ARTIFACT-ACTIVATION
│   └── Match Feedback
│       ├── FX-ILLEGAL-ACTION
│       └── FX-TURN-CHANGE
├── SCENE-PRESENTATION-KIT
│   ├── Splash Presentation
│   │   ├── SCENE-SPLASH
│   │   ├── BG-SPLASH-RUNE-MASTERY
│   │   └── SCENE-SPLASH-COMPOSITION
│   ├── Feature Scenes
│   │   ├── SCENE-LOGIN
│   │   ├── SCENE-ASSET-LOADING
│   │   ├── SCENE-HOME
│   │   ├── SCENE-FIRST-AI-DUEL-ENTRY
│   │   ├── SCENE-MATCH
│   │   ├── SCENE-POST-MATCH
│   │   ├── SCENE-DUEL
│   │   ├── SCENE-FORGE
│   │   └── SCENE-SHRINE
│   ├── Utility Scenes
│   │   ├── SCENE-SETTINGS
│   │   └── SCENE-HELP-GUIDE
│   └── Backgrounds & Transitions
│       ├── FX-SCREEN-TRANSITION
│       ├── FX-SPLASH-AMBIENT
│       └── FEATURE-BACKGROUNDS
├── COSMETICS-KIT
│   ├── Card Cosmetics
│   │   ├── COSMETIC-CARD-BACK-FAMILY
│   │   └── COSMETIC-CARD-VARIANT-FAMILY
│   ├── Player Cosmetics
│   │   ├── COSMETIC-PLAYER-AVATAR-FAMILY
│   │   ├── COSMETIC-PLAYER-FRAME-FAMILY
│   │   └── COSMETIC-PLAYER-TITLE-FAMILY
│   └── Board Cosmetics
│       └── COSMETIC-BOARD-FAMILY
└── LIVE-CONTENT-KIT
    ├── Editions
    │   ├── EDITION-MARK-FAMILY
    │   └── EDITION-KEY-ART-FAMILY
    └── Themes
        ├── EVENT-THEME-PACKAGE
        └── SEASON-THEME-PACKAGE
```
