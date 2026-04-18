---
name: create-vertical-slice
description: >
  Creates the 13_VERTICAL_SLICE.md production planning document (and optionally seeds 15_TASK_BOARD.md) in an Obsidian vault using the GAME_PROJECT_SYSTEM methodology. Use this skill whenever the user runs `/create-vertical-slice <vault-path>`, asks to plan or scope a vertical slice, wants to define their first playable target, is trying to figure out what to actually build first, or says things like "create a vertical slice", "plan my vertical slice", "what should I build first", "I have a vision and a game loop, now what", "scope down to a buildable demo", "cut my game down to something I can finish", "define the slice", "13_VERTICAL_SLICE doc", "I know my game in theory but not what to build", or "I need to cut scope". Even if the user hasn't said "vertical slice" explicitly — if they're trying to convert their vision and loop into one short, finishable, playable section that proves the game and the workflow, use this skill.
user-invocable: true
---

# Create Vertical Slice Document

## What This Is

The vertical slice document (`05_production/13_VERTICAL_SLICE.md`) defines one short playable section that proves both **the game** (the core loop, the systems, the feel) and **the workflow** (the solo + AI production pipeline, end to end). It is not a roadmap and not a feature list. It is the playable target that decides what is in scope right now and what gets deferred.

The slice has two purposes:

- **Internal** — proves the production loop actually works, validates the core game loop in real play, and locks in a creative reference point for the rest of production.
- **External** — when polished, doubles as a standalone asset for cold-player testing, screenshots, trailers, and funding pitches. The internal purpose is required; the external is optional until the internal gate passes.

This skill produces up to two files in `05_production/`:

- **`13_VERTICAL_SLICE.md`** — always created. The scoped definition of the slice: scenario, loop validation, required implementation, layer coverage, workflow proof, and acceptance criteria.
- **`15_TASK_BOARD.md`** — optional, offered after the slice is written. A starter board seeded with the first slice-critical tasks so work can begin the same day.

Keep the slice doc short and ruthless. If something can be deferred, defer it. The slice exists to expose fake scope.

## Step 1: Parse the Vault Path

The user invoked this skill as `/create-vertical-slice <vault-path>`. Extract the vault path from their message. If no path was given, ask for it before continuing:

> "What's the path to your Obsidian vault? (e.g., `~/Vaults/MyGame`)"

Expand `~` to the full home directory path when reading or writing files.

## Step 2: Verify Prerequisites and Read Canon

A vertical slice is only honest when the vision and game loop are already defined. Before starting the interview, check the canon:

- **`<vault>/01_vision/01_VISION.md`** — required. If missing, stop and tell the user to run `/create-vision` first. The slice's "what must this prove" question cannot be answered without the vision's MVP must-prove list.
- **`<vault>/02_design/03_GAME_LOOP.md`** — required. If missing, stop and tell the user to run `/create-game-loop` first. The slice has to validate specific loop and chain claims; without those claims, the slice is just a level.

If both exist, read them silently. Use them as context throughout the interview — reference the player fantasy, the primary loop, the named chains, and the MVP must-prove items to ask sharper questions and catch contradictions. Do not recite the docs back to the user.

Then check for optional context:

- **`<vault>/02_design/04_SYSTEMS.md`** — if it exists, read it. It informs the must-have systems list for the slice.
- **`<vault>/05_production/13_VERTICAL_SLICE.md`** — if it exists, read it and ask whether the user wants to refine the existing slice or replace it. Do not silently overwrite a prior slice.

## Step 3: Interview for the Slice

Your goal is to fill in all sections of the vertical slice template. Do this through a natural conversation, not a form. Move through the interview blocks in order — scope decisions made earlier constrain choices made later. When the user has already answered something implicitly (especially anything already in the vision or game loop), do not re-ask.

If the user gives you everything upfront in a single message — a full description covering scope, loop validation, systems, and acceptance criteria — skip the interview entirely and go straight to writing the file.

### 1. Target Scope & Scenario

Lock the boundaries before discussing anything else. Aim for the smallest scenario that can plausibly prove the game.

- **Duration** — 15 to 30 minutes of play. If the user proposes longer, push back: a 90-minute slice is not a slice, it is a chapter. If shorter than 15 minutes, push back: there is not enough time to demonstrate a real chain or a real arc.
- **Location** — one explorable district, one street cluster, one building, one arena. Not multiple zones.
- **Characters** — 2 to 3 NPCs with meaningful dialogue. Not a full cast.
- **Game-Timeline Position** — this is the most commonly missed rule. The slice must sit at a representative **midpoint** of the game, not the tutorial or the first level. First levels restrict mechanics for teaching reasons; they show what onboarding feels like, not what the real game feels like. Ask the user:
  - Where in the game's progression does this slice sit?
  - What has the player already unlocked by this point — abilities, items, story beats, relationships?
  - Why is this moment representative of the true core loop rather than the training-wheels version of it?

  If the user describes a "level 1" or a "first hour" scenario, push back hard. Suggest jumping to a midpoint and explicitly noting which earlier content is assumed-unlocked.
