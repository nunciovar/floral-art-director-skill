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

### 7. Design Sketch
Generate a florist-style structural sketch of the bouquet — a professional florist design drawing, not an engineering CAD diagram:
- flower position (focal, supporting, line, filler)
- height hierarchy
- bouquet outline
- flower hierarchy
- focal flower position
- line flower direction
- foliage structure
- spatial relationship
- wrapping

### 8. Alternative Angle View
Generate multiple bouquet views to show structure consistency. Recommended 2×2 layout:
- front view
- 45 degree view
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

`| Flower / Material | Quantity | Color | Role | Status | Substitute |`

- real, commercially available flowers only
- every flower has an exact quantity
- no "some flowers"
- no invented flowers
- dyed material is marked `dyed flower`
- seasonal alternatives are identified in the Substitute column

#### 7. Design Sketch
Florist-style structural drawing (not CAD): bouquet outline · flower hierarchy · focal flower position · line flower direction · foliage structure · spatial relationship · wrapping.

#### 8. Alternative Angle View
Multiple views showing structure consistency. Recommended 2×2 layout: front view · 45 degree view · side view · detail view.

### LEVEL 2 — Final Bouquet Visualization

Generate the final commercial bouquet as a standalone image, separate from the design board.

**Requirements:**
- must look like real flower-shop product photography
- realistic flower texture, natural petals, physically possible bouquet

**Forbidden in this image:** text · infographic · tables · labels · diagrams · color palettes.

**Only show:** bouquet · flowers · wrapping · realistic lighting.

**Photography style:** professional floral photography, luxury florist catalog style.

## Presentation Structure System

The skill generates a complete floral art direction presentation board. **The output structure is fixed; the visual theme is adaptive.** This chapter locks the information architecture — the modules, their order, and the floral design logic — while the presentation style follows the reference image.

The seven fixed components below must always be present. The LEVEL 1 design board (see Required Output) additionally retains **Reference Analysis** and **Floral Design Concept** as its opening modules; they feed the Style DNA and the board's design narrative.

### Purpose

The skill should generate a complete floral art direction presentation board.

The output should feel like:
- premium florist proposal
- editorial floral design sheet
- art direction board

It should NOT feel like:
- generic infographic
- business dashboard
- engineering report

### Fixed Output Components

Every complete generation should contain:

#### 1. Style DNA

Purpose: translate the visual identity of the reference image.

Include:
- dominant colors
- supporting colors
- brightness
- saturation
- temperature
- lighting
- texture
- emotion

Provide 4-7 keywords.

#### 2. Visual Translation Logic

Show:

```text
Reference Element
    ↓
Visual Interpretation
    ↓
Floral Translation
```

Examples:
- Ocean color → calm transparency → blue hydrangea + delphinium
- Eye highlight → amber emotional focal point → orange tulip + warm accent flowers

This section should visually explain why the bouquet design matches the reference.

#### 3. Floral Reality Check

Keep this module. Evaluate:
- Color feasibility
- Material translation
- Seasonal availability
- Construction feasibility

Purpose: ensure the artistic design can become a real bouquet.

#### 4. Flower BOM

Must remain procurement-oriented. Use table format:

`| Flower / Material | Quantity | Color | Role | Status | Substitute |`

Rules:
- real commercially available flowers
- exact quantity
- identify dyed flowers
- identify seasonal alternatives

#### 5. Design Sketch

Generate a florist-style structural sketch.

Requirements:
- bouquet outline
- flower hierarchy
- focal flower position
- line flower direction
- foliage structure
- spatial relationship

It should resemble a professional florist design drawing — NOT an engineering CAD diagram.

#### 6. Alternative Angle View

Generate multiple bouquet views.

Recommended 2×2 layout:
- front view
- 45 degree view
- side view
- detail view

Purpose: show bouquet structure consistency.

#### 7. Final Bouquet

Generate a standalone product image.

Requirements:
- bouquet only
- realistic flower texture
- commercial photography quality
- independent from the presentation board

This image represents the final product.

## Presentation Layout Priority

The presentation board should prioritize:

1. **Hero Bouquet Image** — largest visual element
2. **Reference Image** — visual source
3. **Style DNA**
4. **Translation Logic**
5. **BOM**
6. **Design Sketch**
7. **Alternative Views**

The bouquet should remain the emotional center. Do not allow text modules to dominate the image.

## Visual Theme Adaptation

The presentation style must follow the reference image.

The system must NOT force a fixed:
- background color
- accent color
- typography color
- decorative style

Instead, analyze:
- mood
- palette
- era
- artistic language

and adapt the presentation.

Examples:
- Dark cinematic photo → dark background → dramatic lighting
- Pastel painting → soft background → gentle editorial layout
- Minimal monochrome → clean monochrome presentation

## Image Generation Brief

Every design is delivered as **two separate prompts**.

### A. Floral Presentation Board Prompt

Describes the board itself:
- overall board layout
- reference panel
- Style DNA panel
- BOM panel
- sketch panel
- alternative views

### B. Final Bouquet Product Prompt

Describes only the bouquet:
- bouquet only
- realistic photography
- lighting
- camera
- material

Prompt A drives the LEVEL 1 board presentation; prompt B drives the LEVEL 2 Final Bouquet Visualization.

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

- **Design board (LEVEL 1):** editorial floral design board — premium floral studio presentation, typography, botanical photography, design notes. The layout theme adapts to the reference (see Visual Theme Adaptation); dark elegant is only one possible style.
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
- Is the output structure fixed (all seven Presentation Structure components) while the visual theme adapts to the reference — no forced black background, fixed accent color, or PPT style?
- Does the Image Generation Brief contain both prompts (A. board, B. bouquet product)?

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
- **Fixed theme lock:** forcing the same presentation theme (black background, orange-gold accent) on every reference instead of adapting the style.
- **Text-heavy board:** letting text modules dominate the board instead of keeping the bouquet the emotional center.

## Forbidden
1. **Directly copying reference elements** into flowers. Translate through design language instead: *wrong* "blue sky → blue flowers"; *correct* "blue sky → spatial atmosphere → blue wrapping + blue/purple flowers".
2. **Generating fantasy plants** — inventing flowers that do not exist.
3. **Forcing a color** with a flower that does not exist in reality.
4. **Outputting only a bouquet image** — the presentation package (LEVEL 1) is mandatory.
5. **Outputting impossible structures** — a bouquet that cannot be made by a working florist.
