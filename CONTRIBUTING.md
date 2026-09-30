# Contributing to CuevikFlow

## Review flow

- Every change lands through a pull request (PR) from a branch off `main`.
- A change is final only when its PR is merged to `main`. Unmerged branches are drafts.

## Commit convention

Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`, `ci:`.

- Format: `<type>: <imperative summary>` — e.g. `docs: add PRD.md (Step-03)`.
- One logical change per commit.

## Direct-push rule

- Never push directly to `main`.
- Never force-push to a shared branch.

<!-- BEGIN INITIATION-ONLY -->
## Initiation branching & self-review gate

This section governs producing the project initiation documents. It is removed when initiation completes (Step-09).

### Branch naming

Initiation work uses `init/<step>` branches:

| Step | Branch |
| ---- | ------ |
| 01 Repo setup | `init/repo-setup` |
| 02 Product concept | `init/product` |
| 03 PRD | `init/prd` |
| 04 Architecture | `init/architecture` |
| 05 Tech stack | `init/techstack` |
| 06 AI tool guide | `init/aitoolguide` |
| 07 README | `init/readme` |
| 08 Backlog | `init/backlog` |
| 09 Finalize governance | `init/finalize` |

### Branch-per-step

- One branch per initiation step, created from the latest `main`.
- `main` holds only finalized, merged documents.

### Self-review gate

This project is solo and process-enforced: one person holds both the Product Owner and Architect roles, and no second reviewer blocks the merge. Before merging any `init/*` PR, the author confirms:

- [ ] At least a few hours — ideally a full day — have passed since writing the document (fresh-eyes pass).
- [ ] The document covers every section the step guide requires.
- [ ] No upstream document changed after this branch was created.
- [ ] A PR was opened — no direct push to `main`.

Copy this checklist into the PR description and tick every item before merging.
<!-- END INITIATION-ONLY -->
