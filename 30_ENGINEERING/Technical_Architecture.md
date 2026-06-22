# Technical Architecture

> **Status: DRAFT v1 (Claude-proposed schemas). ⚠️ Reconcile with the prototype's real data shapes** before treating as canonical.
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`.

## Profile schema (proposed)

```json
{
  "userId": "string",
  "bodyShape": "Hourglass | Pear | Inverted Triangle | Rectangle | Apple",
  "colourSeason": "one of 12 seasons",
  "faceStyling": {
    "faceShape": "Oval | Round | Square | Heart | Oblong | Diamond",
    "faceSize": "Small | Medium | Large",
    "featureScale": "Delicate | Medium | Bold",
    "featureSharpness": "Soft | Blended | Sharp",
    "facialContrast": "Low | Medium | High"
  },
  "preferences": {
    "occasions": ["Everyday","Work","Event","Off-duty"],
    "comfortVsStatement": "0..1",
    "coverage": "string",
    "goals": "string"
  },
  "confidence": { "bodyShape": "High|Medium|Low", "colourSeason": "...", "faceStyling": "..." }
}
```

## Recommendation schema (proposed)

```json
{
  "type": "garment | colour | faceStyling | look",
  "category": "string",
  "tier": "Top Pick | Best Styles | Style With Care | Your Choice",
  "verdict": "Yes | With Adjustments | No",
  "userFormula": "string",
  "stylingSpec": "string",
  "imageSpec": "string",
  "confidence": "High | Medium | Low"
}
```

## Signature look schema (proposed)

```json
{
  "name": "string",
  "occasion": "string",
  "silhouette": "string",
  "palette": ["hex"],
  "faceStyling": "string",
  "heroPieces": [{ "item": "string", "tier": "string" }],
  "whyItWorks": "string",
  "imageRef": "string"
}
```

## API contracts (proposed)

- `POST /analyze` — { facePhoto, bodyPhoto } → Profile (with confidence).
- `POST /validate` — { profileId, answers } → updated Profile.
- `GET /blueprint/:profileId` — → { looks[], recommendations[] }.
- `GET /item-verdict` — { profileId, item } → recommendation.

## Persistence & image schemas

- **Persistence:** Profile, Blueprint results (cacheable), preferences. Minimise stored photo data.
- **Image schema:** look images keyed by `imageRef`, generated/curated per `50_IMAGES/`.

## AI workflow

Photos → vision analysis → variables → engine → looks/recommendations →
image specs → store. Validation answers re-run the engine cheaply (engine is
stateless).

## Open items to confirm against the prototype

- Real field names/types the prototype already uses (align this schema to them).
- Database choice and auth model.
