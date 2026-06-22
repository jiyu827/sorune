Sorune Governance Rules v1
==========================

Defines source-of-truth hierarchy, change control process, audits and document ownership.

---

## Operating Rules for AIs (added — apply to ChatGPT and Claude)

1. **The repo is the source of truth.** If it isn't committed here, it isn't real.
2. **One file per topic — never duplicate.** Edit the existing file and commit. GitHub's "History" keeps every past version; never make `_v2`/`_final` copies.
3. **Log decisions before changing docs.** Any change to `10_PRODUCT/`, `15_BRAND/`, `20_SYSTEMS/`, or `30_ENGINEERING/` must first get a numbered entry in `00_SOURCE_OF_TRUTH/02_Architecture_Change_Log.md`, then the affected doc is updated to match (ideally same commit).
4. **Conflict hierarchy:** `01_Master_Context_Prompt.md` > `02_Architecture_Change_Log.md` > everything else.
5. **Lanes:** ChatGPT owns architecture & decisions; Claude owns implementation. Either may read anything; each writes mainly in its own lane.
6. **Commit messages say what and why** (e.g. "Decision 007: lock body categories; update Body_Shape_System").
7. **Rough ideas go in `99_WORKING_NOTES/`** until promoted via a logged decision.
