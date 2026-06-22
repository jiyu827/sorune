# Quiz and AI Content

> **Status: DRAFT v1 (Claude-consolidated from Quiz v3 + Quiz/UI-Flow v2). Reconcile against the prototype.**
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.
> Defines the onboarding quiz, the AI extraction step, and the content/output structure.

## Onboarding model

Photo-led with a short validation quiz:

> Face Photo → Body Photo → AI Analysis → Validation Questions → Results

The quiz **confirms and disambiguates** the AI reads (it does not replace them)
and captures preferences the photo can't show (occasions, comfort, goals).

## AI extraction (what the analysis reads)

**From the face photo** → the five hidden variables:
Face Shape · Face Size · Feature Scale · Feature Sharpness · Facial Contrast.

**From the face photo (colour)** → Colour Season signals: undertone, value, chroma
→ one of 12 seasons (`20_SYSTEMS/Colour_System.md`).

**From the body photo** → Body Shape: one of 5 shapes (`20_SYSTEMS/Body_Shape_System.md`).

## Validation questions (the quiz)

Short, plain-language, one idea per screen. Purpose: resolve borderline AI reads
and capture preference. Suggested blocks:

1. **Body confirm** — e.g. "Where do you feel you carry weight / want balance?" (confirms shape when borderline).
2. **Colour confirm** — e.g. reaction to warm vs cool swatches (confirms undertone/contrast).
3. **Face confirm** — light confirmation of jaw/feature read if uncertain.
4. **Preferences** — occasions you dress for; comfort vs. statement; coverage preferences.
5. **Goals** — what "feeling stylish" means to you.

Each answer can **nudge** a variable or set a preference weight; it should not
override a high-confidence AI read unless the user explicitly contradicts it.

## AI content generation (outputs)

The engine then generates:

- **Signature looks** (4–6 complete looks).
- **Per-category recommendations** (body, colour, face) with tiers.
- **Educational copy** — short, warm, confidence-building "why it works" lines.
- **Image specifications** — complete-look briefs (`50_IMAGES/`).

## Output structure (data the app stores)

A single user **Profile** object feeding the engine (see
`30_ENGINEERING/Technical_Architecture.md` for the schema):

- `bodyShape`
- `colourSeason`
- `faceStyling { faceShape, faceSize, featureScale, featureSharpness, facialContrast, earrings, necklaces, sunglasses, hairStyling, hairColour, hatsAndAccessories }`
- `preferences { occasions, comfortVsStatement, coverage, goals }`
- `confidence { perVariable }`

## Tone of all copy

Warm, plain, editorial, confidence-first. Guidance over rules. No jargon shown to
the user; the science stays behind the scenes.

## Open items to confirm against the prototype

- Exact question wording and order already used in the prototype.
- How answers are weighted against AI confidence.
