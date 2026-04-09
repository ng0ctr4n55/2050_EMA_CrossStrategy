# Repository Guidelines

## Project Structure & Module Organization
This repository is a flat collection of TradingView Pine Script files stored at the repo root. Strategy scripts include `2050EMA.pine` and `LT01_Strategy.pine`; indicator scripts include `SuperTrend_EMA.pine`, `Trendilo_lt.pine`, and `BB_20EMA_150EMA.pine`. Reference material lives in `README.md`, and `CLAUDE.md` documents project-specific coding patterns. There is no `src/`, `tests/`, or asset directory, so keep new Pine files in the root unless the structure is intentionally expanded.

## Build, Test, and Development Commands
There is no local build pipeline. Development is done by editing `.pine` files and validating them in TradingView.

- `rg --files` lists all scripts quickly from the repo root.
- `git diff` reviews pending Pine changes before sharing them.
- `git log --oneline -5` checks recent commit style and naming patterns.

Manual validation workflow:
1. Open TradingView Pine Editor.
2. Paste the updated script from this repository.
3. Save, add it to a chart, and check compiler output.
4. For strategy files, open Strategy Tester and verify entries, exits, and alerts.

## Coding Style & Naming Conventions
Use Pine Script v6 for all scripts and keep the MPL 2.0 license header at the top. Follow the existing script order: inputs, calculations, signal conditions, plots, alerts, then strategy logic where applicable. Prefer descriptive `snake_case` names for inputs and calculated series such as `ema_fast_len` or `long_cond`. Keep indentation consistent within a file; use aligned wrapped arguments for long `strategy()` or `indicator()` calls. Add brief section comments only where they improve scanability.

## Testing Guidelines
There is no automated test suite in this repository. Every change should be validated manually in TradingView on the intended timeframe and symbol. When updating a strategy, confirm chart signals, Strategy Tester results, and any `alertcondition()` behavior. If a script enforces a timeframe, such as weekly use in `2050EMA.pine`, verify that the runtime guard still behaves correctly.

## Commit & Pull Request Guidelines
Recent commits use short, direct subjects such as `Update LT01_Strategy.pine`, `update scripts`, and `add price above 9EMA`. Keep commits focused on one script or one behavior change, and use an imperative summary. Pull requests should state which Pine file changed, what trading logic was altered, how it was validated in TradingView, and include screenshots only when chart output materially changed.
