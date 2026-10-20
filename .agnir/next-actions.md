# Next Actions

1. Decide how to resolve the divergence between the fork (`1574695`) and upstream (`c0fa866`):
   - (a) Merge upstream into the fork, then let bot commits resume; or
   - (b) Disable `JSON Build, API Check & Encoding` on the fork so only Fork-sync runs, and accept that generated files will differ from upstream; or
   - (c) Keep both and accept Fork-sync failures.
2. Fix `origin` to use the `github-account-2` SSH alias (or a matching remote URL) so plain `git push` works.
3. Review Actions run history periodically; the Fork-sync workflow prunes old runs.
