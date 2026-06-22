# Recommendation Engine

> **Status: DRAFT v1 (Claude-drafted, replaces the outline/prompt). Reconcile against the prototype** — the prototype's actual logic wins; update and log differences.
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`. This is the AI brain of Sorune.

## Executive summary

The Recommendation Engine is the intelligence layer that turns a user's profile
(Body Shape + Colour Season + Face Styling) into ranked, confident, complete-look
recommendations. It does not redesign the architecture; it applies the systems
docs and the Sorune philosophy.

## Recommendation philosophy

- **Clarity Over Complexity** — few, clear answers, not exhaustive option lists.
- **Guidance Over Rules** — explain, don't dictate.
- **Confidence Over Fashion** — make the user feel sure, not trend-chased.
- **Fewer Better Choices** — curate down, never overwhelm.

## Inputs

| Input | Source doc | Values |
|---|---|---|
| Body Shape | `20_SYSTEMS/Body_Shape_System.md` | 5 shapes |
| Colour Season | `20_SYSTEMS/Colour_System.md` | 12 seasons |
| Face Styling | `20_SYSTEMS/Face_Styling_System.md` | 5 hidden variables |

## Output tiers

Every recommendation is labelled with one tier:

- **Top Pick** — the single best choice.
- **Best Styles** — reliably strong options.
- **Style With Care** — workable with a stated adjustment.
- **Your Choice** — neutral; preference only.

## Recommendation hierarchy (priority order)

Always rank by: **1. Modern → 2. Stylish → 3. Flattering.**
Never invert to Flattering-first. "Flattering" is the floor, not the goal.

## Recommendation structure

For each result the engine returns:

1. **User Formula** — plain-language reason ("Defined waist + cool palette + soft features").
2. **Styling Specification** — the concrete garment/accessory guidance + tier.
3. **Image Specification** — the complete-look image brief (`50_IMAGES/Image_Bible.md`).

## Per-domain logic

- **Body Shape logic:** look up (shape × category) in the Body Shape System; assign tier; prefer Top Pick / Best Styles silhouettes.
- **Colour logic:** filter to the user's season palette; choose core + neutral + one accent; set metals from the season.
- **Face Styling logic:** map the 5 variables to the six categories via the Face Styling Library.
- **Signature Look logic:** combine the above into 4–6 complete looks (`20_SYSTEMS/Signature_Look_Library.md`).

## Conflict Resolution Rules

When inputs disagree, resolve in this order:

1. **Safety of fit/shape goal first** — never recommend something that defeats the shape's Start-Here priority.
2. **Body Shape silhouette outranks Colour** for garment *cut*; **Colour outranks Body** for *colour/metal*.
3. **Face Styling governs accessories/hair**; it yields to Colour on colour/metal.
4. If still tied, choose the option that ranks higher on Modern → Stylish → Flattering.
5. If an option would be **Style With Care** on one axis and **Top Pick** on another, surface it with the adjustment note rather than dropping it.

Worked example: *Body Shape prefers a structured shoulder (Pear, to balance hips) but Face Styling prefers soft shoulders (soft features).* → Garment cut follows Body Shape (structured shoulder, to meet the shape goal); softness is reintroduced through face styling and neckline, not by overriding the silhouette.

## Verdict logic

For a given item the engine returns **Yes / With Adjustments / No**:
- **Yes** — Top Pick or Best Styles on all relevant axes.
- **With Adjustments** — Style With Care on one axis; show the adjustment.
- **No** — works against the shape goal with no reasonable adjustment.

## Compare logic

When ranking items against each other: sort by tier, then Modern → Stylish →
Flattering, then Colour-season fit, then confidence.

## Confidence rules

- **High** — variables clearly determined; recommendation strong on all axes.
- **Medium** — one variable borderline, or one axis Style With Care.
- **Low** — variables uncertain (poor photo / unresolved validation); prompt the user or widen guidance.

## Future expansion (must inherit this engine)

Shopping Assistant, Wardrobe Planner, Beauty Blueprint, Outfit Builder, Travel
Packing all consume the same profile and tiers — no parallel logic.

## Open items to confirm against the prototype

- Exact conflict-resolution order if the prototype already encodes one.
- Whether verdicts are shown per-item, per-look, or both.
- The exact confidence thresholds.
