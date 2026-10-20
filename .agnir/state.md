# Current State

Project: lunatv-config (lineage: lunatv-config-main)

- Fork of `hafrey1/LunaTV-config` at `jaytantech3000/LunaTV-config`.
- Local and `origin/main` at `1574695` (fork-only bot commits on top of `0eb7355`).
- Upstream `hafrey1/LunaTV-config` main is at `c0fa866`, one bot commit ahead of `0eb7355`. The fork and upstream have diverged on generated files, so a fast-forward Fork-sync is not possible.
- Workflows in the fork:
  - `Fork-sync` (daily 01:00 CST + manual): enabled. Manual run succeeded at `0eb7355`. Scheduled run on `4ca2d76` failed (non-fast-forward after the fork's own bot commits).
  - `JSON Build, API Check & Encoding` (daily 01:00 CST, push to `LunaTV-config.json`, manual): enabled. Manual run succeeded at `0eb7355`. Scheduled run succeeded at `4ca2d76`, pushing `4ca2d76` and `1574695`.
  - `Deploy to GitHub Pages`: enabled.
- Deployed proxy: `https://luna.sub.hkcu.cc.cd/` (verified reachable; returns valid JSON/Base58).
- Git push to the fork requires SSH host alias `git@github-account-2` (key `id_ed25519_github_jaytantech`). Default `origin` uses `mattamior` key and is denied.
