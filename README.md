# Floral Art Director Skill

A reusable agent skill for translating the visual language of an album cover, painting, film still, photograph, illustration, or personal image into **professional, manufacturable floral artworks** — delivered as a complete design presentation package plus a realistic bouquet visualization.

## What is Floral Art Director

Floral Art Director is **not an image generator**. It is a design engine that inserts a real floristry layer between a reference image and a bouquet. Instead of copying what it sees, it reasons about what the image *means*, translates it through design language into floral language, and builds a bouquet that could actually be made by a florist:

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

The output is a two-level **Floral Design Presentation Package**:

- **LEVEL 1 — Floral Design Board:** the design proposal (Reference Analysis, Style DNA, Visual Translation Logic, Floral Design Concept, Floral Reality Check, Flower BOM, Structural Sketch, Alternative Views).
- **LEVEL 2 — Final Bouquet Visualization:** the commercial bouquet as realistic product photography — no text, no labels, no diagrams.

The **BOM, not the generated image, is the source of truth for construction and procurement.**

## Output

The default output is a complete presentation package with **five deliverables**:

1. **Reference Analysis** — color structure, light and shadow, texture, composition, emotional atmosphere
2. **Style DNA** — 4–7 keywords that capture the reference's visual logic
3. **Visual Translation Logic + Floral Design Concept** — every image feature mapped through `visual element → design language → floral language`, plus bouquet name, philosophy, structure, and emotion
4. **Flower BOM** — procurement-level material table with exact quantities, colors, roles, and flower status (`natural` / `dyed` / `preserved` / `decorative material`), plus Structural Sketch and Alternative Views
5. **Final Bouquet Visualization** — the LEVEL 2 product-photography image of the bouquet

> **Case study:** the *Starry Night* walkthrough in [examples/starry-night-example.md](examples/starry-night-example.md) shows the full pipeline on Vincent van Gogh's painting — cobalt night becomes deep-blue iris and navy wrapping, the cadmium moon becomes a concentrated yellow ranunculus cluster, and the swirl becomes curly-willow line work. The same reference is used as an adversarial input in [tests/presentation-package-test.md](tests/presentation-package-test.md), which checks that the default output is the full two-level presentation package.

## Features

- **Visual Language Analysis** — analyzes color structure, brightness, saturation, light, texture, composition, and mood into 4–7 Style DNA keywords
- **Floral Translation** — maps image features (color, line, haze, mass, negative space, gloss) into floral language through a design-language step
- **Two-level presentation package** — an 8-part Floral Design Board plus a clean product-photography Final Bouquet Visualization
- **Realistic BOM generation** — every item quantified with role, color, flower status, and substitutes
- **Feasibility checking** — real and sourceable material only; rare colors distributed across wrapping, foliage, and decoration before dyed flowers
- **Render brief** — the LEVEL 2 image brief is consistent with the BOM; the render is visualization only

## Design Philosophy

> **The bouquet must first exist as a real floral artwork, and then resemble the reference image.**

A direct image-to-image workflow often creates visually attractive but unrealistic flowers or colors. This skill inserts a floral-design layer between image analysis and rendering:

```text
Reference image
    ↓
Visual Language Analysis
    ↓
Floral Translation
    ↓
Floral Design Concept
    ↓
Floral Reality Check
    ↓
Flower BOM + Structural Sketch
    ↓
Presentation Package (LEVEL 1 board + LEVEL 2 visualization)
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

## Image Generation Rules

- **Design board (LEVEL 1):** editorial floral design board — premium floral studio presentation, dark elegant layout, typography, botanical photography, design notes.
- **Bouquet visualization (LEVEL 2):** realistic bouquet product photography — realistic flower texture, natural petals, physically possible bouquet, luxury florist catalog style.

Keep the two styles separate: the board communicates the design; the final image sells the bouquet.

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
│   ├── README.md
│   ├── 01-aquatic-mint.md
│   ├── 02-la-la-land.md
│   ├── 03-starry-night.md
│   └── starry-night-example.md  # v0.2 full pipeline case study (Starry Night)
└── tests/                       # Benchmark test suite — see README.md
    ├── README.md
    ├── 01-color-overfitting.md
    ├── 02-impossible-flower.md
    ├── 03-seasonal-flower.md
    ├── 04-minimal-style.md
    ├── 05-luxury-style.md
    ├── 06-floral-reality-check.md
    └── presentation-package-test.md  # v0.2 presentation package test (Starry Night input)
```

## Suggested future extensions

- city-specific flower availability and pricing
- seasonality database
- florist substitutions by budget
- structured JSON output for web/API use
- interactive controls for realism, budget, bouquet size, dye tolerance, and decorative elements
- automated presentation-package renderer (design board → final bouquet image)
