---
name: floral-art-director
description: Use when a user provides a reference image — album cover, painting, movie still, photograph, illustration, or personal image — and wants its visual language translated into a professional, manufacturable floral artwork, delivered as a full design presentation package plus a realistic bouquet visualization.
---

# Floral Art Director

## Overview
An AI floral design system that translates visual references into **professional, manufacturable floral artworks**.

**The bouquet must first exist as a real floral artwork, and then resemble the reference image.**

## When to Use
Use for album covers, paintings, film stills, photographs, illustrations, or personal images when the user wants a professional floral artwork derived from the image's mood, palette, light, texture, or composition.

Do not use this skill merely to identify flowers already visible in an image, or to copy literal objects from the reference into a bouquet.

## Core Workflow — Floral Design Studio

```text
Reference Image
    ↓
Visual Language Analysis
    ↓
Floral Translation
    ↓
Professional Floral Design
    ↓
Presentation Package
    ↓
Real Bouquet Visualization
```

### 1. Visual Language Analysis
Analyze the reference as a design language, not as a checklist:
- color structure: main colors, supporting colors, accent colors
- brightness, saturation, and warm/cool balance
- light and shadow behavior
- texture and material qualities
- composition and visual center
- rhythm and density
- emotional atmosphere and theme

When useful, provide approximate HEX values, but treat them as visual guides rather than measurement claims.

### 2. Floral Translation
Map image language into floral language. Every translation must pass through a **design-language step** before it reaches flowers:

| Image feature | Design language | Floral language |
|---|---|---|
| Dominant color | Spatial atmosphere | Dark wrapping and foliage |
| Accent / highlight | Energy points | Focal or accent flowers |
| Strong directional lines | Line rhythm | Delphinium, snapdragon, branches, grasses |
| Soft haze | Depth and softness | Gypsophila, limonium, fine foliage, translucent layers |
| Dense visual mass | Body and weight | Clustered focal and mass flowers |
| Negative space | Open composition | Asymmetrical structure, restrained filler |
| Gloss / water / glass | Transparency | Clear film, organza, translucent wrapping |
| Grain / rough texture | Tactile contrast | Seed heads, berries, dried texture, foliage contrast |

Do not reproduce the image literally — preserve its visual logic. A blue sky is not "blue flowers"; it is *spatial atmosphere*, expressed through blue wrapping and blue/purple flowers.

### 3. Style DNA
Summarize the reference in 4–7 concise keywords describing atmosphere, color behavior, structure, emotion, and material quality.

Examples: `Aquatic · Mint · Translucent · Floating · Serene · Sunlit`.

### 4. Floral Design Concept
Describe the intended bouquet before any flower is chosen:
- bouquet name
- design philosophy
- bouquet structure (silhouette, density, size)
- emotional expression

If the user gives no budget, recipient, or size, assume a medium-budget, medium-size gift bouquet.

