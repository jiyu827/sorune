# Engineering Architecture

> **Status: DRAFT v1 (Claude-proposed). ⚠️ Must be reconciled with the existing prototype** — replace assumptions below with what the prototype actually uses, then log it.
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.

## Purpose

Canonical engineering architecture for Sorune: how the app is built end to end.

## System architecture (high level)

```
[ Client app ]  →  [ API layer ]  →  [ AI pipeline ]
       │                │                  │
       │                │           Face read (5 vars)
       │                │           Colour read (season)
       │                │           Body read (shape)
       │                ▼
       │        [ Recommendation Engine ]  ← reads Systems docs as rules/data
       │                │
       ▼                ▼
[ Results UI ]   [ Profile + results store ]   →   [ Image layer ]
```

- **Client:** the user-facing app (the existing prototype). [Confirm: web / React / no-code tool.]
- **API layer:** request/response between client, AI pipeline, engine, and storage.
- **AI pipeline:** vision analysis of face + body photos → variables.
- **Recommendation Engine:** pure logic over the profile (`10_PRODUCT/Recommendation_Engine.md`).
- **Storage:** user profile, results, images.
- **Image layer:** complete-look imagery (generated or curated).

## AI pipeline

1. Receive face + body photos.
2. **Face analysis** → Face Shape, Face Size, Feature Scale, Feature Sharpness, Facial Contrast.
3. **Colour analysis** → undertone/value/chroma → 12-season classification.
4. **Body analysis** → 1 of 5 body shapes.
5. Emit a **Profile** with per-variable confidence.
6. Validation answers adjust low-confidence variables.

[Confirm which models/APIs the prototype uses for vision, or whether MVP uses a guided self-classification instead.]

## Recommendation Engine integration

The engine is stateless logic that takes a Profile and returns looks +
recommendations. The styling rules live in the `20_SYSTEMS/` docs and should be
encoded as structured data/config the engine reads — not hard-coded prose.

## Profile schema, API layer, image layer, caching, security, storage

See `Technical_Architecture.md` for the concrete schemas and contracts.
Cross-cutting: cache derived results per profile; secure photo handling (see
Security); store the minimum needed.

## Implementation phases

See `Implementation_Plan.md`.

## Open items to confirm against the prototype

- Actual stack (frontend framework, hosting, database).
- Whether vision AI is live or deferred for MVP.
- Where photos are stored and for how long.
