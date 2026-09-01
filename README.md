# Floral Art Director Skill

A reusable agent skill for translating the visual language of an album cover, painting, film still, photograph, illustration, or personal image into a realistic floral bouquet design.

## What is Floral Art Director

Floral Art Director is **not an image generator**. It is a design engine that inserts a real floristry layer between a reference image and a bouquet. Instead of copying what it sees, it reasons about what the image *means* and builds a bouquet that could actually be made by a florist:

```text
Reference Image
    ↓
Visual Analysis
    ↓
Design Reasoning
    ↓
Floral Translation
    ↓
Real-world Bouquet
```

The output is always a set of four sections:

1. **Style DNA** — palette, light, texture, composition, mood, keywords
2. **Floral Design Concept** — name, silhouette, density, size, design logic
3. **Flower BOM** — real flowers/materials with colors, exact quantities, roles, dye status, substitutions
4. **Image Generation Brief** — a production-ready prompt for bouquet visualization

The **BOM, not the generated image, is the source of truth for construction and procurement.**

## Features

- **Style DNA extraction** — analyzes color structure, brightness, saturation, light, texture, composition, and mood into 4–7 keywords
- **Floral translation** — maps image language (color, line, haze, mass, negative space, gloss) into floral language
- **Realistic BOM generation** — every item quantified with role, color, dye status, and substitutes
- **Feasibility checking** — real and sourceable material only; rare colors distributed across wrapping, foliage, and decoration before dyed flowers
- **Image generation brief** — one production-ready prompt plus visual priorities, consistent with the BOM

## Design Philosophy

> **The bouquet must first work as real floristry, and only then resemble the reference image.**

A direct image-to-image workflow often creates visually attractive but unrealistic flowers or colors. This skill inserts a floral-design layer between image analysis and rendering:

```text
Reference image
    ↓
Style DNA
    ↓
Floral translation
    ↓
Feasibility audit
    ↓
Flower BOM + Design Concept
    ↓
Image Generation Brief
    ↓
Rendered bouquet
```

## Floral Reality Check

The system does not only generate beautiful images. It evaluates whether the bouquet can exist in reality.

Every design passes a mandatory **Floral Reality Check** before any flower is written into the BOM:

```text
Reference Image
    ↓
Visual Understanding
    ↓
Floral Reasoning
    ↓
Reality Validation
    ↓
Bouquet Design
```

Four checks are applied:

- **Color Feasibility** — every color is classified as a *natural flower color*, an *approximation* carried by material, or a labeled *dyed flower*. No invented varieties.
- **Material Translation** — visual effects are decomposed into `flower + material + lighting + composition`; translucency is never reduced to a flower color.
- **Seasonal Availability** — strongly seasonal flowers always carry a substitute matched to their floral role.
- **Construction Feasibility** — the bouquet is stable, proportionate, and buildable by a working florist.

## Repository structure

```text
.
├── SKILL.md                     # The skill definition (workflow + quality gate)
├── README.md
├── agents/
│   └── openai.yaml              # OpenAI Agent Skill configuration
├── assets/
│   └── icon.svg
├── examples/                    # Example gallery — see README.md
│   ├── 01-aquatic-mint.md
│   ├── 02-la-la-land.md
│   └── 03-starry-night.md
└── tests/                       # Benchmark test suite — see README.md
    ├── 01-color-overfitting.md
    ├── 02-impossible-flower.md
    ├── 03-seasonal-flower.md
    ├── 04-minimal-style.md
    └── 05-luxury-style.md
```

## Suggested future extensions

- city-specific flower availability and pricing
- seasonality database
- florist substitutions by budget
- structured JSON output for web/API use
- interactive controls for realism, budget, bouquet size, dye tolerance, and decorative elements
