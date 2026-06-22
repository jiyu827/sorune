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