- **Feature Balance** — aim for roughly 60% genre standards and 40% innovations. Genre standards prove the game is competent; innovations prove why it deserves attention. Have the user enumerate, even loosely:
  - the standard expectations from this genre that the slice will hit
  - the specific innovations or hooks that make this game distinct
- **Narrative & Progression** — exactly:
  - 1 main objective the player pursues during the slice
  - 1 memorable tension event during the slice
  - 1 story reveal that lands inside the slice

  Push for one of each, not three of each. The slice is short.

### 2. Loop & Chain Validation

Tie the slice to specific claims from `03_GAME_LOOP.md`. The slice exists to prove these claims in real play, not in theory.

- **Primary Loop Proof** — which exact second-to-second action will be polished to shipping fidelity in this slice? Reference the primary loop from the game loop doc by name.
- **Cognitive Cycle Test** — which action-feedback loop will the slice prove is readable across visual, audio, and system channels? If the game loop named feedback channels that the slice can't actually implement, surface that as a risk.
- **Chain Demonstration** — which one chain (value, execution, or secret) will the player get to complete inside the 30-minute window? A slice that doesn't resolve at least one chain leaves the player with no payoff.
- **Pacing Proof** — where does the planned moment of rest sit relative to the main tension event? Sketch the rough sequence so the rhythm is visible.

If the user's slice doesn't actually exercise the loops or chains the game loop doc claims are central, that's a red flag — either the slice needs reshaping, or the game loop doc was claiming things the game doesn't really do.

### 3. Required Implementation

Now define only what is strictly necessary to make the scenario playable.

- **Required MVP Systems** — drawn from `04_SYSTEMS.md` if it exists, otherwise drawn from the game loop. List only the systems the slice cannot exist without. If a system is "nice to have" or "would make the slice better," it is out of scope.
- **Required Content & Assets** — art, audio, dialogue files, scripted events. Be concrete and countable. "Some dialogue" is not a content requirement; "12 dialogue lines for Detective Mara, 8 ambient bark lines for street NPCs" is.
- **Out of Scope** — explicit list of features and content the slice will **not** include. Push the user to name at least 5 items, more if the original scope was ambitious. Examples to surface: large talent trees, deep equipment systems, extra locations, side quests, cinematic flourishes, branching dialogue past the slice scenario, save systems, settings menus, alternative endings. Naming what is excluded is more important than naming what is included — it protects the slice from creep.

If the user resists naming out-of-scope items, ask: "What features have you been imagining that you are pretending are part of the slice?" The honest answer is the cut list.

### 4. Layer Coverage ("Slice of Cake")

The slice metaphor is a slice of cake: narrow, but it contains every layer. Inside the slice, no production layer can be missing or clearly temporary. Walk through each of the five layers and confirm the user's intent:

- **Final-quality art** — at least one hero background, character, or key prop rendered at shipping fidelity.
- **Final-quality UI** — HUD, menus, and dialogue UI at shipping fidelity for this slice.
- **Final-quality sound design** — at least one music cue, ambient sound for the location, and key interaction SFX at shipping fidelity.
- **Final-quality mechanics** — the core loop tuned to feel like the shipped game, not a prototype.
- **Final-quality narrative** — writing voice, tone, and pacing at shipping fidelity for this scene, not draft placeholder.

Everything outside the slice can stay placeholder. Inside the slice, no layer is allowed to be missing or obviously temporary. If the user can't commit a layer to shipping fidelity (for example, "I won't have final music in time"), that's allowed but must be recorded as a deferred risk in the doc — not silently skipped.

### 5. Workflow & Pipeline Proof

The slice must also exercise the production pipeline end to end. This is what proves the workflow is real, not just the game.

- **AI Integration** — how AI will be used in producing the slice (dialogue passes, concept art, prototype scaffolding, consistency reviews). Note which AI outputs will pass through human review before becoming canon.
- **Pipeline Steps** — confirm the slice will exercise:
  - asset naming and storage conventions
  - dialogue integration and event scripting
  - the build, test, and review loop
  - the AI output → review → canonical doc path

If the slice plan does not exercise these end-to-end, the slice will only prove the game and not the workflow — which means the next slice will hit the same workflow surprises.

### 6. Acceptance Criteria

