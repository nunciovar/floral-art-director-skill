# Floral Reality Check Test

## Objective

Evaluate whether the skill can distinguish **visual color from real flower availability**. The skill must run its Floral Reality Check before writing the BOM, and must never let an image's impossible appearance dictate an impossible BOM.

## Input

A fantasy reference image containing:

- impossible blue flowers (highly saturated, luminous blue blossoms)
- transparent petals (see-through, crystalline flower structure)
- glowing elements (self-luminous flowers, sparkle particles, halos)

The user asks for a bouquet "like this magical image."

No budget, size, or recipient is given (defaults: medium budget, medium-size gift bouquet).

## Expected

**Correct behavior:**

- **Color Feasibility:** the impossible blue is classified honestly — a natural blue-violet flower (e.g. delphinium, iris, hydrangea) as the *approximation*, the saturated remainder carried by wrapping and material, and **use dyed flowers only if necessary** — any genuinely essential blue flower is a real variety explicitly specified as `染色花材` (dyed) and labeled as such.
- **Material Translation:** the skill must **translate transparency into material** (clear film, frosted wrapping, organza, restrained acrylic), not into "transparent petals"; glow is translated into light-colored focal flowers under controlled light and fine metallic accents, not into glowing plants.
- **Explain limitations:** the design states explicitly what the real world cannot reproduce (self-luminous flowers, see-through petals) and where each effect lives in `flower + material + lighting + composition`.
- **Construction Feasibility:** the resulting bouquet is stable, proportionate, and buildable by a working florist.
- Every BOM item is a real, sourceable variety with a valid `花材状态`.

**Wrong behavior (failure):**

- **Invent impossible flowers** — "luminous blue orchid", "crystal blossom", "glow-petaled rose".
- Treating transparency as a flower color instead of a material quality.
- Writing a BOM before running the Reality Check, or relying on the rendered image to make an unbuildable design believable.
