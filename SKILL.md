---
name: floral-art-director
description: Use when a user provides a reference image and wants its visual language, palette, mood, composition, or material qualities translated into a realistic, buildable floral bouquet design.
---

# Floral Art Director

## Overview
Translate a reference image into a physically plausible floral design. The bouquet should first work as real floristry, and only then echo the image's visual identity.

## When to Use
Use for album covers, paintings, film stills, photographs, illustrations, or personal images when the user wants a bouquet derived from the image's mood, palette, light, texture, or composition.

Do not use this skill merely to identify flowers already visible in an image or to copy literal objects from the reference into a bouquet.

## Core Workflow

```text
Reference Image
    ↓
Visual Analysis
    ↓
Style DNA
    ↓
Floral Design Concept
    ↓
Floral Reality Check
    ↓
Flower BOM
    ↓
Image Generation Brief
```

### 1. Visual Analysis
Analyze:
- color structure: primary, secondary, accent colors
- brightness and saturation
- warm/cool balance
- light and shadow
- material qualities and transparency
- composition and visual center
- rhythm and density
- emotional tone and theme

When useful, provide approximate HEX values, but treat them as visual guides rather than measurement claims.

### 2. Style DNA
Summarize the reference in 4–7 concise keywords. Prefer words that describe atmosphere, color behavior, structure, emotion, and material quality.

Examples: `Aquatic · Mint · Translucent · Floating · Serene · Sunlit`.

### 3. Floral Design Concept
Describe the intended bouquet before any flower is chosen: name, concept/theme, overall style, approximate size, silhouette and density, and the design logic that maps the image to the bouquet.

If the user gives no budget, recipient, or size, assume a medium-budget, medium-size gift bouquet.

### 4. Floral Reality Check
**Mandatory step.** Run before writing any BOM item. The Reality Check proves the design can exist in the real world. Complete all four checks described in the dedicated [Floral Reality Check](#floral-reality-check) chapter below: Color Feasibility, Material Translation, Seasonal Availability, and Construction Feasibility.

### 5. Flower BOM
The BOM is the source of truth for real construction and must be independent from the rendered image.

For every floral material include:
- flower/material name
- color
- exact stem count or quantity
- floral role
- **flower status** — exactly one of: `natural` · `dyed` · `preserved` · `decorative material`
- substitute if seasonal or difficult to source

Also list wrapping and auxiliary materials with quantities.

The image generator is not expected to depict exact stem counts. Do not infer procurement quantities from rendered pixels.

### 6. Image Generation Brief
Write a complete image-generation brief that specifies:
- bouquet subject and silhouette
- palette
- principal flower families
- spacing and layering
- wrapping and decorative material
- background
- lighting
- camera / still-life presentation
- realism requirement

Default to a premium florist portfolio still-life photograph with a simple background unless the user asks for another presentation.

When a reference thumbnail is desired in the final mockup, explicitly reserve a small inset area for it rather than integrating the literal scene into the bouquet.

## Floral Reality Check

The system does not only generate beautiful images — it evaluates whether the bouquet can exist in reality. This chapter is mandatory: **no BOM item may be written until all four checks pass.**

### 1. Color Feasibility

For every color that matters in the design, classify it as exactly one of:

- **natural flower color** — a color that exists naturally in a real flower variety (use it directly)
- **approximate color** — no exact match exists; use the closest natural variety and carry the remainder through material (foliage, wrapping, ribbon, translucent film, decoration)
- **dyed flower required** — the hue has no acceptable natural approximation and is essential to the design; then, and only then, specify a real flower variety to be dyed and label it `染色花材`

**Forbidden:** inventing a flower variety that does not exist in reality just to match a color. If a hue is rare, distribute it across materials before relying on dyed flowers.

### 2. Material Translation

A visual effect is **not** a flower color. Decompose every effect into:

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

## Required Output
Always produce these four sections in this order:

### ① Style DNA
Include visual analysis and 4–7 keywords.

### ② Floral Design Concept
Include name, style, size, silhouette, density, design logic, and intended use if relevant.

### ③ Flower BOM
Use a table whenever practical.

Recommended columns:
`类别 | 花材名称 | 颜色 | 枝数/数量 | 角色/用途 | 花材状态 | 是否染色 | 替代品种`

`花材状态` accepts exactly one of: `natural` · `dyed` · `preserved` · `decorative material`.

Then list wrapping and auxiliary materials.

### ④ Image Generation Brief
Provide one production-ready prompt plus a short list of visual priorities.

## Quality Gate
Before finalizing, check:
- Does the bouquet work as real floristry without the reference image?
- Was the **Floral Reality Check** completed for all four parts before the BOM?
- Is the palette traceable to the source image?
- Are accent colors restrained according to their visual weight in the source?
- Are the flowers real and sourceable?
- Is every BOM item quantified, with a valid `花材状态`?
- Are rare colors handled through materials rather than fabricated varieties?
- Are seasonal substitutions supplied where needed?
- Is the render brief consistent with the BOM and design concept?

If any answer is no, revise before presenting the result.

## Common Mistakes
- **Literal copying:** turning pictured objects into floral props instead of translating visual language.
- **Color overfitting:** forcing impossible flower colors instead of using material and packaging.
- **Render-first design:** generating a beautiful picture before defining a buildable bouquet.
- **Fake precision:** treating generated flower counts as procurement truth.
- **Too many focal flowers:** losing hierarchy and visual rhythm.
- **Decoration overload:** butterflies, feathers, acrylic, or pearls should support the concept rather than become the concept.
- **Skipping the Reality Check:** writing a BOM before proving the design can exist in reality.