Split into two gates. The internal gate is required; the external gate is optional until the internal gate passes.

- **Internal Proof Gate (required)** — what must be true for the slice to count as a production-loop proof? Lean on the user to write these in their own words first, then sharpen for testability. Example shape: "The player can start the game, complete the main objective, experience the story reveal, and hit an end-of-demo screen without game-breaking bugs, with final dialogue and the slice's hero layers at shipping fidelity." If the user writes "feels good" or "is fun," push for a concrete, observable test.
- **External Showcase Gate (optional)** — what would make the slice usable as an external artifact? Offer the standard checklist as a starting point and let the user adjust:
  - plays end-to-end without game-breaking bugs for a cold player
  - at least 3 high-quality screenshots captured at shipping fidelity
  - at least one 30-60 second gameplay video at shipping fidelity
  - ready to send to a curated external playtester list
  - strong enough to anchor a funding pitch or Steam page

Make sure the user understands: do not start polishing for the external gate until the internal gate is real. Beginners burn weeks on screenshots before the slice actually plays.

**Tone:** Be direct. Slice planning fails when the developer is allowed to be vague about scope. If an answer is wishy-washy ("I'll figure that out as I go," "it should feel good"), say so and ask a sharper follow-up. Identify "fake scope" — features the user keeps mentioning that they have not actually committed to building. Naming fake scope and moving it to the cut list is the most valuable thing this skill does.

## Step 4: Write the Vertical Slice File

Once you have enough to fill all sections, write the file to `<vault-path>/05_production/13_VERTICAL_SLICE.md`. Create the `05_production/` directory if it does not exist.

Use this exact template structure:

```md
# Vertical Slice

## 1. Target Scope & Scenario

Keep strictly contained. Do not expand beyond these limits for the slice.

- Exact Duration: [target 15-30 minutes]
- Location: [e.g., one explorable district or street cluster]
- Characters: [2-3 NPCs with meaningful dialogue]

### Game-Timeline Position

This must be a midpoint slice, not a tutorial or first level.

- Where in the game this slice sits:
- What the player has already unlocked by this point (abilities, items, relationships, story beats):
- Why this moment is representative of the true core loop rather than onboarding:

### Feature Balance (≈60/40)

Aim for roughly 60% genre standards and 40% innovations. Genre standards prove competence; innovations prove why this game deserves attention.

Genre Standards included (what players expect from this type of game):
- [Item]
- [Item]

Innovations included (this game's unique hooks):
- [Item]
- [Item]

### Narrative & Progression

- Main Objective:
- Memorable Tension Event:
- Story Reveal:

## 2. Loop & Chain Validation

How this slice tests the claims defined in `03_GAME_LOOP.md`.

### Primary Loop Proof

[The specific second-to-second action that will be polished to shipping fidelity in this slice.]

### Cognitive Cycle Test

[The most important action–feedback loop the slice will prove, and how it will be readable across visual, audio, and system / state channels.]

### Chain Demonstration

[The one specific chain — value, execution, or secret — the player will complete inside the slice's window.]

### Pacing Proof

[Where the planned moment of rest sits relative to the main tension event, and how that rhythm will read to the player.]

## 3. Required Implementation

Only what is strictly necessary to make the scenario playable.

### Required MVP Systems

Drawn from `04_SYSTEMS.md`. Only systems the slice cannot exist without.

- [System]
- [System]

### Required Content & Assets

Art, audio, dialogue files, scripted events. Be concrete and countable.

- [Item]
- [Item]

### Out of Scope (Defer Aggressively)

Features explicitly NOT allowed in this slice — for example large talent trees, deep equipment systems, extra locations, side quests, cinematic flourishes, full save systems.

- [Item]
- [Item]
- [Item]
- [Item]
- [Item]

## 4. Layer Coverage ("Slice of Cake")

The slice must sample every intended final layer of the game. Each layer below must reach shipping fidelity within this window. Anything outside the slice can stay placeholder.

- [ ] **Final-quality art** — [the specific hero asset(s) at shipping fidelity]
- [ ] **Final-quality UI** — [the HUD, menus, and dialogue UI at shipping fidelity for this slice]
- [ ] **Final-quality sound design** — [music cue, ambience, and key interaction SFX at shipping fidelity]
- [ ] **Final-quality mechanics** — [the core loop tuned to feel like the shipped game]
- [ ] **Final-quality narrative** — [writing voice, tone, and pacing at shipping fidelity for this scene]

Deferred layers (named risks):
- [If a layer can't reach shipping fidelity in time, name it here with a one-line reason. If none, write "None."]

## 5. Workflow & Pipeline Proof

This slice must prove the solo + AI production process actually works end to end.

### AI Integration

[How AI will be used here — dialogue passes, concept art, prototype scaffolding, consistency reviews. Note which outputs pass through human review before becoming canon.]

### Pipeline Checklist

This slice must exercise the full workflow.

- [ ] asset naming and storage
- [ ] dialogue integration and event scripting
- [ ] build, test, and review loop
- [ ] AI output → review → canonical doc path

## 6. Acceptance Criteria (Definition of Done)

The exact state this slice must reach to be considered finished. Internal gate is required; external gate is optional until internal passes.

### Internal Proof Gate (required)

[A specific, testable statement of what must be true. Example: "The player can start the game, complete the main objective, experience the story reveal, and hit an end-of-demo screen without game-breaking bugs, with the slice's hero layers at shipping fidelity."]

- [Concrete criterion]
- [Concrete criterion]

### External Showcase Gate (optional)

Do not start polishing for this gate until the internal gate is real.

- [ ] Plays end-to-end without game-breaking bugs for a cold player
- [ ] At least 3 high-quality screenshots captured at shipping fidelity
- [ ] At least one 30-60 second gameplay video at shipping fidelity
- [ ] Ready to send to a curated external playtester list for structured feedback
- [ ] Strong enough to serve as a funding pitch artifact (publisher, Kickstarter, grant)
- [ ] Can anchor a Steam store page and wishlist campaign
```

