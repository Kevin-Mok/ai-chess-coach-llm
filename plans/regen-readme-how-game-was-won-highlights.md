# ExecPlan: Regenerate README From How The Game Was Won

## Goal
Refresh the win-focused parts of `README.md` so they are derived from current decisive-game analysis artifacts, while preserving the existing recruiter/tooling content and structure.

## Assumptions
1. The highlight source of truth is each winning `analysis/*.md` file's `## How The Game Was Won` section, merged with PGN metadata.
2. Loss artifacts stay excluded from README highlight narrative content.
3. The 2026-03-13 Chess.com win should use a derived live-game URL based on the tracked analysis URL because that was explicitly chosen during planning.

## Plan
- [x] Patch `README.md` to explain the highlight-source rule and rebuild win-focused sections from all current SoloPistol wins.
- [x] Refresh `docs/RECRUITER_REPO_IDEAS.md` because the next cadence refresh is due.
- [x] Verify the README structure, move references, opponent coverage, and updated docs diff.

## Review
- Rebuilt the README win-summary bullets, highlight table, key move list, and study/artifact links from the current winning PGNs plus each matching `## How The Game Was Won` section.
- Added the missing 2026-03-06 and 2026-03-13 wins to the highlight inventory while keeping the existing recruiter/tooling sections and `## Next goals` intact.
- Refreshed `docs/RECRUITER_REPO_IDEAS.md` with five new repo ideas that satisfy the current naming and about-text constraints.
- Verification:
  - `rg -n "^## (Overview|SWE Recruiter View|AI Tooling Stack|Local Analysis Pipeline|Chess Improvement View|Highlight Games|Key Moves and Turning Points|High Win% Comeback Evidence|Study/Analysis Links|How to View the Games|Next goals)$" README.md`
  - `rg -n "Woaheee|gaju33333|AmeerIrfan|juliok22|NickGen_Eral|Abhijeetnegi123" README.md`
  - `rg -n "Qxe7#|Qxc7|Rc2|Re1#|Qfh4#|Qxf7#" README.md`
  - `awk '/^About:/{getline; print length($0) "\t" $0}' docs/RECRUITER_REPO_IDEAS.md`
  - `curl -sSI https://www.chess.com/game/live/165901228132`
  - `git diff -- README.md docs/RECRUITER_REPO_IDEAS.md plans/regen-readme-how-game-was-won-highlights.md`
