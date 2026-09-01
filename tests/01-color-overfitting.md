# Test 01 — Color Overfitting

## Test Objective

Verify that a blue-dominant reference image does not push the agent into inventing impossibly colored flowers. The bouquet must keep the image's blue identity while distributing the hard-to-source hue across **natural flowers, foliage, and wrapping material** in the skill's defined priority order.

## Input Scenario

A reference image where electric / royal blue is the **dominant, saturated** color — e.g. a poster or painting with a deep blue field, small white highlights, and cool shadows. The user asks for a bouquet "in the style of this image, keeping the blue."

No budget, size, or recipient is given (defaults: medium budget, medium-size gift bouquet).

## Expected Behavior

- Blue is recognized as **difficult to source naturally** in full saturation.
- The design uses natural blue-violet flowers first (e.g. **blue delphinium, blue/violet hyacinth, bachelor's button, iris, blue hydrangea**) rather than forcing deep blue onto a flower that does not grow blue.
- The bulk of the saturated blue is assigned to **foliage, wrapping, ribbon, or translucent material** (e.g. navy or blue-grey paper, deep blue organza, cool wrapping film) before resorting to dyed flowers.
- If dyed material is used at all, it is **explicitly labeled `染色花材`** and used as a restrained accent, not the whole bouquet.
- The flower palette stays botanically real: the *identity* of the bouquet is blue, but every named flower is a real variety with a real color.
- The BOM table includes quantities, roles, dye status, and substitutes.

## Failure Mode

- ❌ **Inventing an impossible flower color** — e.g. "blue roses", "cyan peonies", "blue lily of the valley" presented as a natural variety with no `染色花材` label.
- ❌ Placing the entire color-matching burden on flowers, leaving no blue in wrapping or foliage.
- ❌ Using dyed flowers as the dominant mass without labeling them.
- ❌ Matching the hex value of the reference literally instead of preserving its visual weight and role.
