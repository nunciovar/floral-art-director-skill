# Test 08 — Presentation Structure (locked output structure, adaptive theme)

Targets the v0.3 **Presentation Structure System**: the output structure is fixed, the visual theme adapts to the reference. The skill must always produce the same information architecture — never a fixed black background, orange-gold accent, or generic PPT style.

## Input scenarios

Run the skill end-to-end with each of these reference types:

- an **album cover** (e.g. La La Land)
- a **painting** (e.g. Van Gogh's *Starry Night*)
- a **photograph** (e.g. a monochrome eye close-up)

Each reference has a different mood, palette, era, and artistic language.

## Expected behavior

Every response contains the seven fixed output components:

- [x] **Style DNA** — 4–7 keywords; dominant/supporting colors, brightness, saturation, temperature, lighting, texture, emotion
- [x] **Visual Translation Logic** — reference element → visual interpretation → floral translation (e.g. *ocean color → calm transparency → blue hydrangea + delphinium*)
- [x] **Floral Reality Check** — color feasibility, material translation, seasonal availability, construction feasibility
- [x] **Flower BOM** — table format `| Flower / Material | Quantity | Color | Role | Status | Substitute |`; real commercially available flowers; exact quantities; dyed flowers identified; seasonal alternatives identified
- [x] **Design Sketch** — florist-style structural sketch (bouquet outline, flower hierarchy, focal flower position, line flower direction, foliage structure, spatial relationship); resembles a florist's design drawing, not an engineering CAD diagram
- [x] **Alternative Angle View** — multiple bouquet views (recommended 2×2: front / 45 degree / side / detail)
- [x] **Final Bouquet** — standalone product image; bouquet only, realistic flower texture, commercial photography quality, independent of the board

The output should feel like a **premium florist proposal / editorial floral design sheet / art direction board** — NOT a generic infographic, business dashboard, or engineering report.

## Theme adaptation checks (must hold across all three inputs)

- The presentation theme is **NOT** forced to a fixed black background.
- The presentation theme is **NOT** forced to a fixed orange-gold accent.
- The presentation theme is **NOT** forced to a fixed typography or decorative style.
- The output does **NOT** look like a generic PPT / business dashboard / engineering report.

The presentation style must **differ per input** and follow each reference's mood, palette, era, and artistic language:

- dark cinematic photo → dark background → dramatic lighting
- pastel painting → soft background → gentle editorial layout
- minimal monochrome → clean monochrome presentation

## Failure mode

The test fails if any of the following fires:

- **Missing component** — any of the seven fixed output components is absent.
- **Theme lock** — all three inputs share the same fixed theme (same background, same accent color, same typography), i.e. the theme was forced instead of adapted.
- **PPT / dashboard / report output** — the response reads as a generic infographic, business dashboard, or engineering report rather than an art direction board.
