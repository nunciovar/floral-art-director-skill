# Pressure Tests

These scenarios are intended to catch common failure modes before deployment.

## Test 1 — Impossible color pressure
**Input:** A neon cyan cyberpunk poster.

**Failure to catch:** Inventing naturally cyan peonies or roses.

**Expected behavior:** Use natural white/blue-purple flowers where possible; assign cyan primarily to translucent wrapping, ribbon, acrylic, or restrained dyed material; label dyed flowers explicitly.

## Test 2 — Literal-object copying
**Input:** A painting of a red boat on a gray sea.

**Failure to catch:** Adding a miniature boat prop by default.

**Expected behavior:** Translate red boat → concentrated focal red; gray sea → cool foliage / wrapping; horizontal calm composition → low, extended bouquet geometry.

## Test 3 — Exact-count hallucination
**Input:** User requests a render and BOM.

**Failure to catch:** Claiming the generated picture visibly contains exactly the BOM stem counts.

**Expected behavior:** Treat BOM as procurement truth and rendering as visualization only.

## Test 4 — Seasonal flower
**Input:** User reference strongly suggests peonies outside typical local season.

**Failure to catch:** Provide peonies with no warning or substitute.

**Expected behavior:** Flag seasonality and give at least one usable substitute such as garden rose or ranunculus depending on aesthetic role.

## Test 5 — Decoration overload
**Input:** Dreamy image with butterflies, water, glitter, and feathers.

**Failure to catch:** Add every decorative cue literally.

**Expected behavior:** Select only one or two supporting materials and preserve floral hierarchy.

## Test 6 — Dark reference
**Input:** Nearly black album cover with a tiny amber light.

**Failure to catch:** Produce an all-black bouquet using unrealistic dyed flowers.

**Expected behavior:** Use deep burgundy, chocolate, plum, dark foliage, smoky translucent wrapping, and a tiny amber/gold focal accent while preserving buildability.

## Pass criteria
A response passes when it:
- gives all four required sections;
- uses real/sourceable botanical materials;
- quantifies every BOM item;
- separates BOM truth from render appearance;
- provides substitutions for strongly seasonal material;
- preserves palette hierarchy rather than merely matching colors;
- produces a render brief consistent with the concept and BOM.
