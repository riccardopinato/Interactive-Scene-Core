# Changelog
## 2026-11-11 — Snapshot workflow merge identity fixed (CI validated)
- Live Agent Core [rerun #43040897071](https://github.com/riccardopinato/App-Factory-Agent-Core/actions/runs/43040897071) found a shared workflow defect: `git merge --no-edit` could run before `git config user.name/user.email`, producing `Committer identity unknown` when the base advanced.
- Fixed the same snapshot workflow on this repository using [PR #4](https://github.com/riccardopinato/Interactive-Scene-Core/pull/4), keeping metadata-only PR workflow, daily cron and `workflow_dispatch` unchanged. The fix is **CI_VERIFIED, NOT independently RUNTIME_VERIFIED** on this repository.
- In the Agent Core donor, [real run #43052705998](https://github.com/riccardopinato/App-Factory-Agent-Core/actions/runs/43052705998) confirmed successful branch merge after the fix; the separate GitHub Actions create-PR admin setting remains blocked there. No product implementation, financial trading, renderer, or Golden promotion.

## 2026-11-11 — Knowledge bootstrap
- Added scope, Product Bible, stage-gated roadmap, consumer file inventory, conceptual Schema-2 contract, license/Deskland GPL reference-only rules, QA matrix and provenance.
- Added automatic snapshot of GitHub upstream SHAs via scheduled PR-only workflow, no renderer code imported.
- No engine release, physical QA or cross-app Donor/Golden certification claimed.
