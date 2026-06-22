# Architecture Change Log

The running record of every locked decision. Newest at the top.
Decisions are never deleted — superseded ones are marked, not removed.

**How to add one:** copy the template, fill it in, give it the next number,
then update any affected docs in the same commit.

---

## Template (copy me)

### Decision NNN — <short title>
- **Date:** YYYY-MM-DD
- **Decided by:** <ChatGPT / Claude / Jiyu>
- **Status:** Active
- **Affects:** <which docs/folders>

**Decision:**
<what was decided>

**Reason:**
<why>

**Supersedes:** <Decision NNN, or "none">

---

## Decision 001 — Repository established as single source of truth
- **Date:** 2026-06-22
- **Decided by:** Jiyu
- **Status:** Active
- **Affects:** whole repo

**Decision:**
All Sorune documentation lives in this repo, converted from the original DOCX
files into Markdown and organised into the numbered structure. Superseded and
pre-rebrand ("Stylist App" / "Kikonasu") files are kept in `_ARCHIVE/` only.

**Reason:**
Replace scattered, conflicting DOCX files with one versioned source both AIs work from.

**Supersedes:** none

---

## Decision 002 — MVP scope: photo (face + body) + quiz
- **Date:** 2026-06-22
- **Decided by:** Jiyu
- **Status:** Active
- **Affects:** 10_PRODUCT/*, 30_ENGINEERING/*

**Decision:**
The MVP onboarding is photo-led with a validation quiz: Face Photo → Body Photo →
AI Analysis → Validation Questions → Results. Photo analysis of both face and body
is in scope (sequencing of automated vision vs. guided validation is an
engineering decision, not a scope change).

**Reason:** Confirmed product direction.

**Supersedes:** none

## Decision 003 — Documentation filled from outlines to working drafts
- **Date:** 2026-06-22
- **Decided by:** Claude (to be reviewed by Jiyu)
- **Status:** Active (pending review)
- **Affects:** 10_PRODUCT/*, 20_SYSTEMS/*, 30_ENGINEERING/*, 50_IMAGES/*

**Decision:**
The previously skeletal docs were filled with real, usable content: Body Shape
System (5 shapes × categories × tiers), Face Styling System + Library, Signature
Look Library, Recommendation Engine logic, Blueprint, Quiz & AI Content, the
engineering/UX drafts, and the image bibles. Every doc carries a "Draft v1 —
reconcile against the prototype" header.

**Reason:** Docs were tables of contents, not specs; the app cannot be built from
outlines.

**Supersedes:** the outline/prompt versions of those files.

## Decision 004 — Prototype is the tie-breaker for build details
- **Date:** 2026-06-22
- **Decided by:** Jiyu
- **Status:** Active
- **Affects:** 30_ENGINEERING/*, 20_SYSTEMS/*

**Decision:**
A clickable prototype already exists. Where a drafted doc and the prototype
disagree on build/logic specifics, the prototype wins; the doc is updated to match
and the change is logged. Prototype screens/exports should be added to `prototype/`.

**Reason:** Align documentation to what is actually built.

**Supersedes:** none

## Decision 005 — Brand palette reset to cool neutral + design ethos
- **Date:** 2026-06-22
- **Decided by:** Jiyu
- **Status:** Active
- **Affects:** 15_BRAND/*, 00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md, 50_IMAGES/*, 20_SYSTEMS/Colour_System.md, 30_ENGINEERING/UX_Screen_Spec.md

**Decision:**
The brand palette changes from warm earth tones (Ivory/Stone/Taupe/Sage) to a cool
neutral system: Porcelain #F4F5F7, Pearl #E7E8EC, Dove #C4C7CF, Slate #6F7480, Ink
#1E2024, with whisper accents Wisteria #D7D5E0 and Mist #CBD6DA. Rationale: Sorune
delivers each user a personal colour analysis, so the brand must be a near-neutral
canvas rather than impose a colour (the "gallery wall, not the painting" principle).
Added design ethos: unique, timeless, feminine, understated, and **never
AI-generated/templated in feel**. Typography (Cormorant Garamond + Inter) retained.

**Reason:** Earth tones clash with cool-toned users and contradict a colour-analysis product; founder is not an earth-tone person.

**Supersedes:** the v1 earth-tone palette in Design_System and references to it.


## Decision 006 — Palette refined for contrast + single signature
- **Date:** 2026-06-22
- **Decided by:** Jiyu
- **Status:** Active
- **Affects:** 15_BRAND/*, 00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md, 50_IMAGES/*, 20_SYSTEMS/Colour_System.md

**Decision:**
The cool-neutral palette is refined to a defined light-to-deep ladder — Porcelain
#F4F5F7, Cloud #DDE0E5, Pewter #9197A1, Graphite #4A4F58, Ink #15171B — with ONE
cool signature accent, Plum #5E4F66 (used sparingly), and a Mist #C7D2D7 whisper.
Replaces the softer v2 set (Pearl/Dove/Slate + Wisteria/Mist) which read washed-out.

**Reason:** Previous palette was too soft/low-contrast; needed a backbone and a confident signature while staying neutral-led.

**Supersedes:** Decision 005's specific colour values (principle and ethos unchanged).
