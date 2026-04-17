# GAME PROJECT FULL SYSTEM

This is the complete methodology. It defines the phase model, production rules, AI operating model, and practical constraints for a solo developer making a story-driven 2D game.

If you are new to game development, start with [GAME_PROJECT_SOLO_PRACTICAL_MODE.md](GAME_PROJECT_SOLO_PRACTICAL_MODE.md) and treat this document as the expanded version you grow into.

For canonical file paths and document schemas, use [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md).

## 1. Project North Star

Before building anything, answer these questions clearly:

- What is the one-sentence game concept?
- What specific player fantasy or experience are you promising?
- What must the vertical slice prove?
- What is explicitly out of scope?

The point of the system is to repeatedly turn:

`idea -> structure -> task -> playable result`

If the structure is weak, AI will only create more noise.

## 2. Success Definition

The project succeeds when it produces a vertical slice that proves:

- the core loop is engaging and understandable
- the world, writing, and art direction feel coherent
- the solo workflow is sustainable
- the production process can reliably turn design decisions into playable content

An externally presentable slice is valuable, but it is not the first goal. Internal proof comes first.

## 3. Unified Phase Model

Use one active numbered phase at a time. Some work can overlap, but the team of one should always know which phase is currently driving decisions.

### Phase 0 - Pre-production

Goal:
- turn vague ideas into a clear game concept and slice target

Main outputs:
- vision
- design pillars
- game loop
- first vertical-slice hypothesis

Exit criteria:
- you can explain the game in one sentence
- you know what the slice must prove
- you know what the project is not

### Phase 1 - Narrative and World Exploration

Goal:
- create only the story, character, location, and world structure needed to support the slice

Main outputs:
- story spine
- character cards
- location and faction notes
- dialogue rules
- early quests or scene plans

Exit criteria:
- the slice has enough story context to be built
- you are not worldbuilding blindly beyond slice needs

### Phase 2 - Systems Prototype

Goal:
- make the core gameplay loop work in-engine with placeholder content

Main outputs:
- working prototype
- system specs
- test notes
- clear list of system risks

Exit criteria:
- the main loop is playable
- the biggest technical risks have a known path
- placeholder content is enough to validate interaction and flow

### Phase 3 - Vertical Slice Production

Goal:
- build one short, representative, polished playable section that proves the full production loop

Main outputs:
- playable slice build
- integrated content
- production-ready asset list
- acceptance criteria results

Exit criteria:
- the internal proof gate passes
- optional: the external showcase gate passes

### Phase 4 - Replan Based on Reality

Goal:
- use what the slice taught you to redefine scope, cost, pace, and risks

Main outputs:
- revised production plan
- updated task board
- updated risk log
- cut list and next milestone

Exit criteria:
- you know whether to continue, reduce scope, pause, or reposition the project

## 4. Vertical Slice First

Do not try to build the full game first.

The vertical slice is the first real proof that:

- the core loop works
- the content pipeline works
- the AI review pipeline works
- the asset organization is manageable
- the project is still finishable

If the slice is hard to finish, the full game is currently too large.

## 5. Internal Gate Before External Gate

The slice has two possible quality gates.

### Internal Proof Gate

This is required.

It proves:

- the player can complete the target path end-to-end
- the core loop is readable and fun enough to justify the project
- the highest-risk systems work
- the slice-critical surfaces have the quality needed to judge the direction honestly
- the build survives real testing without game-breaking failures on the target path

### External Showcase Gate

This is optional until the internal proof gate passes.

It proves the slice is ready for:

- cold-player testing
- screenshot and trailer capture
- public-facing feedback
- publisher, grant, or crowdfunding pitch use

Do not block progress on external polish before the internal gate is real.

## 6. Canonical vs Exploratory

This rule is central.

### Canonical artifacts

These are sources of truth:

- markdown docs in the project structure
- the source repo
- tracked asset folders

### Exploratory artifacts

These are useful but not authoritative:

- whiteboards
- canvases
- Twine experiments
- AI brainstorms
- rough prototype branches

### Operational rule

Nothing important is considered real until it is merged into a canonical source.

## 7. Idea Processing Workflow

Every idea should pass through the same steps:

1. Capture it quickly without interrupting active work.
2. Clarify whether it is a system, story, world, asset, workflow, or research idea.
3. Decide whether it supports the current phase and current slice.
4. Convert it into one of:
   - doc update
   - task
   - asset request
   - research note
   - later / cut item