**Writing rules:**

- Write in plain, declarative prose — no marketing language
- Every section must be filled; nothing blank or left as a placeholder
- Duration must be 15-30 minutes — if longer, the slice is too large and must be cut
- The slice must be a midpoint, not a tutorial — if the user described a "first level" scenario, the Game-Timeline Position section must explicitly state what is assumed-unlocked
- Feature Balance must list at least 2 genre standards and at least 2 innovations
- Out of Scope must have at least 5 items — push for more if the original concept was ambitious
- Layer Coverage checkboxes must each have a one-line plan; an unchecked layer is allowed but must be named in the "Deferred layers" section as a risk, not silently skipped
- Internal Proof Gate criteria must be specific enough to be testable — not "feels good" or "is fun," but "the player can complete X without Y"
- Total document length: aim for 80-160 lines. If much longer, content has probably leaked from `04_SYSTEMS.md` or the production plan; if much shorter, the slice is underspecified

After writing the file, confirm the path to the user and move to Step 5.

## Step 5: Offer the Task Board Seed (or Defer)

After the slice file is written, ask whether to also seed the task board now:

> "Want to seed `15_TASK_BOARD.md` now with the slice-critical first tasks? You can also defer this and run `/plan-week` later when you're ready to plan your first work session — just say 'skip' or 'later'."

If the user defers, stop here. Confirm the slice is done and let the user know `15_TASK_BOARD.md` can be added later.

If the user wants to continue, move to Step 6.

## Step 6: Seed the Task Board

Write to `<vault-path>/05_production/15_TASK_BOARD.md` using the simple starter template. Populate **This Week** with 3 to 5 slice-critical first tasks derived from the interview — verbs first, one visible result each. Leave Next, Blocked, Later, and Done lightly populated or empty; the `plan-week` skill will refine the board over time.

Use this exact template structure:

```md
# Task Board

## This Week

- [ ] [Task: verb-first, produces one visible result]
- [ ] [Task]
- [ ] [Task]

## Next

- [ ] [Task]
- [ ] [Task]

## Blocked

- [ ] [None yet, or specific blocker]

## Later

- [ ] [Lower-priority slice tasks or deferred items]

## Done

- [x] [Empty until work begins]
```

**Writing rules:**

- Every task in **This Week** starts with a verb (Build, Draft, Implement, Wire, Capture, Tune, Polish)
- Every task names one visible result, not a category of work — "Implement dialogue UI shipping-quality for slice" not "Work on UI"
- **This Week** has 3-5 tasks — fewer than 3 and the user isn't planning enough; more than 5 and the week is overcommitted
- **Next** holds 2-4 follow-on tasks that the user can promote into This Week when the current items finish
- Put any obvious slice-critical work that the user has flagged as risky into **Blocked** with a one-line note, not into This Week — blocked work hides as in-progress otherwise
- Put deferred features and explicit cut items into **Later** so they are visible without being active

After writing the file, confirm both paths to the user. Note that:

- the slice doc is the playable target — when in doubt about whether a task or feature belongs, the slice doc decides
- the next canonical docs to consider are `04_SYSTEMS.md` (use `/define-system` once it ships) for any unclear must-have system, and `15_TASK_BOARD.md` will be refined ongoing via `/plan-week`
