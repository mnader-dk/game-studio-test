# Framework

The `framework/` directory contains reusable rules, templates, schemas, and guides used by the game.

## Role

- Define the baseline game folder structure.
- Provide Markdown templates for human-reviewed game production documents.
- Provide image-generation workflow guidance for concept review.
- Explain the recommended order for building a project from concept to playable slice.

## Directory Layout

```text
framework/
  templates/  # human-readable Markdown templates
  guides/     # workflow guides
```

## Main Templates

| Template | Purpose |
|---|---|
| `game_concept.template.md` | Define the game concept |
| `game_design_principles.template.md` | Define game design principles |
| `game_design_document.template.md` | Draft the game design document |
| `art_sub_structure_readme.template.md` | Create the art sub-structure entry point |
| `art_direction.template.md` | Define art direction |
| `concept_brief.template.md` | Review concept images and art intent |
| `traceability_matrix.template.md` | Track design-to-implementation coverage |

## Image Generation Principles

`imagegen` is used to help people review art direction quickly. Generated images are references, not final production assets.

- Store generated images next to the category that uses them.
- Do not collect every image under a single central `art/images/` folder.
- Example paths: `art/gameplay_objects/images/modeling_reference/`, `art/characters/images/concept_reference/`.
- Do not expose raw image-generation prompts in user-facing review documents.
- Record the image, purpose, decision, and revision notes instead.

## Principles

1. Keep shared framework docs free of game-specific lore.
2. Store game-specific concepts, systems, art direction, versions, and validation under `game/`.
3. Treat Markdown as the primary human review format.