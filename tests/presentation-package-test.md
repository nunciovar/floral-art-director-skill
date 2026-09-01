# Test 07 — Presentation Package (Starry Night input)

Targets the v0.2 default output: the two-level **Floral Design Presentation Package**.

## Input scenario

Reference image: Vincent van Gogh's *The Starry Night* — swirling cobalt-and-indigo night sky, painterly brush strokes, glowing cadmium-yellow crescent moon and star halos, teal-cyan undertones, dark village silhouette.

Run the skill end-to-end with this reference. Score the response against Expected Behavior below.

## Expected behavior

The response is a complete **LEVEL 1 Floral Design Board** containing all eight parts:

1. **Reference Analysis** — color structure, light and shadow, texture, composition, emotional atmosphere
2. **Style DNA** — 4–7 concise keywords (e.g. cobalt, solar yellow, swirling, expressive)
3. **Visual Translation Logic** — every major element mapped as `visual element → design language → floral language` (e.g. *dark night sky → deep spatial background → dark wrapping and foliage*; *golden stars → energy points → yellow focal flowers*)
4. **Floral Design Concept** — bouquet name, design philosophy, structure, emotional expression
5. **Floral Reality Check** — all four answers: Color Feasibility, Material Translation, Seasonal Availability, Construction Feasibility
6. **Flower BOM** — a procurement-level table in the format `|Flower/Material|Quantity|Color|Role|Status|`, every item quantified, each with a valid flower status (`natural` / `dyed` / `preserved` / `decorative material`), plus substitutes for seasonal material
7. **Structural Sketch** — flower position, height hierarchy, focal/supporting/line flowers, wrapping
8. **Alternative Views** — at least three views (front, side, detail)

The response also contains a **LEVEL 2 Final Bouquet Visualization**:

- A standalone bouquet image that looks like real flower-shop product photography (realistic flower texture, natural petals, physically possible bouquet)
- **No** text, infographic, tables, labels, diagrams, or color palettes in the image
- **Only** bouquet, flowers, wrapping, realistic lighting

## Checkpoints (each must pass)

| # | Check | v0.2 skill requirement |
|---|---|---|
| 1 | Style DNA | 4–7 keywords present in LEVEL 1 |
| 2 | Translation Logic | `element → design language → floral language` mapping present; cobalt night → dark wrapping/foliage, not "blue flowers" |
| 3 | BOM | table format `|Flower/Material|Quantity|Color|Role|Status|`; exact quantities; valid flower status per item; seasonal substitutes present |
| 4 | Structural Sketch | present with position + height hierarchy + focal + wrapping |
| 5 | Final Bouquet Image | LEVEL 2 image exists and is clean product photography — no text/labels/diagrams |

## Failure mode

The test fails if any of the following fires:

- **Bouquet-only output** — only a bouquet image is produced; no LEVEL 1 Floral Design Board (missing any of the eight parts)
- **No final bouquet image** — only a design board is produced; LEVEL 2 is missing
- **Literal copying** — the translation maps image objects directly to flowers (e.g. *blue sky → blue flowers*) instead of passing through design language
- **Text in the final image** — the LEVEL 2 visualization contains text, infographic, tables, labels, diagrams, or color palettes
- **Unquantified BOM** — a BOM item without an exact quantity, or missing a valid flower status
- **BOM before Reality Check** — the BOM is written before the four reality checks are answered
