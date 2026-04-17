# GAME PROJECT SYSTEM

This doc set defines a practical, AI-assisted workflow for a solo developer making a finishable game project.

This file is intentionally short. It is the index, reading order, and boundary map for the rest of the methodology. Detailed rules live in the linked docs below.

## Start Here

- New to game development or feeling overwhelmed: read [GAME_PROJECT_SOLO_PRACTICAL_MODE.md](GAME_PROJECT_SOLO_PRACTICAL_MODE.md)
- Want the complete production methodology: read [GAME_PROJECT_FULL_SYSTEM.md](GAME_PROJECT_FULL_SYSTEM.md)
- Need the canonical folder structure and document schemas: read [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md)
- Want to design focused AI helpers for this workflow: read [GAME_PROJECT_SKILL_CREATION.md](GAME_PROJECT_SKILL_CREATION.md)

## Doc Boundaries

- `GAME_PROJECT_SYSTEM.md`
  - Purpose: index only
  - Owns: reading order, document boundaries, migration note
- `GAME_PROJECT_FULL_SYSTEM.md`
  - Purpose: the full methodology
  - Owns: phase model, operating rules, AI usage model, scope rules, production basics, tool roles
- `GAME_PROJECT_TEMPLATES.md`
  - Purpose: canonical project structure and document schemas
  - Owns: folder layout, filenames, required sections for each canonical doc
- `GAME_PROJECT_SOLO_PRACTICAL_MODE.md`
  - Purpose: the lightweight working mode for one person
  - Owns: minimal active-doc set, weekly loop, decision filter, task-board starter format
- `GAME_PROJECT_SKILL_CREATION.md`
  - Purpose: design AI skills that fit this system
  - Owns: skill boundaries, build order, design template, review rules

## Shared Invariants

- One canonical source per topic.
- Finish a vertical slice before expanding into the full game.
- Exploratory artifacts are not real until merged into canonical docs or the source repo.
- AI generates candidates and drafts; humans approve canon.

## Recommended Beginner Path

1. Read [GAME_PROJECT_SOLO_PRACTICAL_MODE.md](GAME_PROJECT_SOLO_PRACTICAL_MODE.md).
2. Create the five active working docs using the canonical file paths from [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md).
3. Build a placeholder-first prototype that proves the core loop.
4. Pull in additional templates only when a real production problem appears.
5. Move to the full system when the project has enough complexity to justify it.

## Naming Rule

Solo Practical Mode uses friendly names such as `VISION.md` and `TASK_BOARD.md` as shorthand only. Do not create parallel duplicate files. The real source-of-truth filenames remain the canonical paths defined in [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md).

## Migration Note

The previous monolithic `GAME_PROJECT_SYSTEM.md` has been split into orthogonal docs so that:

- system rules change in one place
- document schemas change in one place
- solo workflow changes in one place
- skill-design rules change in one place

If you are updating the methodology, change the owning document above rather than duplicating the edit across the whole set.
