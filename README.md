# Floral Art Director Skill

A reusable agent skill for translating the visual language of an album cover, painting, film still, photograph, illustration, or personal image into a realistic floral bouquet design.

The core principle is simple:

> **The bouquet must first work as real floristry, and only then resemble the reference image.**

## What it produces

1. **Style DNA** — palette, light, texture, composition, mood, keywords
2. **Floral Design Concept** — bouquet name, silhouette, density, size, design logic
3. **Flower BOM** — real flowers/materials with colors, exact quantities, roles, dye status, substitutions
4. **Image Generation Brief** — a production-ready prompt for bouquet visualization

## Why this is different from reference-image generation

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

The **BOM, not the generated image, is the source of truth for construction and procurement**.

## Repository structure

```text
.
├── SKILL.md
├── README.md
├── examples/
│   └── aquatic-mint-example.md
└── tests/
    └── pressure-tests.md
```

## Suggested future extensions

- city-specific flower availability and pricing
- seasonality database
- florist substitutions by budget
- structured JSON output for web/API use
- interactive controls for realism, budget, bouquet size, dye tolerance, and decorative elements
