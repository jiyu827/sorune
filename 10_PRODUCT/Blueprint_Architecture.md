# Style Blueprint Architecture

> **Status: DRAFT v1 (Claude-expanded from the v2 outline). Reconcile against the prototype.**
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.

## What the Blueprint is

The Style Blueprint is the user's complete, personalised styling result — the
core product. It is assembled from five layers and presented as a small set of
signature looks plus the guidance behind them.

## The five layers

> Body Shape **+** Colour Season **+** Face Styling **+** Signature Looks **+** Style Personality *(future)* **= Complete Style Blueprint**

| Layer | Produces | System doc |
|---|---|---|
| Body Shape | Silhouette guidance across garment categories | `20_SYSTEMS/Body_Shape_System.md` |
| Colour Season | Palette, metals, combinations | `20_SYSTEMS/Colour_System.md` |
| Face Styling | Earrings, necklaces, sunglasses, hair styling, hair colour, hats & accessories | `20_SYSTEMS/Face_Styling_System.md` |
| Signature Looks | 4–6 complete named looks | `20_SYSTEMS/Signature_Look_Library.md` |
| Style Personality | (Future) tone/aesthetic preference layer | TBD |

## Face Styling engine (inputs → output)

> Face Shape + Face Size + Feature Scale + Feature Sharpness + Facial Contrast → Face Styling Recommendations

Outputs the six user-facing face categories. Variables are hidden; users see only
finished recommendations.

## User journey (photo-led + quiz)

Per the agreed MVP scope (face photo **and** body photo **plus** quiz):

1. **Welcome** — set expectations, privacy note on photos.
2. **Face Photo** — capture/upload; AI reads the five face variables.
3. **Body Photo** — capture/upload; AI reads body shape.
4. **AI Analysis** — derive Body Shape, Colour Season, Face Styling variables.
5. **Validation Questions** — short quiz to confirm/disambiguate the AI reads and capture preferences.
6. **Blueprint Generation** — engine builds looks + recommendations.
7. **Explore Results** — user browses looks, items, and the guidance behind them.

## How the Blueprint is presented

- **Headline:** the signature looks (complete-look imagery, names, why-it-works).
- **Beneath each look:** the contributing Body / Colour / Face recommendations with tiers.
- **Explore:** deeper guidance per category; verdicts on items (Yes / With Adjustments / No).

## Output naming (consistent everywhere)

Top Pick · Best Styles · Style With Care · Your Choice.

## Open items to confirm against the prototype

- Exact screen order and whether validation questions are per-layer or one block.
- How much of the "hidden variables" (if any) is ever surfaced.
- Whether Style Personality is in MVP or deferred.
