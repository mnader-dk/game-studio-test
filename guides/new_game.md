# New Game Guide

Use this guide when starting a new game under `game/`.


## 1. Create the Folder Structure

```text
game/
  README.md
  design/
  systems/
  art/
    README.md
    direction/
    concepts/
    characters/
    gameplay_objects/
    environment/
    animation_vfx/
    production/
    reviews/
    work_items/
  ux/
  qa/
  production/
  slices/
  versions/
  work_items/
  project_memory/
```

## 2. Start With Game Design

Create these documents first:

- `design/game_concept.md`
- `design/game_design_principles.md`
- `design/game_design_document.md`
- `systems/core_loop.system.md`

Do not start from isolated assets. Start from the game promise, player goal, core loop, and version target.

## 3. Add the Art Sub-Structure

The game art folder should explain how art direction, concept references, modeling references, and asset briefs are managed.

Recommended image stages:

| Stage | Purpose |
|---|---|
| `concept_reference` | Visual direction and concept review |
| `modeling_reference` | Orthographic or part-focused references for 3D modeling |
| `production_reference` | Finalized production reference images |
| `legacy` | Old references kept for history only |
| `superseded_reference` | Rejected or replaced references |

## 4. Keep Project Memory Updated

The `game_memory/` folder should summarize decisions so future agents do not need to reconstruct the project from chat history.