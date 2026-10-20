# Decisions

## D1: Fork source
Fork of `hafrey1/LunaTV-config`. Upstream is tracked via `git pull` / Fork-sync.

## D2: Push identity
Pushes to `jaytantech3000/LunaTV-config` use the `github-account-2` SSH host (`id_ed25519_github_jaytantech`). The default `github.com` host uses `mattamior` and lacks write access.

## D3: Enable Fork-sync, leave build workflow on
Fork-sync was enabled and run manually to sync `main` to upstream `0eb7355`. The JSON Build workflow was enabled by the Principal; it is not yet manually verified.

## D4: Agnir adoption
Agnir `v1.0.2` (`repository-filesystem/1.0`) installed for this Project. Entry point: `AGENTS.md` → `AGNIR.md` → `AGNIR.yaml` → `.agnir/`.

## D5: Fork divergence from generated files (open)
Fork-sync failed on the scheduled run because the fork's bot commits (`4ca2d76`, `1574695`) and upstream's bot commit (`c0fa866`) diverge. Resolution is pending the Principal's choice (see next-actions.md, item 1). No merge was performed.

## D6: origin uses github-account-2 alias
`origin` is set to `git@github-account-2:jaytantech3000/LunaTV-config.git` so plain `git fetch` and `git push` use the `id_ed25519_github_jaytantech` key. Replaces the default `github.com` host (`mattamior`, no write access).
