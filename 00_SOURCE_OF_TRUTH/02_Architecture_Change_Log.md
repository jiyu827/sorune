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
