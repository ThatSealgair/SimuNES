# Contributing Guide: NES Emulator

## Branching Strategy

- **main** (or **master**):
Contains production-ready, stable code. All releases and finished features are merged here.
- **dev**:
Integration branch where new features and fixes are merged before they’re ready for main. Regularly updated.
- **feature branches**:
For developing new components or large changes.
Naming: `feature/<component>` (e.g., `feature/cpu-core`, `feature/ppu`, `feature/apu`, `feature/mapper-support`)
- **bugfix branches**:
For fixing specific issues/bugs.
Naming: `bugfix/<description>` (e.g., `bugfix/ppu-render-crash`)

---

## Pull Request (PR) Workflow

1. **Sync first:**
    - Before starting new work, always `pull` the latest changes from `dev` and rebase or merge to keep your branch up to date.
2. **Make atomic commits:**
    - Commit only logically related changes. Each commit message should be meaningful and descriptive (e.g., "Implement 6502 addressing modes for CPU").
3. **Push to your branch:**
    - Push your local feature/bugfix branch to the remote repository.
4. **Open a Pull Request:**
    - Target PRs against the **dev** branch.
    - PR title: Summarize the feature/component (e.g., "Add core CPU emulation logic").
    - PR description: Explain:
        - What component/area is affected (CPU, PPU, Controller, etc.)
        - Key changes or architecture notes
        - Any tests or ROMs used
5. **Checklist before requesting review:**
    - Code compiles and passes project tests
    - New/changed code is documented or commented if necessary
    - No unrelated or "misc" changes included
6. **Tag reviewers:**
    - Assign relevant maintainers or teammates for review, especially those owning related components.
7. **Address feedback:**
    - Tidy up your branch with additional commits (or rebase if requested)
    - Mark conversations as resolved and summarize major decisions in the PR
8. **Merging:**
    - PRs are merged to `dev` after review and successful tests.
    - If there are conflicts, resolve them in your branch before merging.

---

## Component Example

Break your emulator into branches per area:

- `feature/cpu-core`
- `feature/ppu`
- `feature/apu`
- `feature/input`
- `feature/rom-mapper`
- `feature/testing-harness`

---

## Additional Tips

- Avoid working directly on main or dev branches.
- Use clear, standard names for branches and PRs.
- Keep PRs focused: one component or logical change per PR.
- Document tricky or architectural decisions in the PR description or comments.
