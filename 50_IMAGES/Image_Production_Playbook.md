# Image Production Playbook

> **Purpose:** produce ALL of Sorune's styling images as one cohesive, premium,
> timeless editorial set — photoreal, never "AI", never trashy — affordably.
> Companion to `Image_Bible.md` (the *what*); this is the *how*.
> **Golden rule:** every image must look like the same shoot, with the same small cast of models. Consistency beats any single striking image.

## 1. Faces — yes, with a consistent cast (revised)

We are **not** going faceless. For a personal-styling product, customers expect to
see real, aspirational, human looks — and the face-styling formulas (earrings,
hair, etc.) literally need faces. Headless everywhere would feel cold and, frankly,
a bit creepy.

Instead we use a **small cast of recurring "house models"** — like a real brand's
lookbook. Modern tools can lock one identity across an entire library (see §2), so
the same few faces appear throughout and everything feels intentional and human.

- **A small, diverse cast** (suggested 3–5 identities across ages, skin tones and
  body types) so users see themselves and the brand reads inclusive.
- The **same locked identities** are reused for body looks AND face styling, so the
  whole app feels like one world.
- Headless / cropped shots are fine as an *occasional* editorial device, not the rule.

## 2. Tool choice (revised — consistency first)

Because we now need the **same faces repeated** across a whole library, the priority
shifts from "prettiest single image" to "locks identity + style + commercially safe
+ affordable." On that basis:

- **Primary (production library): an identity-locking model — Nano Banana Pro or Seedream.**
  Nano Banana Pro locks a character from reference images and keeps it consistent
  across poses/angles, with a clean, literal, commercial-friendly look and built-in
  content authentication. Seedream's "universal reference" keeps characters and
  brand assets consistent across generations at low cost — built for exactly this.
- **Optional (aesthetic exploration / hero moodboards): Midjourney.** Best *default*
  taste, but its character reference **drifts** on new poses/angles and it auto-adds
  cinematic flair — great for finding the look, weaker for a consistent library.
- **Commercial licensing:** confirm the licence of whatever you pick before shipping.
  Identity tools accessed via fal (Nano Banana) and licensed-data models (Firefly,
  FLUX) are the safer commercial routes. Don't skip this.

Practical path: optionally use Midjourney to *define* the look, then build the
**production library in Nano Banana Pro or Seedream** with locked identities.

## 3. The consistency system (apply ALL, every image)

1. **Locked Style Core** — a fixed prompt block (lighting, lens, grade, palette,
   background, mood), pasted on every prompt, never edited. See §4.
2. **Locked identities** — the same reference images for each house model, reused
   everywhere (this is the feature the chosen tool must do well).
3. **Fixed parameters** — same aspect ratio (4:5), realism settings, every time.
4. **Fixed background** — same seamless pale porcelain/cool-grey studio backdrop.
5. **One post-grade preset** — run every final through the same light colour-grade
   tuned to the cool-neutral palette. The final unifier.

If an image breaks any lock, it doesn't enter the library.

## 4. Prompt template

**Variable part:** `editorial photograph of [HOUSE MODEL NAME/REF] wearing [OUTFIT + silhouette from Body_Shape_System], [pose/framing]`

**Locked Style Core (every prompt, never edit):**
`editorial fashion photography, soft natural daylight, muted cool-neutral colour grade, seamless pale porcelain-grey studio background, minimal refined styling, calm timeless mood, quiet-luxury aesthetic (The Row, Toteme, COS), fine fabric detail, generous negative space, 85mm, photorealistic`

Keep aspect 4:5, realism-leaning settings, and the model's locked reference attached.

## 5. How many images — be generous, but structured

You're paying a subscription, so the *generation* is effectively free at the
margin — so yes, generate plenty. But the real cost isn't compute, it's **your
curation time** (every image must be vetted to hold the "never looks AI" bar) and
**consistency risk** (more images = more chances to drift). So:

- **Be generous *within* a deliberate structure** — many variations per look, all
  the look slots you want, several house models. A rich library is good.
- **Don't generate the blind full matrix** (body × season × category × style =
  thousands). It adds curation/management burden with **no UX payoff**, because
  **colour is delivered by each user's palette + text, not a unique photo per season.**
- Sensible launch target: **3–5 house models × 5 body-shape looks × 4 slots**
  (Everyday · Elevated · Work · Event), generate 6–8 variations each, keep the best
  1–2. That's a generous but curatable library, not an unmanageable dump.

Rule of thumb: generate freely, **keep ruthlessly.** Quantity is cheap; a sloppy
library is expensive.

## 6. Keeping cost low

- **Flat-rate subscription / unlimited tier** rather than pay-per-image, so volume
  is one predictable cost. *(Check current plan prices before subscribing.)*
- **Lock style + identities first** so you stop re-rolling for consistency.
- **Scope discipline** (§5) — generous within structure, not the infinite matrix.
- One focused batch session: lock models + style → run looks → curate → grade.

## 7. Curation rubric — reject if ANY of these

Plastic/waxy skin · warped hands or jewellery · garbled text/logos on garments ·
uncanny or inconsistent faces (must match the locked model) · lighting/background/
grade that doesn't match the set · anything that reads "AI" for even a second.
Generate many, keep few — a large reject pile means it's working.

## 8. Library naming & handoff

`model_bodyshape_lookslot_variant.jpg` → e.g. `maya_hourglass_everyday_01.jpg`.
Keep originals + graded versions. These feed `Signature_Look_Library.md` and the
Recommendation Engine's "Image Specification".

## 9. Do-this-now: the pilot

1. Pick the production tool (Nano Banana Pro or Seedream) and a flat-rate plan.
2. Create **one** house model: lock its reference images / identity.
3. With the Style Core, generate **one look** (e.g. Hourglass — Everyday) ~8 times
   with that locked identity.
4. Curate to the best 1–2; apply the colour-grade preset.
5. Judge hard: consistent face? never looks AI? on-brand and timeless? If yes →
   add the rest of the cast and scale. If no → adjust Style Core wording and re-test
   before scaling.

One model + one look proves the whole pipeline for almost nothing.
