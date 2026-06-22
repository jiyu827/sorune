# Colour System

> **Status: DRAFT v1 (Claude-drafted, needs Jiyu's review).** No source document
> existed for this; this first version is built to be consistent with the
> Master Context Prompt, Blueprint Architecture, and Recommendation Engine,
> which all reference a **twelve-season Colour Season** model with palettes,
> metals, and combinations. Confirm or correct the bracketed assumptions, then
> log a decision in `02_Architecture_Change_Log.md`.
>
> **Scope:** this is the *styling* colour system — how Sorune determines the
> colours that suit the **user**. It is NOT the app's brand palette (Ivory,
> Stone, Taupe, Charcoal, Black, Sage), which lives in
> `15_BRAND/Design_System.md`.

## Role in the Blueprint

Colour Season is one of the five layers of the Complete Style Blueprint:

> Body Shape + **Colour Season** + Face Styling + Signature Looks + Style Personality (Future)

It supplies the colour intelligence the Recommendation Engine uses when it
selects and ranks garments, metals, and complete looks.

## The Twelve Seasons

Sorune uses a twelve-season model: the four classic seasons, each split into
three by the dominant characteristic (light / true / deep, or soft / bright).

| Season family | Sub-seasons |
|---|---|
| Spring | Light Spring · True (Warm) Spring · Bright (Clear) Spring |
| Summer | Light Summer · True (Cool) Summer · Soft Summer |
| Autumn | Soft Autumn · True (Warm) Autumn · Deep Autumn |
| Winter | Bright (Clear) Winter · True (Cool) Winter · Deep Winter |

> [Confirm these twelve names — this is the standard 12-season set; adjust if
> Sorune uses different labels.]

## How a user's season is determined

From the AI photo analysis plus validation questions, Sorune reads three
dimensions and maps them to a season:

1. **Undertone** — warm / cool / neutral.
2. **Value** — how light or deep the natural colouring is.
3. **Chroma** — how soft/muted or bright/clear the colouring is.

These align with the **Facial Contrast** variable already captured in the Face
Styling engine, so contrast feeds both systems consistently.

> [Confirm the exact inputs and how validation questions resolve borderline cases.]

## What each season defines

For every season, the system holds:

- **Palette** — the set of flattering colours (core, accent, and neutral groups).
- **Metals** — recommended metal tones (e.g. gold / silver / rose / mixed).
- **Combinations** — colour pairings and "wear together" guidance.
- **Use with care** — colours to limit or avoid for that season.

> [Populate the actual palettes, metals, and combinations per season, or link to
> a palette library file if one is created.]

## How Colour feeds the Recommendation Engine

Colour Season is an input to the engine alongside Body Shape and Face Styling.
Per the engine's rules:

- Recommendations are prioritised **Modern → Stylish → Flattering** (never the reverse).
- Outputs use the standard tiers: **Top Pick · Best Styles · Style With Care · Your Choice**.
- When Colour and another layer disagree (e.g. Body Shape prefers A, Colour
  prefers B), resolution follows the Conflict Resolution Rules in
  `10_PRODUCT/Recommendation_Engine.md`.

## Open questions to resolve

- Confirm the twelve season names and any Sorune-specific labels.
- Define the exact palette, metals, and combinations for each season.
- Confirm how undertone/value/chroma are scored from the photo + validation answers.
- Decide whether palettes live here or in a dedicated palette library file.
