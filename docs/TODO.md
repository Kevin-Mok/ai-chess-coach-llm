# TODO (Expanded)

This document expands the shorthand items in `todo.md` into actionable tasks.

## Assumptions

1. `refactor script` refers to cleanup of the analysis entrypoint flow (`scripts/analyze_game.sh`) and any closely related CLI glue in `analyze_pgn.py`.
2. The `--ollama-max-tokens: command not found` error came from running a multiline command in `fish` where the flag line was interpreted as a separate command.
3. `use Gemini API` means adding Gemini as an optional `forensic-llm` rewrite backend, not replacing existing local backends.

## Priority

1. Fix shell command UX around `--ollama-max-tokens`.
2. Refactor script logic with no behavior regressions.
3. Add Gemini backend as an opt-in path.

## 1) Refactor script

Scope focus:
- `scripts/analyze_game.sh`
- Any minimal `analyze_pgn.py` argument plumbing required by the refactor

Tasks:
- Separate path resolution, output-path mapping, and command assembly into clearly named helper blocks/functions.
- Keep current behavior for:
  - Exact file paths
  - Relative repo paths
  - Name-only game lookup
  - `games/scratch-games/**` to `analysis/scratch-games/**` mapping
- Improve failure output for ambiguous or missing matches.
- Add or update usage examples to show common invocation patterns.

Acceptance criteria:
- Existing command examples still work.
- Output markdown path mapping remains unchanged.
- Script remains pass-through for extra analyzer args.
- No regressions in scratch-game routing behavior.

## 2) Fix `--ollama-max-tokens` fish-shell error

Observed note from `todo.md`:
- `fix --ollama-max-tokens: command not found`
- `fish: --ollama-max-tokens 120`

Likely cause:
- A multiline command was entered without line continuation, so `fish` tried to execute `--ollama-max-tokens` as a standalone command.

Tasks:
- Add shell-safe command examples (single-line first, multiline second) in docs where this flag is shown.
- Ensure multiline examples include explicit continuation syntax.
- Prefer `scripts/analyze_game.sh ... [extra args]` examples so users avoid long manual commands.
- Add a short troubleshooting note: if shell prints `command not found` on a flag, the previous line likely did not continue.

Acceptance criteria:
- A documented example works in `fish` without triggering `command not found`.
- `--ollama-max-tokens` is shown in at least one verified invocation pattern.

## 3) Use Gemini API (optional backend)

Goal:
- Support Gemini as another rewrite backend for `--cause-mode forensic-llm`.

Implementation outline:
- Extend `--llm-backend` choices to include `gemini`.
- Add Gemini config inputs (API key, model, timeout, token budget) with sensible defaults.
- Implement Gemini rewrite call with strict JSON output handling to match current rewrite contract.
- Preserve deterministic fallback text when Gemini is unavailable or fails.
- Keep existing backends (`ollama`, `llama-cli`, `auto`) working unchanged.

Docs and ops:
- Document required secrets/env vars and example commands.
- Clarify backend selection order and fallback behavior.
- Note network dependency tradeoff versus local-only inference.

Acceptance criteria:
- `forensic-llm` works with `--llm-backend gemini` when credentials are present.
- Failures fall back to deterministic forensic output without crashing analysis.
- Existing Ollama and llama-cli flows still pass.

## Suggested execution sequence

1. Ship fish-shell/docs fix first (lowest risk, immediate usability).
2. Refactor script with behavior-preserving checks.
3. Add Gemini backend behind explicit opt-in and document setup.
