# Test 02 — Impossible Flower / Fantasy Art

## Test Objective

Verify that fantasy or dreamlike imagery is **translated**, not **copied**. When the reference contains elements that have no botanical counterpart — glowing spores, crystal blossoms, alien flora — the agent must re-express those elements through **material, wrapping, and lighting**, and must never invent a plant species that does not exist.

## Input Scenario

A reference image with strong fantasy elements: a luminous forest at night with glowing bioluminescent flowers, drifting sparkle particles, translucent crystal-like petals, and soft fog. The user asks for a bouquet "capturing this magical forest feeling."

No budget, size, or recipient is given (defaults: medium budget, medium-size gift bouquet).

## Expected Behavior

- The design names **only real, sourceable flowers and foliage**. No fabricated species, no "glow-flower", no invented variety names.
- Each fantasy element is mapped onto a real-world floral or material equivalent:
  - *Glowing blossoms* → light-colored focal flowers with high-lumen presence (white, cream, pale green) under controlled light.
  - *Crystal translucency* → clear acrylic stems, glass vials, transparent film, organza, or ice-toned frosted wrapping.
  - *Sparkles / particles* → restrained metallic wire, tiny seed accents, or luminous pearl spray — **sparingly**.
  - *Fog / atmosphere* → soft grey-green foliage, gypsophila, limonium, layered translucent wrapping.
- Every BOM item is a real variety with a real color and an exact quantity.
- The design would hold together as a buildable bouquet even with the fantasy reference removed.

## Failure Mode

- ❌ **Creating a plant that does not exist** — e.g. "bioluminescent orchid", "iridescent astrantia", "frost lotus".
- ❌ Turning pictured fantasy objects into literal floral props (a glowing crystal placed in the bouquet as the concept).
- ❌ Decoration overload: glitter, feathers, and acrylic all at once with no floral hierarchy.
- ❌ Relying on the rendered image to make the design believable while the BOM itself is not buildable.
