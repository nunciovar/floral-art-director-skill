---
name: floral-art-director
description: Use when a user provides a reference image — album cover, painting, movie still, photograph, illustration, or personal image — and wants its visual language translated into a professional, manufacturable floral artwork, delivered as a full design presentation package plus a realistic final floral piece (wrapped bouquet, vase arrangement, vessel arrangement, or floral installation).
---

# Floral Art Director

## Overview
An AI floral design system that translates visual references into **professional, manufacturable floral artworks**.

**The floral piece must first exist as a real floral artwork, and then resemble the reference image.**

The system spans **multiple floral formats**: Wrapped Bouquet（手绑花束）· Vase Arrangement（瓶插花艺）· Vessel Arrangement（盆器插花）· Floral Installation（艺术花艺装置）.

## When to Use
Use for album covers, paintings, film stills, photographs, illustrations, or personal images when the user wants a professional floral artwork derived from the image's mood, palette, light, texture, or composition.

Do not use this skill merely to identify flowers already visible in an image, or to copy literal objects from the reference into a floral piece.

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
Final Floral Piece Visualization
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

### 4. Floral Format Selection
After the Style DNA, decide the floral format that best matches the reference's visual language, spatial relationships, emotional expression, and intended usage scenario — see the dedicated [Floral Format Selection](#floral-format-selection) chapter. Choose **one or more** of: Wrapped Bouquet · Vase Arrangement · Vessel Arrangement · Floral Installation. Record the choice and its reasoning in the [Floral Format Decision](#floral-format-decision).

### 5. Floral Design Concept
Describe the intended floral piece (in its selected format) before any flower is chosen:
- piece name (format-aware)
- design philosophy
- structure (silhouette, density, size) — adapted to the selected format
- emotional expression

If the user gives no budget, recipient, or size, assume a medium-budget, medium-size piece appropriate to the selected format.

