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

### 3. Floral Translation
Map image language into floral language:

| Image feature | Floral mapping |
|---|---|
| Dominant colors | Natural flower colors first; foliage and wrapping may carry difficult hues |
| Highlight color | Focal flower or sparse accent flower |
| Strong directional lines | Delphinium, snapdragon, branches, grasses, or other line material |
| Soft haze | Gypsophila, limonium, fine foliage, translucent layers |
| Dense visual mass | Clustered focal and mass flowers |
| Negative space | Open asymmetrical structure and restrained filler |
| Gloss / water / glass | Clear film, organza, translucent wrapping, restrained acrylic detail |
| Grain / rough texture | Seed heads, berries, dried texture, foliage contrast |

Do not reproduce the image literally. Preserve the overall visual logic.

### 4. Feasibility Check
Before writing the BOM, audit the design for real-world floristry:
- Prefer commercially available flowers and foliage.
- Never invent flower varieties just to match a color.
- Mark artificially colored material as `染色花材`.
- If a target hue is rare in natural flowers, distribute that color across wrapping, foliage, ribbon, or decorative material before relying on dyed flowers.
- Keep flower roles coherent: focal, mass, transition, line, filler, foliage, decorative material.
- Avoid structurally impossible combinations or excessive decorative elements that make the bouquet non-buildable.
- If a flower is strongly seasonal, provide at least one substitute.

### 5. Floral Design Concept
Provide:
- bouquet name
- concept / theme
- overall style
- approximate size
- bouquet silhouette and density
- suitable recipient or occasion when relevant
- concise explanation of how image features became floral decisions

If the user gives no budget, recipient, or size, assume a medium-budget, medium-size gift bouquet.

### 6. Flower BOM
The BOM is the source of truth for real construction and must be independent from the rendered image.

For every floral material include:
- flower/material name
- color
- exact stem count or quantity
- floral role
- whether dyed
- substitute if seasonal or difficult to source

Also list wrapping and auxiliary materials with quantities.

The image generator is not expected to depict exact stem counts. Do not infer procurement quantities from rendered pixels.

### 7. Image Generation Brief
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
`类别 | 花材名称 | 颜色 | 枝数/数量 | 角色/用途 | 是否染色 | 替代品种`

Then list wrapping and auxiliary materials.

### ④ Image Generation Brief
Provide one production-ready prompt plus a short list of visual priorities.

## Quality Gate
Before finalizing, check:
- Does the bouquet work as real floristry without the reference image?
- Is the palette traceable to the source image?
- Are accent colors restrained according to their visual weight in the source?
- Are the flowers real and sourceable?
- Are rare colors handled through materials rather than fabricated varieties?
- Is every BOM item quantified?
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
