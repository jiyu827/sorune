# Implementation Plan

> **Status: DRAFT v1 (Claude-proposed). Reconcile with what the prototype already covers** — tick off what's built, focus on the gaps.
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.

## Goal

Turn the prototype + these specs into a working MVP: photo (face + body) + quiz →
Blueprint with signature looks.

## Phases

1. **Encode the styling rules as data.** Convert `20_SYSTEMS/` docs into structured
   config the engine reads (body-shape × category × tier; season palettes; face
   variable → category maps). *Depends on: brain docs (now drafted).*
2. **Body shapes & categories.** Confirm the 5 shapes and the garment category
   list; wire shape → recommendations in the engine.
3. **Colour.** Finalise the 12-season palettes/metals; wire colour logic.
4. **Face styling.** Wire the 5 variables → six categories via the library.
5. **Recommendation engine.** Implement tiers, hierarchy, verdicts, conflict rules.
6. **Signature looks.** Assemble 4–6 complete looks per profile.
7. **Onboarding & quiz.** Face/body photo capture + validation questions → Profile.
8. **AI analysis.** Integrate vision reads (or guided self-classification for MVP v1).
9. **Images.** Complete-look imagery per `50_IMAGES/`.
10. **Cleanup & testing.** Reconcile docs ↔ prototype; test the full flow end to end.

## Suggested MVP cut line

If photo-AI vision is heavy: ship **v1** with photo capture + strong guided
validation that sets the variables, full engine, looks, and images. Add automated
vision reads as **v1.1**. (Confirm — the agreed scope includes photo analysis, so
this is a sequencing option, not a scope change.)

## Open items to confirm against the prototype

- Which phases the prototype already completes.
- Whether vision AI ships in MVP or as a fast-follow.
