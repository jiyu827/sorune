# Signature Look Library

> **Status: DRAFT v1 (Claude-drafted from Sorune architecture). Reconcile against the prototype.**
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`. Sorune
> shows **complete looks, not modular garments** (Master: "Use complete looks. Not modular garments.").

## Purpose

Defines how Body Shape + Colour Season + Face Styling combine into a small set of
**complete, named signature looks** for each user — the headline output of the
Blueprint. A signature look is a full outfit concept (silhouette + palette +
styling), not a single item.

## What a signature look contains

Each look is a bundle:

- **Name** — short, memorable (e.g. "The Modern Minimalist", "Soft Tailoring", "Easy Elegance").
- **Occasion / mood** — where it's worn (Everyday, Work, Event, Off-duty).
- **Silhouette** — the shape recipe from `Body_Shape_System.md` (e.g. defined waist + straight leg).
- **Palette** — colours drawn from the user's Colour Season (`Colour_System.md`).
- **Face styling** — the earrings/necklace/hair/sunglasses notes from the face system.
- **Hero pieces** — the 3–5 garments that build the look, each with its tier.
- **Why it works** — one line of educational copy.
- **Image** — a complete-look image per `50_IMAGES/Image_Bible.md`.

## How looks are generated

1. **Pull the user's profile:** Body Shape, Colour Season, Face Styling variables.
2. **Select silhouettes** that are Top Pick / Best Styles for the shape.
3. **Apply the season palette** to those silhouettes (core + neutral + one accent).
4. **Layer face styling** so accessories and hair match the face system.
5. **Assemble 3–5 hero pieces** that form a coherent, wearable outfit.
6. **Rank** the looks Modern → Stylish → Flattering and label confidence.

## The signature look set

Each user receives a curated set (suggested **4–6 looks**) spanning their core
occasions, so the Blueprint reads as a small, confident capsule rather than an
endless catalogue ("Fewer Better Choices").

Suggested coverage:

| Look slot | Purpose |
|---|---|
| Everyday | The most-worn, easy default. |
| Elevated Everyday | Same ease, dressed up. |
| Work / Smart | Polished, structured. |
| Event | Statement / occasion. |
| Off-duty | Relaxed, weekend. |
| (Optional) Seasonal | Weather/season-specific. |

> [Confirm the exact number and slot names against the prototype.]

## Consistency rules

- A look must not contain a **Style With Care** item in a way that contradicts the
  shape goal unless the adjustment is shown.
- Palette must stay within the user's Colour Season (one accent maximum from an
  adjacent season is acceptable; log if the prototype allows more).
- Face styling in the look must match the face library; no metal/colour that the
  Colour System flags against.
- Conflicts resolve via the engine's Conflict Resolution Rules.

## How this feeds the engine and Blueprint

The Recommendation Engine builds these looks and the Blueprint presents them as
the user's headline result, with individual garment, colour and face
recommendations available underneath each look.
