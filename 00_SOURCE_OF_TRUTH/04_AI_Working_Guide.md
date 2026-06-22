# AI Working Guide

How ChatGPT and Claude plug into this repo. The repo is always the single
source of truth; the AIs read from it and write back to it.

## The loop

1. Make sure the AI has read: `README.md`, `01_Master_Context_Prompt.md`,
   `02_Architecture_Change_Log.md`, `03_Governance_Rules.md`.
2. Ask for the change.
3. Take the AI's output and save it back into the repo (commit/push).
4. Log any real decision in `02_Architecture_Change_Log.md`.

## Lanes

- **ChatGPT** — architecture and decisions. Proposes changes, records them.
- **Claude** — implementation. Turns decisions into the build.

## ChatGPT setup (Project)

Create a Project named "Sorune" and paste the standing instruction below into
its custom instructions. Upload the four core files above into the Project.
When a core file changes in GitHub, re-upload the new version (the Project copy
is a convenience copy — GitHub is the truth).

### Standing instruction to paste into the ChatGPT Project

> You are working on Sorune, a styling app. The GitHub repo is the single source
> of truth. Before answering, read the provided files, especially the README,
> Master Context Prompt, Architecture Change Log, and Governance Rules — these
> override everything. If documents conflict: Master Context Prompt > Change Log
> > everything else. Your lane is architecture and decisions. When you propose a
> change: (1) write the decision entry for the Change Log, and (2) give the exact
> updated file content I can paste back into GitHub. Never invent new structure
> or rename things without a logged decision. Never create "v2" copies of files —
> give edits to the existing file.

## Keeping them in sync

Both AIs work off the same committed files. There is no live link — freshness
comes from you saving outputs back to the repo and re-sharing updated files.
