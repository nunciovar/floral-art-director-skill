# Floral Art Director — Benchmark Test Suite

This directory is a quality-evaluation system for the Floral Art Director skill. It is not a feature checklist; it is a set of **adversarial scenarios** designed to catch the failure modes that degrade a floral design from *buildable floristry* into *pretty but fake rendering*.

## How to run

For each numbered test:

1. Feed the **Input Scenario** to the skill as the user prompt (the reference image is described textually; use any equivalent real image with the same visual language).
2. Run the skill end-to-end (all four output sections: Style DNA → Floral Design Concept → Flower BOM → Image Generation Brief).
3. Score the response against **Expected Behavior**.
4. If the response exhibits any item under **Failure Mode**, the test fails — record which failure mode(s) fired.

## Test inventory

| # | Scenario | Failure mode targeted |
|---|---|---|
| 01 | Color overfitting (blue-dominant reference) | Inventing impossible flower colors to match the image |
| 02 | Fantasy art (dreamlike, non-realistic imagery) | Creating plants that do not exist |
| 03 | Seasonal flower (peony out of season) | Omitting substitutes for seasonal material |
| 04 | Minimal style (quiet, sparse reference) | Over-stuffing the bouquet with flowers |
| 05 | Luxury style (dark, gold-tinged reference) | Using cheap decorative clutter instead of quality |

## Shared pass criteria

A response passes *any* test only when it satisfies **all** of these:

- Produces the four required sections **in the fixed order**: ① Style DNA, ② Floral Design Concept, ③ Flower BOM, ④ Image Generation Brief.
- Uses only real, sourceable botanical material — **no invented varieties**.
- Every BOM item is quantified with an exact stem count or quantity.
- Rare or hard-to-source colors are handled through **materials first** (foliage, wrapping, ribbon, translucent film, restrained decoration), then dyed flowers only as a last resort, and dyed material is explicitly labeled `染色花材`.
- Seasonal material carries **at least one usable substitute**.
- The palette hierarchy of the reference is *preserved*, not merely color-matched.
- The render brief is consistent with the BOM and design concept — render is visualization only; **BOM is procurement truth**.
- The design would work as real floristry **without** the reference image.

## Scoring

| Level | Meaning |
|---|---|
| PASS | Meets all Expected Behavior points; zero failure modes fired |
| PARTIAL | Meets Expected Behavior but with one minor, non-structural deviation |
| FAIL | Any Failure Mode point fired |

## Purpose

These tests exist to keep the skill honest. The core principle under test:

> **The bouquet must first work as real floristry, and only then resemble the reference image.**
