# Example Gallery

Each example walks the full Floral Art Director pipeline, from a **reference image** to a buildable bouquet:

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

Every case is a **design document**, not a rendered picture. The BOM is the source of truth for construction and procurement; the render brief is only its visualization spec. Case pages embed their showcase renders (under `assets/images/…`) at the bottom as the realized visual output of each design.

## Cases

| # | Case | Visual challenge |
|---|---|---|
| 01 | [Aquatic Mint](01-aquatic-mint.md) | Water-green palette, translucency, airy negative space |
| 02 | [La La Land](02-la-la-land.md) | Purple-blue night palette, romantic cinematic mood, starlight atmosphere |
| 03 | [Starry Night](03-starry-night.md) | Strong blue–gold contrast, painterly/artistic, deliberately non-realistic colors (includes the final bouquet render and the same reference in Vase + Vessel formats) |
| 04 | [Amber Within](04-amber-within.md) | Conceptual photography (monochrome eye + amber pupil) → focal-color hierarchy, monochrome translation, line structure, emotional translation, real-world manufacturability |

Each case stresses a different translation problem — **material realism**, **mood translation**, **handling impossible colors**, and **focal-color hierarchy inside a monochrome field** — and shows how the skill resolves it with real floristry. All four examples follow the same one-page design-document structure, and each visual case owns an independent namespace under `assets/images/…` (the Amber Within case is `assets/images/case_eye_amber/…`), independent of the other cases.