### 6. Floral Reality Check
**Mandatory step.** Run before writing any BOM item. Complete all four checks in the dedicated [Floral Reality Check](#floral-reality-check) chapter: Color Feasibility, Material Translation, Seasonal Availability, Construction Feasibility.

### 7. Flower BOM
The BOM is the source of truth for real construction and procurement, and must be independent from any rendered image.

For every floral material include:
- flower/material name
- color
- exact stem count or quantity
- floral role
- **flower status** — exactly one of: `natural` · `dyed` · `preserved` · `decorative material`
- substitute if seasonal or difficult to source

Every BOM item must be quantified. "Some flowers" is not a BOM.

Also list wrapping (for a bouquet), the container (for vase/vessel/installation), and auxiliary materials with quantities.

### 8. Design Sketch
Generate a florist-style structural sketch of the floral piece in its selected format — a professional florist design drawing, not an engineering CAD diagram:
- flower position (focal, supporting, line, filler)
- height hierarchy
- piece outline
- flower hierarchy
- focal flower position
- line flower direction
- foliage structure
- spatial relationship
- wrapping

### 9. Alternative Angle View
Generate multiple views of the piece to show structure consistency. Recommended 2×2 layout:
- front view
- 45 degree view
- side view
- detail view (e.g. a close focal flower, the binding point, or a wrapping fold)

## Floral Format Selection

After the Style DNA, the AI must automatically decide the floral format that best fits the reference's visual language, spatial relationships, emotional expression, and intended usage scenario. One or more formats may be selected. Record the decision in the Floral Format Decision.

### 1. Wrapped Bouquet（手绑花束）
The classic hand-tied bouquet.

Suitable for:
- gift-giving scenarios
- a strong central visual focus
- presentation through wrapping

Design focus:
- bouquet outline
- wrapping material
- flower layering and hierarchy
- handheld visual proportion

### 2. Vase Arrangement（瓶插花艺）
Suitable for:
- spatial display
- home and interior
- tabletop art

Design focus:
- the container must never steal the visual center from the flowers
- prefer: transparent glass bottles · plain ceramic bottles · linen-textured containers · plain stone vessels
- forbid: luxurious decorated vases · complex-texture containers · overly artistic containers

Principle: **Container supports flowers, not competes with flowers.**

### 3. Vessel Arrangement（盆器插花）
Suitable for:
- Eastern flower arranging
- art installations
- horizontal spatial expression

Design focus:
- a low, plain basin or vessel
- emphasize the spatial relationships of the flowers
- emphasize branch direction and line flow
- emphasize negative space（留白）

Recommended containers: plain clay pots · concrete pots · shallow stone basins · matte black pots.

Forbidden: overly decorative containers.

### 4. Floral Installation（艺术花艺装置）
Suitable for:
- exhibitions
- concept design
- large-scale expression

Design focus:
- scale, spatial presence, and the reference's concept
- structural mounting must be realistically buildable by a working florist
- every material must be obtainable — nothing floats unsupported

## Required Output — Floral Design Presentation Package

The default output is a complete presentation package in two levels, produced **for each selected floral format** (see [Floral Format Selection](#floral-format-selection)). **LEVEL 1 is the per-format design board; LEVEL 2 is the per-format final render** — the final piece may be a wrapped bouquet, vase arrangement, vessel arrangement, or floral installation, not necessarily a bouquet. The package opens with the Floral Format Decision and delivers each selected format independently.

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
- Piece name (format-aware)
- Design philosophy
- Structure (silhouette, density, size) — adapted to the selected format
- Emotional expression

#### 5. Floral Reality Check
Answer all four questions:
- **Color Feasibility** — can this color be achieved with real flower material?
- **Material Translation** — where a color or effect cannot be achieved by flowers, state the exact channel: `wrapping`, `foliage`, `lighting`, or `accessory`.
- **Seasonal Availability** — list the seasonal flowers and their substitutes.
- **Construction Feasibility** — piece size, structure, manufacturability.

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
Florist-style structural drawing (not CAD): piece outline · flower hierarchy · focal flower position · line flower direction · foliage structure · spatial relationship · wrapping (bouquet), container and waterline (vase), or horizontal spread and negative space (vessel).

#### 8. Alternative Angle View
Multiple views showing structure consistency. Recommended 2×2 layout: front view · 45 degree view · side view · detail view.

### LEVEL 2 — Final Floral Piece Visualization

Generate the final floral piece (wrapped bouquet, vase arrangement, vessel arrangement, or installation) as a standalone image, separate from its design board. Name it by format: **Final Bouquet**, **Vase Arrangement Final Render**, **Vessel Arrangement Final Render**, or **Installation Final Render**.

**Requirements:**
- must look like real product photography for the chosen format
- realistic flower texture, natural petals and material, physically possible arrangement
- the container (if any) supports the flowers, never competes with them

**Forbidden in this image:** text · infographic · tables · labels · diagrams · color palettes.

**Only show:** the piece — flowers, and the container or wrapping the format uses · realistic lighting.

**Photography style:** professional floral photography, luxury florist catalog style.

## Floral Format Decision

The final design plan must open with the format decision.

### Selected Format
(choose one or more)
- Wrapped Bouquet（手绑花束）
- Vase Arrangement（瓶插花艺）
- Vessel Arrangement（盆器插花）
- Floral Installation（艺术花艺装置）

### Reason
Explain why the selected format(s) best match the reference's:
- visual language
- spatial relationships
- emotional expression
- usage scenario

### Format-Specific Deliverables

Each selected format is delivered **independently** — its own design board and its own final render.

- **Wrapped Bouquet** → Bouquet Design Board + Final Bouquet
- **Vase Arrangement** → Vase Arrangement Design Board + Vase Arrangement Final Render
- **Vessel Arrangement** → Vessel Arrangement Design Board + Vessel Arrangement Final Render
- **Floral Installation** → Floral Installation Design Board + Floral Installation Final Render

Each design board carries the fixed components (Style DNA, Visual Translation Logic, Floral Reality Check, Flower BOM, Design Sketch, Alternative Angle View) tuned to that format. Each final render is a standalone product image of that format.

❌ **Forbidden:** combining bouquet + vase + vessel (or any formats) into one horizontal display image.
✅ **Required:** each selected format shown independently, never mixed in a single frame.

## Presentation Structure System

The skill generates a complete floral art direction presentation board. **The output structure is fixed; the visual theme is adaptive.** This chapter locks the information architecture — the modules, their order, and the floral design logic — while the presentation style follows the reference image.

The seven fixed components below must be present in **every format-specific design board**. The LEVEL 1 design board (see Required Output) additionally retains **Reference Analysis** and **Floral Design Concept** as its opening modules; they feed the Style DNA and the board's design narrative.

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

This section should visually explain why the design matches the reference.

#### 3. Floral Reality Check

Keep this module. Evaluate:
- Color feasibility
- Material translation
- Seasonal availability
- Construction feasibility

Purpose: ensure the artistic design can become a real floral piece in its selected format.

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
- piece outline
- flower hierarchy
- focal flower position
- line flower direction
- foliage structure
- spatial relationship

It should resemble a professional florist design drawing — NOT an engineering CAD diagram.

#### 6. Alternative Angle View

Generate multiple views of the piece.

Recommended 2×2 layout:
- front view
- 45 degree view
- side view
- detail view

Purpose: show structure consistency of the piece.

#### 7. Final Floral Piece

Generate a standalone final image of the selected floral format — wrapped bouquet, vase arrangement, vessel arrangement, or floral installation (not necessarily a bouquet).

Requirements:
- the selected piece only
- realistic flower texture
- commercial photography quality
- independent from the presentation board

This image represents the final product.

## Presentation Layout Priority

The presentation board should prioritize:

1. **Hero Image of the Piece** — largest visual element
2. **Reference Image** — visual source
3. **Style DNA**
4. **Translation Logic**
5. **BOM**
6. **Design Sketch**
7. **Alternative Views**

The floral piece should remain the emotional center. Do not allow text modules to dominate the image.

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

## Presentation Board Style

Every format-specific design board is built in the same premium art-direction language — the modules vary by format, the visual quality never degrades.

- **Premium magazine feel** — editorial layouts, refined typography hierarchy, generous breathing space; each module sits on a modular card with clear spatial separation
- **Hero visual** — the board opens with the piece (or its reference) as the dominant image
- **Bilingual titles** — an **English main title** with a **Chinese auxiliary title（中文辅助标题）** beneath it
- **Art-direction modules** — Style DNA, Visual Translation Logic, Floral Reality Check, Flower BOM, Design Sketch line art, Alternative Angle View rendered as designed panels, never as raw lists
- **Tone** — a restrained dark ground is the default premium board base; the tone may soften or shift to follow the reference's mood, palette, and era (see Visual Theme Adaptation). Do not force a background that fights the reference.

Never degrade the board to:
- a generic PPT slide
- an e-commerce detail page
- a bare collection of AI-generated images

## Image Generation Brief

Every design is delivered as **two separate prompts**.

### A. Floral Presentation Board Prompt

Describes the board itself:
- overall board layout
- format-titled board (English main title + Chinese auxiliary title)
- reference panel
- Style DNA panel
- BOM panel
- sketch panel
- alternative views

### B. Final Floral Piece Product Prompt

Describes only the selected piece (wrapped bouquet, vase arrangement, vessel arrangement, or floral installation):
- the selected piece only
- for vase/vessel/installation, the container is present but plain and supportive
- realistic photography
- lighting
- camera
- material

Prompt A drives the LEVEL 1 board presentation; prompt B drives the LEVEL 2 Final Floral Piece Visualization.

## Floral Reality Check

The system does not only generate beautiful images — it evaluates whether the piece can exist in reality. No BOM item may be written until all four checks pass.

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
Check the piece as a physical object:
- **structural stability** — the structure can be bound, held, or mounted; line material is anchored, not floating
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

- **Design board (LEVEL 1):** editorial floral design board — premium magazine layout, modular cards, bilingual titles, botanical photography, design notes, hero visual. Built in the board style described in Presentation Board Style; its tone adapts to the reference (see Visual Theme Adaptation); dark elegant is the default but never the only possible style.
- **Final floral piece (LEVEL 2):** realistic product photography of the selected format — realistic flower texture, natural petals, physically possible piece, plain supportive container or wrapping, luxury florist catalog style.

Keep the two styles separate: the board communicates the design; the final image sells the piece.

## Quality Gate
Before finalizing, check:
- Does the piece work as real floristry without the reference image?
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
- Does the Image Generation Brief contain both prompts (A. board, B. final floral piece product)?
- Does the package open with the **Floral Format Decision** (Selected Format + Reason)?
- Is every selected format delivered **independently** — its own design board and its own final render — never combined into one image?
- Does each final render match its selected format (vase → Vase Arrangement Final Render; vessel → Vessel Arrangement Final Render)?
- Does every design board keep the premium art-direction style (magazine layout, modular cards, bilingual titles) — no PPT, e-commerce detail page, or AI-image gallery look?

If any answer is no, revise before presenting the result.

## Common Mistakes
- **Literal copying:** turning pictured objects into floral props instead of translating visual language ("blue sky → blue flowers").
- **Color overfitting:** forcing impossible flower colors instead of using material and packaging.
- **Render-first design:** generating a beautiful picture before defining a buildable piece.
- **Fake precision:** treating generated flower counts as procurement truth.
- **Too many focal flowers:** losing hierarchy and visual rhythm.
- **Decoration overload:** butterflies, feathers, acrylic, or pearls should support the concept rather than become the concept.
- **Skipping the Reality Check:** writing a BOM before proving the design can exist in reality.
- **Bouquet-only output:** showing only the image without the design board.
- **Impossible structures:** proposing a piece no florist can build.
- **Wrong format:** defaulting to a bouquet when the reference's spatial language calls for a vase, vessel, or installation.
- **Mixing formats in one image:** combining bouquet + vase + vessel in a single frame instead of delivering each format independently.
- **Container competing with flowers:** a decorated or artistic vase/vessel stealing the visual center from the arrangement.
- **Board degradation:** letting the board collapse into a PPT slide, an e-commerce detail page, or a bare collection of AI images.
- **Fixed theme lock:** forcing the same presentation theme (black background, orange-gold accent) on every reference instead of adapting the style.
- **Text-heavy board:** letting text modules dominate the board instead of keeping the piece the emotional center.

## Forbidden
1. **Directly copying reference elements** into flowers. Translate through design language instead: *wrong* "blue sky → blue flowers"; *correct* "blue sky → spatial atmosphere → blue wrapping + blue/purple flowers".
2. **Generating fantasy plants** — inventing flowers that do not exist.
3. **Forcing a color** with a flower that does not exist in reality.
4. **Outputting only a floral piece image** — the presentation package (LEVEL 1) is mandatory.
5. **Outputting impossible structures** — a piece that cannot be made by a working florist.
6. **Combining floral formats in one display** — bouquet + vase + vessel (or any formats) in a single horizontal image; each selected format must be shown in its own independent board and render.
7. **Letting the container compete with the flowers** — for vase and vessel arrangements, the container must stay plain and supportive; it supports the flowers, never competes with them.