5. Produce the draft, implementation, or artifact.
6. Review it and either merge, revise, or reject it.

## 8. Scope Control Rules

Whenever a new idea appears, ask:

1. Does it directly strengthen the current slice?
2. Does it solve a real player problem?
3. Is it essential to the game's identity?
4. Can it be delayed without damaging the slice?

If the answer is mostly no, move it to `Later`.

Use your design pillars to resolve close calls. If two good ideas compete, pick the one that better supports the pillars and costs less to prove.

## 9. Task Tracking Rule

Beginners should start with a simple board:

- This Week
- Next
- Blocked
- Later
- Done

Only add epics, features, estimates, or multi-level hierarchies when the project actually has multiple active workstreams or collaboration overhead.

A lightweight board used every day is better than a sophisticated board used once a month.

## 10. AI Operating Model

AI should be used as an amplifier, not an unreviewed authority.

### Good uses

- concept clarification
- system scaffolding
- dialogue and quest variants
- asset briefs and prompt drafting
- consistency review
- bug hypothesis generation

### Risky uses

- core architecture you do not understand
- wholesale canon generation without review
- large content dumps with no schema
- production assets with unclear rights or provenance

### Core rules

1. Human defines the schema first.
2. AI generates candidates, not truth.
3. Important outputs resolve into one canonical version.
4. Reusable prompts are stored and revised deliberately.
5. AI-generated assets record origin, date, tool, and shipping status.
6. If AI output becomes vague or contradictory, reduce freedom and increase structure.

## 11. Operational Basics

These are required even if the project is small.

### Engine selection

Pick the engine based on:

- the workflow you already know best
- 2D tooling quality
- dialogue and event support
- save/load support
- export support for your target platform
- how fast you can prototype and debug in it

Default rule:

- choose the engine that gives you the fastest believable path to a slice
- do not switch engines after Phase 2 unless a real blocker appears

### Version control and backups

Use version control from day one.

- keep the code and asset project in a repo
- commit small, meaningful chunks
- write commit messages that describe finished progress
- back up both the repo and design vault off-machine on a regular schedule
- keep generated assets and source files organized enough to restore or replace them

### Rights and sources

Every external reference or generated asset needs enough metadata to answer:

- where it came from
- what tool made it
- whether you have the right to ship it
- whether it still needs replacement or editing

If you cannot answer those questions, it should not be treated as shippable.

### Playtest loop

Once the internal slice gate passes:

- recruit 3-5 cold players
- give them one clear build and one clear objective
- collect feedback in a fixed structure:
  - confusion
  - friction
  - interest
  - bugs
  - moments remembered later
- separate taste feedback from comprehension failures
- update the task board and risk log after each test round

## 12. Tool Roles

Every tool should have a clear role.

- Canonical tool: stores truth
- Exploration tool: used for thinking, sketching, branching, and simulation
- Execution tool: used to build the actual game
- Agent skill: used to clarify, convert, or review

If a tool does not clearly reduce friction more than it adds overhead, do not add it yet.

## 13. Recommended Minimal Toolchain

Start with the lightest setup that can carry the project:

- markdown docs for canon
- optional canvas or whiteboard for exploratory thinking
- optional Twine for branching narrative tests
- game engine plus code editor for implementation
- one task board
- one dev log

Heavy toolchains are usually a late optimization, not an early requirement.

## 14. Recommended Starting Sequence

Create these first, in order:

1. `01_VISION.md`
2. `03_GAME_LOOP.md`
3. `13_VERTICAL_SLICE.md`
4. `04_SYSTEMS.md` with slice-critical systems only
5. `15_TASK_BOARD.md`
6. `DEV_LOG.md`

Then add these as soon as the project needs them:

- `02_DESIGN_PILLARS.md` if the pillars outgrow the vision doc
- `09_STORY_SPINE.md` once the slice needs stable story structure

Then build a placeholder-first prototype.

## 15. First Week Plan

### Day 1

- write the one-sentence concept
- define design pillars
- define what the slice must prove

### Day 2

- define the core loop
- sketch the slice scope
- write the out-of-scope list

### Day 3

- define protagonist, conflict, and one strong scenario
- identify the 2-3 most important NPCs or interactables

### Day 4

- define slice-critical systems
- create the simple task board

### Day 5

- create the dev log
- create the asset registry
- plan the placeholder-first prototype

## 16. Final Principle

Your job is not to make everything.

Your job is to repeatedly turn ambiguity into playable proof without drowning in optional work.
