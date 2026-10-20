# Next Actions

1. Decide how to resolve the divergence between the fork (`f8ab407`) and upstream (`c0fa866`):
   - (a) Merge upstream into the fork, then let bot commits resume; or
   - (b) Disable `JSON Build, API Check & Encoding` on the fork so only Fork-sync runs, and accept that generated files will differ from upstream; or
   - (c) Keep both and accept Fork-sync failures.
2. Review Actions run history periodically; the Fork-sync workflow prunes old runs.
