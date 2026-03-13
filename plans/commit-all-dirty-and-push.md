# ExecPlan: Commit All Dirty Work And Push

## Goal
Commit the current dirty worktree as one coherent documentation/planning change, then push it to `origin main`.

## Assumptions
1. The current branch `main` is the intended target branch.
2. The only intended dirty paths for this batch are:
   - `README.md`
   - `docs/RECRUITER_REPO_IDEAS.md`
   - `plans/regen-readme-how-game-was-won-highlights.md`
3. The refreshed plan file itself should be committed with the batch, since plan files are tracked in this repo.

## Plan
- [x] Recheck the current worktree and confirm the dirty set matches the intended README/docs refresh.
- [x] Inspect the README and recruiter-doc diffs to confirm they belong in one documentation-focused commit.
- [ ] Stage the current dirty files plus this refreshed ExecPlan:
  - `README.md`
  - `docs/RECRUITER_REPO_IDEAS.md`
  - `plans/regen-readme-how-game-was-won-highlights.md`
  - `plans/commit-all-dirty-and-push.md`
- [x] Run pre-commit verification focused on the changed docs:
  - `rg -n "^## (Overview|SWE Recruiter View|AI Tooling Stack|Local Analysis Pipeline|Chess Improvement View|Highlight Games|Key Moves and Turning Points|High Win% Comeback Evidence|Study/Analysis Links|How to View the Games|Next goals)$" README.md`
  - `rg -n "Woaheee|gaju33333|AmeerIrfan|juliok22|NickGen_Eral|Abhijeetnegi123" README.md`
  - `rg -n "Qxe7#|Qxc7|Rc2|Re1#|Qfh4#|Qxf7#" README.md`
  - `awk '/^About:/{getline; print length($0) "\t" $0}' docs/RECRUITER_REPO_IDEAS.md`
  - `git diff -- README.md docs/RECRUITER_REPO_IDEAS.md plans/regen-readme-how-game-was-won-highlights.md plans/commit-all-dirty-and-push.md`
- [ ] Commit once with a conventional message:
  - `docs(readme): refresh win highlights and recruiter repo ideas`
- [ ] Push the commit to `origin main`, per repo policy for successful commits.

## Review
- Current dirty set before refreshing this plan:
  - `README.md`
  - `docs/RECRUITER_REPO_IDEAS.md`
  - `plans/regen-readme-how-game-was-won-highlights.md`
- The README/doc diffs are tightly related: both stem from the recent README regeneration work and recruiter-ideas cadence refresh.
- No code, tests, or analysis artifacts are currently dirty, so splitting this into multiple commits would add churn without improving traceability.
- Verification passed:
  - README required section headings are present.
  - README includes the expected highlighted opponents and SAN finish references.
  - Recruiter repo-idea `About` lines are all under the 160-character limit.
