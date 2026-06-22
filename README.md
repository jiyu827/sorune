# Sorune

The single source of truth for the Sorune styling app. All product, brand,
system, and engineering documentation lives here. GitHub keeps the full version
history, so we never duplicate files or make "v2" copies — we edit and commit.

## Read this first (humans and AIs)

Before generating or changing anything, read these in order:

1. `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`
2. `00_SOURCE_OF_TRUTH/02_Architecture_Change_Log.md`
3. `00_SOURCE_OF_TRUTH/03_Governance_Rules.md`

These override every other document.

## Conflict hierarchy

If two documents disagree, the higher one wins:

> Master Context Prompt  >  Architecture Change Log  >  everything else

## Folder map

| Folder | What lives here |
|---|---|
| `00_SOURCE_OF_TRUTH/` | The rules and the running log of every decision. Highest authority. |
| `10_PRODUCT/` | What we're building and why (blueprint, recommendation engine, quiz/AI content). |
| `15_BRAND/` | Brand guidelines and design system / visual identity (incl. the app colour palette). |
| `20_SYSTEMS/` | The styling logic (body shape, colour, face styling, look libraries). |
| `30_ENGINEERING/` | How it's built (architecture, technical spec, implementation plan, UX/screen spec). |
| `40_AUDITS/` | Checks that docs and prototype actually match. |
| `50_IMAGES/` | Image guidelines ("bibles"). Keep actual image files reasonably sized. |
| `99_WORKING_NOTES/` | Scratch space for half-baked ideas and AI drafts. Not authoritative. |
| `prototype/` | Working prototype files. |
| `_ARCHIVE/` | Superseded versions and pre-rebrand files. Kept for history, not authoritative. |

## Who does what

- **ChatGPT** — architecture and decisions. Proposes and records changes.
- **Claude** — implementation. Turns recorded decisions into the build.
- Both work *from* this repo and commit *back* to it. The repo is their shared memory.

## Golden rule

No change to a `10_/15_/20_/30_` document without a matching entry in
`00_SOURCE_OF_TRUTH/02_Architecture_Change_Log.md` first.
