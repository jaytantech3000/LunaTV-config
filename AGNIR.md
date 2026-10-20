# Agnir Project Instructions

This file is the canonical Executor-facing activation and Project-operation surface for this Agnir-enabled Project. It is Project content, not Agnir Core state and not a replacement for `AGNIR.yaml` or `.agnir/` durable continuity.

## Activation

1. **Enter through the authorized Project Entry Point.** Treat this repository root as the boundary for discovery. Do not search neighboring Projects or guess another root.
2. **Discover.** Read top-level `AGNIR.yaml`. Validate the declared Core/profile compatibility (`agnir.version: "1.0"`, `repository-filesystem/1.0`), the Project identity, and the selected logical Continuity Lineage.
3. **Load.** Load Current State and Next Actions from `.agnir/`. Load Decisions and Evidence when they materially constrain the operation. Prefer durable Project truth over private conversational memory unless superseded by a newer Principal instruction or directly observed Project fact.
4. **Work.** Perform the actual Project task outside Agnir Core. The root `SKILL.md` of the Agnir distribution is the canonical procedure for install, migration, upgrade, or repair.

## Checkpoint

At an intentional checkpoint, save-progress, finish, or repository commit boundary:

1. reconcile Project truth, not a transcript;
2. classify only material continuity changes for the selected lineage;
3. if durable truth is unchanged, the checkpoint evaluation is a no-op;
4. if material truth changed, construct the complete coherent checkpoint candidate before publication;
5. reject stale-base publication with `AGNIR_CHECKPOINT_CONFLICT`, then re-resolve and reconcile instead of overwriting newer truth;
6. fresh-resolve the same Project identity and selected lineage after publication so a fresh Executor can resume.

A checkpoint boundary requires **checkpoint evaluation**, not forced mutation of `.agnir/`. Never manufacture State or Evidence changes merely to make a commit contain Agnir files.

## Repository operations

Interpret repository intent by context rather than global string matching.

- `commit`, `提交`, or `提交代码` in repository context means: **checkpoint evaluation → Project-defined pre-commit policy when declared → commit**.
- `commit and push` or `提交推送` means: **checkpoint evaluation → Project-defined pre-commit policy when declared → commit → push → verify the actual destination ref**.
- Do not execute an isolated Git commit path that bypasses checkpoint evaluation in an Agnir-enabled Project.
- Prefer one coherent VCS revision for Project changes and any material Agnir checkpoint changes. A legitimate checkpoint no-op does not require an `.agnir/` diff.

Project-defined verification commands belong to the Project's operation policy; they are not Agnir Core checkpoint semantics.

## Compatibility locator

`README.md#Agnir-Project-Instructions` is a backward-compatible locator that points to this file.
