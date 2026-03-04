# ExecPlan: Fix 2026-03-03 Comeback Analysis Artifact

## Goal
Regenerate `analysis/2026-03-03-comeback-vs-gaju33333.md` using the current helper script and keep `README.md` evidence in sync.

## Plan
- [x] Run `scripts/analyze_game.sh 2026-03-03-comeback-vs-gaju33333` to regenerate the artifact.
- [x] Validate the markdown is complete (swing block + move table present).
- [x] Update README sections that currently reference the truncated file state.
- [x] Verify final diffs and ensure claims match repository artifacts.

## Review
- Regeneration command completed with output file:
  - `analysis/2026-03-03-comeback-vs-gaju33333.md`
- New artifact now includes:
  - `## Significant Swings` with 6 events
  - Full move table block
- README sync completed:
  - Replaced stale "headers only" note with current swing evidence (`29...Qb8`, expected score `0.87 -> 0.00`).
- Verification checks:
  - `rg -n "^## Significant Swings|^Ply\\s+Turn\\s+Move|^34\\.\\.\\.\\s+me\\s+Qxc7" analysis/2026-03-03-comeback-vs-gaju33333.md`
  - `rg -n "29\\.\\.\\.Qb8|analysis/2026-03-03-comeback-vs-gaju33333\\.md" README.md`