### 5. Floral Reality Check
**Mandatory step.** Run before writing any BOM item. Complete all four checks in the dedicated [Floral Reality Check](#floral-reality-check) chapter: Color Feasibility, Material Translation, Seasonal Availability, Construction Feasibility.

### 6. Flower BOM
The BOM is the source of truth for real construction and procurement, and must be independent from any rendered image.

For every floral material include:
- flower/material name
- color
- exact stem count or quantity
- floral role
- **flower status** — exactly one of: `natural` · `dyed` · `preserved` · `decorative material`
- substitute if seasonal or difficult to source

Every BOM item must be quantified. "Some flowers" is not a BOM.

Also list wrapping and auxiliary materials with quantities.

### 7. Structural Sketch
Describe the bouquet's structure so it can be built:
- flower position (focal, supporting, line, filler)
- height hierarchy
- focal flower
- supporting flowers
- line flowers
- wrapping

### 8. Alternative Views
Describe at least three distinct views for the visualization stage:
- front view
- side view
- detail view (e.g. a close focal flower, the binding point, or a wrapping fold)

## Required Output — Floral Design Presentation Package

The default output is a complete presentation package in two levels. **LEVEL 1 is the design proposal; LEVEL 2 is the final commercial bouquet visualization.**

### LEVEL 1 — Floral Design Board

Generate a complete design-proposal poster. It contains eight parts:

#### 1. Reference Analysis
Cover: color structure · main colors · supporting colors · accent colors · light and shadow · texture · composition · emotional atmosphere.

#### 2. Style DNA
4–7 keywords, formatted as:

```text
Style DNA:
- keyword 1
- keyword 2
- keyword 3
```

#### 3. Visual Translation Logic
Explain every major translation as `visual element → design language → floral language`:

```text
Dark night sky
↓
Deep spatial background
↓
Dark wrapping and foliage

Golden stars
↓
Energy points
↓
Yellow focal flowers
```

#### 4. Floral Design Concept
- Bouquet name
- Design philosophy
- Bouquet structure
- Emotional expression

#### 5. Floral Reality Check
Answer all four questions:
- **Color Feasibility** — can this color be achieved with real flower material?
- **Material Translation** — where a color or effect cannot be achieved by flowers, state the exact channel: `wrapping`, `foliage`, `lighting`, or `accessory`.
- **Seasonal Availability** — list the seasonal flowers and their substitutes.
- **Construction Feasibility** — bouquet size, structure, manufacturability.

#### 6. Flower BOM
Procurement-level material table:

`|Flower/Material|Quantity|Color|Role|Status|`

- every flower has an exact quantity
- no "some flowers"
- no invented flowers
- dyed material is marked `dyed flower`

#### 7. Structural Sketch
Flower position · height hierarchy · focal flower · supporting flowers · line flowers · wrapping.

#### 8. Alternative Views
At least three angles: front view · side view · detail view.

### LEVEL 2 — Final Bouquet Visualization

Generate the final commercial bouquet as a standalone image, separate from the design board.

**Requirements:**
- must look like real flower-shop product photography
- realistic flower texture, natural petals, physically possible bouquet

**Forbidden in this image:** text · infographic · tables · labels · diagrams · color palettes.

**Only show:** bouquet · flowers · wrapping · realistic lighting.

**Photography style:** professional floral photography, luxury florist catalog style.

## Floral Reality Check

The system does not only generate beautiful images — it evaluates whether the bouquet can exist in reality. No BOM item may be written until all four checks pass.

### 1. Color Feasibility
For every color that matters in the design, classify it as exactly one of:
- **natural flower color** — a color that exists naturally in a real flower variety (use it directly)
- **approximate color** — no exact match exists; use the closest natural variety and carry the remainder through material (foliage, wrapping, ribbon, translucent film, decoration)
- **dyed flower required** — the hue has no acceptable natural approximation and is essential to the design; then, and only then, specify a real flower variety to be dyed and label it `dyed flower`

**Forbidden:** inventing a flower variety that does not exist in reality just to match a color.

### 2. Material Translation
A visual effect is not a flower color. Decompose every effect into:

```text
flower + material + lighting + composition
```

- translucency → clear film, organza, frosted wrapping — not "translucent blue flowers"
- gloss / water / glass → transparent film, restrained acrylic, satin ribbon
- glow / halation → light-colored focal flowers under controlled light, fine metallic accents
- haze / fog → gypsophila, limonium, fine foliage, layered translucent material
- swirl / brush strokes → line material (curly willow, branches, grasses) and spiral arrangement
- grain / rough texture → seed heads, berries, dried texture, foliage contrast

The final design must state where each effect lives across these four channels.

### 3. Seasonal Availability
For any strongly seasonal flower:
- flag it as seasonal
- provide **at least one usable substitute** matched to its floral role (focal / mass / transition / line / filler)
- if the risk is high, name the substitute as the primary choice and the seasonal flower as the occasional upgrade

### 4. Construction Feasibility
Check the bouquet as a physical object:
- **bouquet stability** — the structure can be bound and held; line material is anchored, not floating
- **flower proportion** — stem counts and sizes fit the declared silhouette and density; no mathematically impossible composition
- **realistic florist workflow** — every material can be sourced, cut, and assembled by a working florist; no element requires fabrication that does not exist

If any of the four checks fails, revise the concept before writing the BOM.

## Color Mapping Priority
When a reference color is difficult to source naturally, use this order:
1. natural flower color approximation
2. foliage or naturally colored botanical material
3. wrapping / ribbon / translucent material
4. restrained decorative accents
5. dyed floral material only when needed

Avoid putting the entire color-matching burden on flowers.

## Image Generation Rules

- **Design board (LEVEL 1):** editorial floral design board — premium floral studio presentation, dark elegant layout, typography, botanical photography, design notes.
- **Bouquet visualization (LEVEL 2):** realistic bouquet product photography — realistic flower texture, natural petals, physically possible bouquet, luxury florist catalog style.

Keep the two styles separate: the board communicates the design; the final image sells the bouquet.

## Quality Gate
Before finalizing, check:
- Does the bouquet work as real floristry without the reference image?
- Was the **Floral Reality Check** completed for all four parts before the BOM?
- Is every Visual Translation Logic entry honest (`element → design language → floral language`)?
- Is the palette traceable to the source image?
- Are accent colors restrained according to their visual weight in the source?
- Are the flowers real and sourceable?
- Is every BOM item quantified, with a valid `flower status`?
- Are rare colors handled through materials rather than fabricated varieties?
- Are seasonal substitutions supplied where needed?
- Does the LEVEL 1 design board contain all eight parts?
- Does the LEVEL 2 visualization contain no text, labels, or diagrams?
- Is the render brief consistent with the BOM and design concept?

If any answer is no, revise before presenting the result.

## Common Mistakes
- **Literal copying:** turning pictured objects into floral props instead of translating visual language ("blue sky → blue flowers").
- **Color overfitting:** forcing impossible flower colors instead of using material and packaging.
- **Render-first design:** generating a beautiful picture before defining a buildable bouquet.
- **Fake precision:** treating generated flower counts as procurement truth.
- **Too many focal flowers:** losing hierarchy and visual rhythm.
- **Decoration overload:** butterflies, feathers, acrylic, or pearls should support the concept rather than become the concept.
- **Skipping the Reality Check:** writing a BOM before proving the design can exist in reality.
- **Bouquet-only output:** showing only the image without the design board.
- **Impossible structures:** proposing a bouquet no florist can build.

## Forbidden
1. **Directly copying reference elements** into flowers. Translate through design language instead: *wrong* "blue sky → blue flowers"; *correct* "blue sky → spatial atmosphere → blue wrapping + blue/purple flowers".
2. **Generating fantasy plants** — inventing flowers that do not exist.
3. **Forcing a color** with a flower that does not exist in reality.
4. **Outputting only a bouquet image** — the presentation package (LEVEL 1) is mandatory.
5. **Outputting impossible structures** — a bouquet that cannot be made by a working florist.
