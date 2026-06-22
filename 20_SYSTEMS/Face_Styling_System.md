# Face Styling System

> **Status: DRAFT v1 (Claude-drafted from Sorune architecture). Reconcile against the prototype.**
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.

## Purpose

Defines the **hidden variables** Sorune reads from the face photo and how they
drive face-styling recommendations. Users never see the raw variables — they see
finished recommendations in the six face-styling categories.

## The five hidden variables (inputs)

Extracted by AI from the face photo, confirmed by validation questions.

| Variable | What it measures | Values |
|---|---|---|
| **Face Shape** | Outline of the face | Oval, Round, Square, Heart, Oblong/Long, Diamond |
| **Face Size** | Overall scale of the face relative to the body/frame | Small, Medium, Large |
| **Feature Scale** | Size of features (eyes, nose, lips) relative to the face | Delicate, Medium, Bold |
| **Feature Sharpness** | Soft/rounded vs. angular/defined features | Soft, Blended, Sharp |
| **Facial Contrast** | Difference between hair, skin, eyes (light↔dark) | Low, Medium, High |

> [Confirm the exact value sets — these are sensible defaults; match the prototype's actual options.]

## The six output categories (what the user sees)

Earrings · Necklaces · Sunglasses · Hair Styling · Hair Colour · Hats & Hair Accessories.

## Core mapping principles

1. **Shape balances shape.** Recommend lines that balance the face shape — e.g.
   soften angular faces, add definition/length to round faces, balance width at
   the jaw or forehead.
2. **Scale matches scale.** Feature Scale and Face Size set the size of accessories:
   delicate features → finer pieces; bold features/large face → larger statement pieces.
3. **Sharpness echoes or softens.** Sharp features can carry geometric/angular
   shapes; soft features suit rounded/organic shapes. Echo for a harmonious look,
   contrast deliberately for a modern edge.
4. **Contrast sets intensity.** High facial contrast carries bold colour and
   strong metal/shape contrast; low contrast suits tonal, blended choices.

## Variable → recommendation logic (summary)

### Face Shape
- **Oval:** balanced — most styles are Best Styles/Your Choice; avoid overwhelming the natural balance.
- **Round:** add length and angle — Top Pick: drop earrings, V/longline necklaces, angular frames; Style With Care: round studs/round frames.
- **Square:** soften the jaw — Top Pick: curved/hoop earrings, rounded frames; Style With Care: sharp geometric pieces near the jaw.
- **Heart:** balance a wider forehead/narrow chin — Top Pick: wider-at-the-bottom earrings (teardrop), rounded frames; Style With Care: top-heavy styles.
- **Oblong/Long:** add width, reduce length — Top Pick: studs/round earrings, wider frames, fuller hairstyles; Style With Care: long drops.
- **Diamond:** soften cheekbones, balance — Top Pick: studs and curved pieces, frames wider than cheekbones.

### Face Size & Feature Scale (accessory sizing)
- Small face / delicate features → fine, smaller-scale pieces (Top Pick).
- Medium → mid-scale; broad latitude (Your Choice).
- Large face / bold features → statement, larger-scale pieces (Top Pick); tiny pieces are Style With Care (they get lost).

### Feature Sharpness
- Soft → rounded, organic shapes (hoops, teardrops, rounded frames).
- Sharp → geometric, angular shapes (studs, rectangular frames).
- Blended → either; lead with Stylish/Modern preference.

### Facial Contrast (colour & metal intensity)
- High → bold colours, high-contrast metals/stones welcome.
- Medium → mid-intensity; broad latitude.
- Low → tonal, blended colours; avoid harsh contrast.

## How this feeds the engine

The engine combines the variables, looks up the per-category recommendations in
`Face_Styling_Recommendation_Library.md`, applies the tier language, and merges
with Body Shape and Colour Season per `10_PRODUCT/Recommendation_Engine.md`.

## Open items to confirm against the prototype

- Exact value sets per variable and how validation questions resolve ties.
- Whether hair recommendations consider current hair length/type as an input.
