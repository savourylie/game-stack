# GAME PROJECT SOLO PRACTICAL MODE

Use this mode if the full system feels too heavy.

This is the beginner-first operating mode. It keeps the smallest structure that still prevents chaos.

## 1. Hard Rule

Use the same canonical files from [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md).

Do not create both:

- `VISION.md` and `01_VISION.md`
- `GAME_LOOP.md` and `03_GAME_LOOP.md`
- `VERTICAL_SLICE.md` and `13_VERTICAL_SLICE.md`

The friendly names below are shorthand only.

## 2. Active Working Set

Keep only these five documents active during day-to-day work:

1. `VISION.md` -> `docs/01_vision/01_VISION.md`
2. `GAME_LOOP.md` -> `docs/02_design/03_GAME_LOOP.md`
3. `VERTICAL_SLICE.md` -> `docs/05_production/13_VERTICAL_SLICE.md`
4. `TASK_BOARD.md` -> `docs/05_production/15_TASK_BOARD.md`
5. `DEV_LOG.md` -> `docs/05_production/DEV_LOG.md`

Everything else is supporting reference material that you pull in only when needed.

## 3. What Each Active Doc Does

### VISION.md

Owns:

- the one-sentence concept
- the player fantasy
- the design pillars
- the MVP proof goal
- the non-goals

Use it when:

- a new feature idea appears
- you are unsure whether the game is drifting

### GAME_LOOP.md

Owns:

- what the player does moment to moment
- what the short loop is
- what the long-session hook is
- what feedback makes the loop readable

Use it when:

- a mechanic feels vague
- the game is technically working but not satisfying

### VERTICAL_SLICE.md

Owns:

- the current playable target
- what is required for the slice
- what is out of scope
- what counts as done

Use it when:

- deciding weekly priorities
- deciding what to cut
- checking whether a new idea belongs now or later

### TASK_BOARD.md

Owns:

- what to do next
- what is blocked
- what has been delayed

Use it as a simple board, not a project-management hobby.

### DEV_LOG.md

Owns:

- what happened today
- what got finished
- what got blocked
- what new ideas appeared
- where to resume next session

Use it to reduce restart friction and false memory.

## 4. Weekly Workflow

### Monday - Decide

- re-read `VERTICAL_SLICE.md`
- choose one main outcome for the week
- choose up to three supporting tasks
- cut anything non-essential

### During the Week - Build

For each session:

1. Re-read `VERTICAL_SLICE.md`.
2. Choose one task only.
3. Ask AI for help only on that task.
4. Integrate and test immediately.
5. Log the result in `DEV_LOG.md`.

### Friday - Review

Ask:

- what actually moved the slice forward?
- what was fake progress?
- what should be cut?
- what should become a reusable prompt, template, or workflow?

## 5. Session Loop

At the start of a session:

- choose one main task
- choose one backup task
- define what done means today

At the end of a session:

- log progress
- note blockers
- capture new ideas
- update the task board

## 6. Starter Task Board Format

Use this exact structure first:

```md
# Task Board

## This Week
- [ ]
- [ ]
- [ ]

## Next
- [ ]
- [ ]

## Blocked
- [ ]

## Later
- [ ]

## Done
- [x]
```

Task rule:

- each task starts with a verb
- each task produces one visible result

Good examples:

- Implement dialogue box with speaker name and choices
- Draft 3 NPC cards for the slice area
- Create placeholder background for the first street

Bad examples:

- Work on dialogue
- Think about the story
- Improve atmosphere

## 7. Solo Decision Filter

Whenever a new idea appears:

1. Classify it: system, story, world, asset, workflow, or research.
2. Ask whether it helps the current slice.
3. Decide whether it is a doc update or a task.
4. Ask whether it can be finished in one session.
5. If not, split it or move it to `Later`.

## 8. Internal Slice First

As a solo beginner, aim for the internal proof gate first.

That means:

- the slice plays end-to-end
- the main loop is clear
- the biggest system risk is proved
- the core content supports honest evaluation

Do not delay completion because the slice is not yet marketing-ready.

## 9. When to Graduate to the Full System

Move beyond Solo Practical Mode when one of these becomes true:

- the project has enough content that canon is drifting
- you need dedicated world, story, or asset docs
- your task board needs more than one level of organization
- your AI workflow needs explicit review and prompt tracking
- playtesting reveals recurring production or clarity problems

At that point, keep the same canonical files and add structure from:

- [GAME_PROJECT_FULL_SYSTEM.md](GAME_PROJECT_FULL_SYSTEM.md)
- [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md)

## 10. Default Beginner Rule

If you are unsure whether to add more process, do not.

Only add the next layer of structure when the current project creates a real, repeated problem.
