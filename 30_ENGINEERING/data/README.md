# Engine Data (machine-readable styling rules)

Structured versions of the styling "brain" for the app/engine to read directly,
instead of parsing prose. Source of truth for the *logic* remains the `20_SYSTEMS/`
and `10_PRODUCT/` docs; these JSON files are the operational encoding.

- `body_shapes.json` — per shape: summary, start-here priorities, and per-garment
  recommendations tagged with tier (Top Pick / Best Styles / Style With Care / Your Choice). From `20_SYSTEMS/Body_Shape_System.md`.
- `recommendation_config.json` — tiers, the Modern>Stylish>Flattering hierarchy,
  verdict logic, confidence levels and conflict-resolution rules. From `10_PRODUCT/Recommendation_Engine.md`.

**Status: DRAFT v1 — reconcile against the prototype's real data shapes; the prototype wins.**
Still to encode: `colour_seasons.json` (12 seasons + palettes/metals) and
`face_styling.json` (5 variables → six categories).
