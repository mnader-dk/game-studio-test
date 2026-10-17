---
title: Asset Brief Template
summary: Essential visual and technical requirements for one asset family.
---

# Asset Brief

## Purpose

Define the visual form, required variants, runtime outputs, and technical construction of one asset
family. Use exact values or `Not Applicable — <reason>`.

## Definition

| Field | Requirement |
|---|---|
| Asset ID and family | `<stable ID and name>` |
| Role and player-facing outcome | `<responsibility and what must be understood or felt>` |
| Target contexts | `<screens, scenes, viewports, backgrounds, camera, and neighboring content>` |
| Scope | `<included assets, states, variants, and explicit exclusions>` |
| Dependencies | `<required assets, systems, or specifications>` |

## Deliverables

| Asset or group | Required states or variants | Source master | Runtime outputs |
|---|---|---|---|
| `<asset>` | `<set>` | `<dimensions, format, and layers>` | `<sizes, formats, and variants>` |

## Visual Contract

| Field | Requirement |
|---|---|
| Shape and readability | `<silhouette, proportions, focal detail, and smallest-size read>` |
| Color, material, and lighting | `<palette roles, surfaces, light direction, and contrast>` |
| View and composition | `<camera, facing, framing, safe regions, and responsive behavior>` |
| Fixed elements | `<symbols, geometry, proportions, or details that may not change>` |
| Avoid | `<style drift, misleading meaning, and baked-in dynamic content>` |

## Technical Contract

| Field | Requirement |
|---|---|
| Canvas and layout | `<dimensions, bounds, safe area, padding, grid, pivot, anchor, and orientation>` |
| Files and rendering | `<formats, bit depth, color space, alpha, masks, filtering, mipmaps, and compression>` |
| Scaling and assembly | `<uniform scale, crop, slicing, tiling, layers, and assembly order>` |
| Motion and accessibility | `<animation groups, interruption result, reduced motion, contrast, and non-color cues>` |
| Platforms and performance | `<runtime targets and texture, geometry, material, particle, memory, or overdraw limits>` |

## States and Events

Use this table only when the family has visual states, variants, or events.

| State or event | Meaning | Required presentation and non-color cue | Motion or VFX | Final and reduced-motion result |
|---|---|---|---|---|
| `<name>` | `<player-facing meaning>` | `<construction, shape, value, symbol, or label>` | `<behavior or none>` | `<deterministic result>` |
