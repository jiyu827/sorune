# Image Production Playbook

> **Purpose:** how to produce ALL of Sorune's styling images so they look like
> one cohesive, premium, timeless editorial shoot — never AI, never trashy — and
> do it cheaply. Companion to `Image_Bible.md` (the *what*) — this is the *how*.
> **Golden rule:** every image must look like it came from the same shoot. Consistency beats any single "wow" image.

## 1. The consistency system (read this first)

Five locks. Use ALL of them on every image. This — not the tool — is what makes 200 images look like one brand.

1. **Locked Style Core.** A fixed block of prompt text appended to *every* prompt (lighting, lens, grade, palette, background, mood). You never change it. See §3.
2. **Locked Style Reference.** In Midjourney, generate once, find a style you love, then reuse its **`--sref` code** (and/or a **moodboard / personalization profile**) on every image forever. This is the single biggest consistency lever and costs nothing extra.
3. **Fixed parameters.** Same aspect ratio, same version, same stylize value, every time (see §3).
4. **Fixed background.** Always the same seamless pale studio backdrop (Porcelain #F4F5F7 / soft cool grey). A constant background instantly unifies a library.
5. **One post-grade preset.** After generating, run every image through the *same* light colour-grade preset (Lightroom/Photoshop/free tools) tuned to the cool-neutral palette. This erases small differences and is the final unifier.

If an image breaks any lock, it doesn't go in the library.

## 2. Tool choice

- **Start / pilot: Midjourney.** Best editorial aesthetic, least "AI" looking, and its **`--sref` + personalization** features are the easiest way to lock one style across a whole library. Web interface, no code.
- **Scale / tighter control: FLUX.2 Pro.** Photoreal, strong reference control, cost-effective at volume.
- **Commercial-safety priority: Adobe Firefly or FLUX** (trained on licensed/clean data — safest to ship commercially). **Confirm the licence terms of whatever you choose before building a library you publish.**
- Recommendation: pilot in Midjourney for the look; if licensing/scale demand it, move the bulk run to FLUX.2 or Firefly using the same Style Core.

## 3. The prompt template (fill in the blanks)

**Variable part (changes per image):**
`[full-length OR cropped] editorial photograph of a woman wearing [OUTFIT: garments + silhouette from Body_Shape_System], [pose/framing]`

**Locked Style Core (paste on EVERY prompt, never edit):**
`editorial fashion photography, soft natural daylight, muted cool-neutral colour grade, seamless pale porcelain-grey studio background, minimal refined styling, calm timeless mood, quiet-luxury aesthetic inspired by The Row, Toteme and COS, fine fabric detail, generous negative space, shot on 85mm, photorealistic`

**Locked parameters (never change):**
`--ar 4:5 --style raw --stylize 150 --sref [YOUR_LOCKED_CODE] --v 7`

> Notes: `--ar 4:5` = portrait for app/social; `--style raw` = less "AI-stylised"; lower `--stylize` keeps it realistic; `--sref` = your locked style code; `--v 7` = use the current Midjourney version. Adjust syntax to the current version if it has changed.

**Worked examples** (silhouettes pulled from `20_SYSTEMS/Body_Shape_System.md`):

- *Hourglass — Everyday:* "cropped editorial photograph of a woman wearing a fitted wrap dress that follows a defined waist, straight relaxed pose, face turned away" + Style Core + params
- *Pear — Work:* "full-length editorial photograph of a woman wearing a structured-shoulder blazer over a column skirt, balanced silhouette, headless crop at the chin" + Style Core + params
- *Rectangle — Elevated Everyday:* "cropped editorial photograph of a woman in a belted shirt dress creating a defined waist, soft daylight" + Style Core + params

## 4. Faces — the rule that saves you

Faces and hands are the AI giveaways and the hardest thing to keep consistent. So for body/look images: **crop them out** — headless, face turned away, or cropped at the chin. This is genuine editorial style (The Row, COS do it constantly), it removes the #1 "AI tell," and it kills the most expensive consistency problem at zero cost.

Face-styling images (earrings, hair) *do* need faces — **handle that category last and separately** (tighter crops of just ear/neck/hair, or licensed imagery). Do not let it hold up the main library.

## 5. Scope for MVP — keep it small and cheap

Do **not** generate the full matrix (body × season × category × style = thousands). You don't need it: **colour is delivered by each user's palette + recommendation text, not a unique photo per season.** So:

- **5 body shapes × 4 look slots** (Everyday · Elevated Everyday · Work · Event) = **20 hero looks**.
- Generate ~6–8 variations each, **keep the best 1–2** → a **~20–40 image** launch library.
- Expand later (Off-duty, more looks) once the pipeline is proven.

That's a tiny, controllable, inexpensive set — not thousands.

## 6. Keeping cost low

- **Use a flat-rate subscription with an unlimited/"relax" generation tier** (Midjourney-style) rather than pay-per-image API billing. For a curated library, a flat monthly fee = effectively unlimited attempts for one predictable cost. *(Check current plan prices before subscribing — they change.)*
- **Scope discipline** (§5) is the real cost control — 30 images, not 3,000.
- **Lock the style first** (§1) so you stop re-rolling for consistency.
- **Cropped framing** (§4) means fewer rejected images (no face/hand glitches to throw away).
- Do a single **batch session**: lock sref → run all 20 looks → curate → grade. One focused sitting.

## 7. Curation rubric — reject if ANY of these

- Plastic/waxy skin or "too perfect" surfaces
- Warped or extra fingers, mangled hands/jewellery
- Garbled text or fake logos on garments
- Unnatural symmetry or an uncanny face (prefer cropped — see §4)
- Lighting, background, or grade that doesn't match the rest of the set
- Anything that makes you think "AI" for even a second

Generate many, keep few. The reject pile should be large — that's the process working.

## 8. Library naming & handoff

Save finals with a consistent name so they map to the app and styling docs:

`bodyshape_lookslot_variant.jpg` → e.g. `hourglass_everyday_01.jpg`, `pear_work_01.jpg`

Store originals + graded versions. These feed `Signature_Look_Library.md` and the Recommendation Engine's "Image Specification".

## 9. Do-this-now: the pilot batch

Before building all 20, prove the look:

1. In Midjourney, run the Style Core with `--sref random` a few times; pick the style you love; **copy and lock that `--sref` code.**
2. Generate **one look for one body shape** (e.g. Hourglass — Everyday) ~8 times with the locked sref.
3. Curate to the best 1–2. Apply your colour-grade preset.
4. Look hard: does it clear "never looks AI, timeless, on-brand"? If yes → scale to all 20. If not → adjust the Style Core wording and re-test (don't scale until the pilot passes).

That pilot is the whole risk, de-risked for the price of one look.
