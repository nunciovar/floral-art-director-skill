# Test 03 — Seasonal Flower

## Test Objective

Verify that strongly seasonal material is flagged and always accompanied by **at least one usable substitute**. The skill must never hand back a BOM that silently depends on a flower that is out of season at purchase time.

## Input Scenario

A soft romantic reference image (blush pink and ivory, gentle light) that strongly suggests peonies. The user is buying the bouquet "next month" — a time of year when peonies are out of season in their region. The user did not specify a region, so the agent must assume the default market and treat peonies as seasonal.

No budget, size, or recipient is given (defaults: medium budget, medium-size gift bouquet).

## Expected Behavior

- The design may feature peonies (they carry the reference's romantic, full, layered texture) **but** must explicitly flag them as seasonal.
- **At least one substitute is provided for each seasonal item**, matched to its aesthetic role:
  - Full, ruffled focal texture → **garden rose** or **ranunculus**.
  - Voluminous, layered mass → **dahlia**, **double tulip**, or **camellia** depending on the role.
- The substitute keeps the same visual role (focal / mass / transition), not merely the same color.
- The substitution note is part of the **BOM table**, not buried in prose.
- If the seasonality risk is high, the design names the *substitute as the primary* and peonies as the occasional upgrade, so the bouquet stays buildable.

## Failure Mode

- ❌ Listing peonies with **no warning and no substitute**.
- ❌ Substituting a flower that changes the design role (e.g. replacing a focal peony with a filler) without noting it.
- ❌ Providing a substitute only in the render brief while the BOM table remains seasonal-dependent.
- ❌ Asserting year-round availability for a strongly seasonal flower.
