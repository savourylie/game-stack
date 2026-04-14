# GAME PROJECT SYSTEM

## Purpose

This document defines a practical, AI-native project management system for a solo developer building a story-driven 2D game. Its goal is to turn vague ideas into a structured, finishable production pipeline.

---

# 1. Project North Star

## One-Sentence Game Concept

*Example: A 2D exploration RPG set in a fictional city, where the player navigates social tensions, builds relationships, and unravels a personal mystery with broader consequences.*

## Core Promise

Deliver a dense, atmospheric, story-rich playable experience that feels larger than a solo project because AI is used as a force multiplier for ideation, scaffolding, asset previsualization, and content drafting.

## What Success Means

The project succeeds if it produces a polished vertical slice that proves:

- the setting is compelling
- the exploration and dialogue loop works
- the art and writing direction feel coherent
- the solo and AI workflow is sustainable

---

# 2. Design Pillars

Use these pillars to decide what belongs in the game and what should be cut.

1. **Atmosphere first** — The world should feel alive, specific, and emotionally distinct.
2. **Dense, not huge** — Prioritize compact, high-detail spaces over a large world.
3. **Dialogue and interaction over feature bloat** — Strong writing, NPCs, and moment-to-moment interaction matter more than many systems.
4. **Mystery-driven progression** — The player should feel pulled forward by questions, discoveries, and consequences.
5. **AI as amplifier, not author-in-chief** — AI helps generate options and speed up execution, but the game's identity comes from clear human direction.

---

# 3. Development Strategy

Do not build the full game first.

Build in this order:

### Phase 0 — Pre-production

Goal: define the game well enough to avoid wandering.

### Phase 1 — Systems Prototype

Goal: prove the core exploration, dialogue, and interaction loop works in-engine.

### Phase 2 — Vertical Slice

Goal: build one short, representative, polished playable section.

### Phase 3 — Replan Based on Reality

Goal: use what the slice taught you to redefine scope, cost, and production pace.

---

# 4. Document Structure

Create a project folder with the following canonical docs.

```
/docs
    /01_vision
        01_VISION.md
        02_DESIGN_PILLARS.md
    /02_design
        03_GAME_LOOP.md
        04_SYSTEMS.md
        05_PLAYER_EXPERIENCE.md
    /03_world
        06_WORLD.md
        07_FACTIONS.md
        08_LOCATIONS.md
    /04_story
        09_STORY_SPINE.md
        10_CHARACTERS.md
        11_DIALOGUE_RULES.md
        12_QUESTS.md
    /05_production
        13_VERTICAL_SLICE.md
        14_PRODUCTION_PLAN.md
        15_TASK_BOARD.md
        16_RISK_LOG.md
    /06_ai_pipeline
        17_AI_PIPELINE.md
        18_PROMPT_LIBRARY.md
        19_CONTENT_REVIEW_RULES.md
    /07_assets
        20_ASSET_REGISTRY.md
        21_ART_DIRECTION.md
        22_AUDIO_DIRECTION.md
```

## Canonical Source Rule

Each topic should have **one canonical document**. All brainstorms, rough ideas, and AI variants must eventually resolve into that source.

---

# 5. What Goes in Each Doc

---

### 01_VISION.md

Keep this short.

Include:

- game elevator pitch
- genre
- target emotional experience
- intended audience
- what makes the concept distinctive
- what the MVP must prove
- what the game is explicitly not

#### Template

```md
# Vision

## Elevator Pitch

## Genre

## Player Fantasy

## Emotional Tone

## Why This Game Exists

## What Makes It Distinct

## MVP Must Prove

## This Game Is Not
```

---

### 02_DESIGN_PILLARS.md

#### Purpose
Define the small set of principles that guide decisions across design, story, systems, art, and scope.

#### How to Use
Use these pillars to judge:
- what belongs in the game
- what should be cut
- what should be simplified
- what kinds of tradeoffs are acceptable

#### Rule
A pillar should be:
- short
- memorable
- actionable
- broad enough to guide many decisions
- specific enough to reject bad ideas

#### Template

```md
## Pillar 1
### Name
### Statement
A one-sentence version of the principle.

### Why It Matters
Why this pillar is essential to the identity of the game.

### Design Implications
What this means for systems, content, pacing, or presentation.

### What It Encourages
- 
- 
- 

### What It Rejects
- 
- 
- 

## Pillar 2
### Name
### Statement

### Why It Matters

### Design Implications

### What It Encourages
- 
- 
- 

### What It Rejects
- 
- 
- 

## Pillar 3
### Name
### Statement

### Why It Matters

### Design Implications

### What It Encourages
- 
- 
- 

### What It Rejects
- 
- 
- 

## Pillar 4
### Name
### Statement

### Why It Matters

### Design Implications

### What It Encourages
- 
- 
- 

### What It Rejects
- 
- 
- 

## Pillar 5
### Name
### Statement

### Why It Matters

### Design Implications

### What It Encourages
- 
- 
- 

### What It Rejects
- 
- 
- 

## Conflict Resolution Rule
If two good ideas compete, prefer the one that better supports the design pillars.

## Scope Control Rule
If an idea sounds interesting but supports none of the pillars strongly, move it to Later or cut it.

## Review Checklist
- Is each pillar actually useful in decision-making?
- Do the pillars overlap too much?
- Would these pillars help reject the wrong features?
- Do they reflect the real game, not the imagined oversized version?
- Are they still valid for the current vertical slice?

## Notes
```

---

### 03_GAME_LOOP.md

Define what the player does repeatedly.

Include:

- moment-to-moment loop
- short loop
- long loop
- fail states and tension sources
- reward structure

#### Template

```md
# Game Loop

## Moment-to-Moment Loop

- Move
- Observe
- Interact
- Converse
- Solve / evade / discover

## Short Loop

## Long Loop

## Sources of Tension

## Rewards
```

---

### 04_SYSTEMS.md

List only the systems needed now.

For each system, document:

- purpose
- player-facing effect
- MVP scope
- later expansion ideas
- dependencies

#### Suggested MVP Systems

- character movement
- interaction system
- dialogue system
- quest flags
- area transitions
- save and load
- inventory or key item system
- scripted event triggers

#### Template

```md
# System: [Name]

## Purpose

## Player Experience

## MVP Scope

## Out of Scope for MVP

## Dependencies

## Notes
```

---

### 06_WORLD.md

Capture the world only at gameplay-relevant resolution.

Include:

- setting framing
- social atmosphere
- daily life details
- movement restrictions or social structures
- important institutions
- local symbols and recurring motifs

Do not write an encyclopedia.

#### Template

```md
# World

## Time Period

## Political / Social Atmosphere

## Daily Life

## Themes the Player Feels

## Game-Relevant Setting Details

## Recurring Motifs
```

---

### 07_FACTIONS.md

Define factions in a way that keeps story, quests, world logic, and gameplay consequences aligned.

#### Template

```md
# Factions

## Faction ID
FAC_001

## Name

## Public Identity
What this faction appears to be on the surface.

## Real Nature
What it actually represents, wants, or does behind that public image.

## Goals
What this faction is trying to achieve.

## Methods
How it pursues those goals.

## Resources
What kinds of people, information, money, access, political leverage, or infrastructure it controls.

## Relationship to Protagonist
What the current relationship is between the protagonist and this faction.

## Relationship to Other Factions
Its alliances, rivalries, dependencies, and manipulations.

## Presence in the World
Where this faction appears most often in locations, events, or quests.

## Gameplay Function
How this faction affects gameplay. Examples:
- access restrictions
- information flow
- quest branching
- dialogue tone
- danger level

## Narrative Function
What role this faction plays in the story.

## Escalation Path
How this faction grows from background presence into a more active force.

## Notes
```

---

### 08_LOCATIONS.md

Describe locations as production-ready spaces for gameplay, story, and asset planning rather than pure lore entries.

#### Template

```md
# Locations

## Location ID
LOC_001

## Name

## Type
Examples:
- street
- apartment
- checkpoint
- cafe
- shop
- station
- rooftop
- outdoor zone

## Summary
A one-sentence description of the location's core identity.

## Atmosphere
What the player should feel upon entering.

## Narrative Purpose
What this location does for the story.

## Gameplay Purpose
What this location does for gameplay. Examples:
- tutorial area
- dialogue area
- puzzle area
- chase area
- stealth area
- quest turn-in area

## Key NPCs
Who is commonly found here.

## Key Interactables
Objects, clues, devices, or environmental elements the player can interact with.

## Entry Conditions
When and how the player can enter.

## Exit / Transition Links
What other places this location connects to.

## Required Assets
Backgrounds, props, sound cues, scripted events, and other content needed.

## Reusable Motifs
Visual or narrative motifs repeated here.

## Risks / Constraints
What makes this location difficult or expensive to produce.

## Notes
```

---

### 09_STORY_SPINE.md

Do not start with a full screenplay.

Include:

- protagonist
- want
- fear
- central conflict
- inciting incident
- midpoint shift
- climax direction
- ending possibilities

#### Template

```md
# Story Spine

## Protagonist

## What They Want

## What They Fear

## Core Conflict

## Inciting Incident

## Major Turning Points

## Climax Direction

## Ending Space
```

---

### 10_CHARACTERS.md

Each important character should use the same schema.

#### Template

```md
# Character Card

## Name

## Role

## Public Persona

## Private Truth

## Wants

## Fears

## Relationship to Protagonist

## Speech Pattern

## Visual Notes

## Gameplay Function

## Story Function
```

---

### 11_DIALOGUE_RULES.md

Keep dialogue consistent across AI drafts, human writing, branching scenes, and implementation passes.

#### Template

```md
# Dialogue Rules

## Global Tone
The overall dialogue tone. Examples:
- restrained
- suspicious
- intimate but guarded
- thematically charged
- grounded, not theatrical

## Writing Principles
- Prefer short, sharp lines over long explanations
- Avoid direct exposition unless absolutely necessary
- Use subtext to express emotion, ideology, and relationships
- Do not make characters state things they already know
- Every line should serve character, information, tension, or choice

## Dialogue Do
- Let background and role shape word choice
- Preserve pauses, evasion, interruptions, and silence
- Reveal information unevenly
- Make choices reflect different attitudes, risks, or values

## Dialogue Don't
- Do not write long exposition dumps
- Do not let every character sound the same
- Do not make choices differ only by politeness
- Do not sacrifice setting feel or character truth for easy clarity

## Character Voice Rules

### [Character Name]
- speech rhythm:
- vocabulary level:
- emotional openness:
- taboo topics:
- recurring phrases:
- what they avoid saying directly:

## Choice Design Rules
- Each choice set should express a real difference in attitude, risk, or value
- Some choices should affect flags, relationships, or available information
- Avoid fake choices with no meaningful distinction

## Information Control Rules
- What the player may learn early
- What must be delayed
- What can only be learned through specific characters or events

## Formatting Rules
- speaker name format
- interruption format
- pause and silence format
- thought and internal narration format

## Review Checklist
- Is the character voice consistent?
- Does the scene have a clear purpose?
- Is anything overexplained?
- Do the player choices genuinely differ?
- Has "literary style" harmed usability or implementation clarity?

## Notes
```

---

### 12_QUESTS.md

Each quest should be compact and implementation-friendly.

#### Template

```md
# Quest ID: QUEST_001

## Title

## Narrative Purpose

## Player Goal

## Entry Condition

## Steps

## Key NPCs

## Key Dialogue

## Required Assets

## Reward / Consequence

## Flags Set
```

---

### 13_VERTICAL_SLICE.md

This is the most important production document.

Define:

- exact duration target
- one area or small chain of areas
- one central scenario
- required systems
- required assets
- acceptance criteria

#### Recommended Scope

- 15–30 minutes
- 1 explorable district or street cluster
- 2–3 NPCs with meaningful dialogue
- 1 main objective
- 1 memorable tension event
- 1 story reveal

#### Template

```md
# Vertical Slice

## Purpose

## Target Duration

## Playable Area

## Main Objective

## Required Systems

## Required Content

## Required Assets

## What This Slice Must Prove

## Done Criteria
```

---

### 14_PRODUCTION_PLAN.md

Break the project into explicit stages.

#### Template

```md
# Production Plan

## Phase 0: Pre-production

### Goals

### Deliverables

### Not Included

### Done Criteria

## Phase 1: Prototype

### Goals

### Deliverables

### Not Included

### Done Criteria

## Phase 2: Vertical Slice

### Goals

### Deliverables

### Not Included

### Done Criteria
```

---

### 15_TASK_BOARD.md

Use this as the logic behind your board, not just a checklist.

#### Work Item Hierarchy

- Epic
- Feature
- Task
- Subtask

#### Suggested Status Columns

- Inbox
- Clarify
- Ready
- In Progress
- Review
- Done
- Cut / Later

#### Suggested Fields

- ID
- title
- parent item
- owner
- status
- priority
- milestone
- estimate
- dependencies
- definition of done
- notes

#### Example

```md
Epic: Vertical Slice
Feature: Dialogue System
Task: Build branching dialogue UI
Subtasks:
  - render speaker name
  - show choices
  - support next-node transitions
  - set story flags
  - test edge cases
```

---

### 16_RISK_LOG.md

#### Template

```md
# Risk Log

## Risk ID
RISK_001

## Title

## Description

## Category
- scope
- technical
- narrative
- art consistency
- workflow
- burnout
- legal / reference

## Probability
- low
- medium
- high

## Impact
- low
- medium
- high

## Mitigation
What you will do to reduce the risk.

## Trigger / Warning Signs
What signals that this risk is beginning to materialize.

## Owner
Usually yourself.

## Review Date

## Status
- open
- watching
- mitigated
- closed

## Notes
```

---

### 17_AI_PIPELINE.md

Define what AI is allowed to do in the project, what it is not allowed to do, and how outputs move into canon.

#### Template

```md
# AI Pipeline

## Purpose
Define what AI is responsible for in this project and what remains human-controlled.

## Core Principle
AI generates candidates, not canon.

## Approved Use Cases
- concept ideation
- system scaffolding
- dialogue variants
- quest generation
- asset briefs
- prompt drafting
- review and consistency checks

## Disallowed or Cautious Use Cases
- moving unreviewed AI output directly into canon
- accepting generated architecture you do not understand
- generating large amounts of content without naming, classification, or status tracking

## Workflow
1. Human defines the schema
2. AI generates candidates
3. Human reviews and trims
4. Output is converted into structured docs, tasks, or assets
5. Canonical source is updated

## Input Requirements
Before prompting AI, provide at least:
- current phase
- target artifact
- constraints
- tone and style rules
- output format

## Output Requirements
AI output should prefer:
- checklists
- cards
- structured field blocks
- scene sheets
- implementation steps

## Validation Rules
- Does it support the current slice?
- Does it conflict with canon?
- Can it be converted into a task, spec, or asset brief?
- Should it be explicitly marked as draft?

## File / Asset Tagging Rules
Every AI-generated output should record:
- date
- tool / model
- purpose
- status
- keep / reject / revise

## Notes
```

---

### 18_PROMPT_LIBRARY.md

Turn useful prompts into reusable project assets instead of rewriting them from scratch every time.

#### Template

```md
# Prompt Library

## Prompt ID
PROMPT_001

## Name

## Purpose
What this prompt is for.

## When to Use

## Required Inputs
What information must be available before using it.

## Output Format
What format the AI should return.

## Prompt
Full prompt text.

## Example Input

## Example Output Summary

## Failure Modes
Common failures:
- too vague
- too long
- conflicts with canon
- lacks implementation value

## Revision Notes
How this prompt has been improved or changed.

## Status
- draft
- active
- deprecated
```

---

### 19_CONTENT_REVIEW_RULES.md

Give AI outputs, human-written content, and integrated content a shared review standard.

#### Template

```md
# Content Review Rules

## Purpose
Define what qualifies as usable content versus rough draft material.

## Review Dimensions
- canon consistency
- tone consistency
- implementation readiness
- production cost
- gameplay usefulness
- narrative clarity

## Review Questions
- Does this conflict with existing canon?
- Does it actually support the current slice?
- Can it be converted into a quest, system, asset, or scene?
- Is it only "cool," or is it useful?
- Is the production cost too high for its value?

## Pass / Revise / Reject Rules

### Pass
Can move directly into a canonical doc or implementation pipeline.

### Revise
Core idea is useful, but it needs reduction, rewriting, or format correction.

### Reject
It does not fit the direction, costs too much, or creates confusion.

## Special Rules for AI Output
- AI output is not final by default
- Content without a clear use should not be kept
- Keep only a small number of high-quality candidates per topic

## Review Checklist
- clear
- in scope
- coherent
- playable and implementable
- emotionally aligned
- production-feasible

## Notes
```

---

### 20_ASSET_REGISTRY.md

Track every content asset with a consistent schema.

#### Fields

- asset ID
- name
- type
- usage
- location / chapter
- source
- AI-generated (yes / no)
- current status
- owner
- file path
- needs revision (yes / no)
- notes

#### Types

- character sprite
- portrait
- background
- tileset
- UI element
- sound effect
- music track
- dialogue file
- script scene
- cutscene panel

#### Example

```md
ID: BG_STREET_01
Name: City Street at Dusk
Type: Background
Usage: Vertical slice intro area
Source: AI concept → edited
Status: In progress
File Path: /assets/backgrounds/street_01/
Needs Revision: Yes
```

---

### 21_ART_DIRECTION.md

Turn visual direction into something that can guide production, generation, review, and revision.

#### Template

```md
# Art Direction

## Art Pillars
The core visual principles of the game. Examples:
- stylized realism
- environmental storytelling
- intimate human detail

## Overall Style
High-level description of the intended visual style.

## Shape Language
What kind of shape language defines characters, props, and spaces.

## Color Logic
Color strategy in terms of mood and function, not just palette.

## Lighting Logic
How lighting changes by time, place, mood, and narrative purpose.

## Texture / Surface Rules
Material feel, age, grit, wear, and environmental roughness.

## Character Visual Rules
Rules for designing character silhouettes, clothing, posture, and visual identity.

## Environment Visual Rules
Rules for streets, interiors, public spaces, signage, and density.

## UI Visual Rules
How UI should align with the setting and the rest of the visual language.

## Animation Feel
What the movement style should feel like.

## Reference Anchors
What kinds of reference works are useful, without directly copying them.

## Do / Don't

### Do
- preserve a believable setting feel
- reinforce the world's social and spatial identity
- show traces of ordinary daily life

### Don't
- do not drift into unintended genre aesthetics
- do not exceed production capacity for the current slice
- do not look inconsistent across areas and characters

## Review Checklist
- Does it support the visual pillars?
- Is it aligned with the subject matter and story?
- Can it be reproduced consistently in production?
- Does it exceed the quality level actually needed for the current slice?

## Notes
```

---

### 22_AUDIO_DIRECTION.md

Define how sound and music support story, space, tension, and gameplay instead of being treated as generic mood.

#### Template

```md
# Audio Direction

## Audio Pillars
Examples:
- tense but restrained
- pressure embedded in everyday environments
- strong sense of place and space
- voice and ambience both carry narrative weight

## Music Strategy
When music should appear, and when it should deliberately not appear.

## Ambience Strategy
How ambience creates place, pressure, distance, and emotional texture.

## SFX Strategy
Rules for interaction sounds, machinery, doors, footsteps, distant activity, and mechanical texture.

## Dialogue Audio Rules
If voice, processing, or voice-adjacent treatment is used later, define the rules here.

## Silence Rules
When to intentionally leave space without music or obvious sound emphasis.

## Location-Based Audio Notes

### [Location Name]
- key ambience:
- notable distant sounds:
- emotional effect:

## Event Audio Notes

### [Event Name]
- tension cue:
- transition cue:
- aftermath cue:

## Technical Notes
- loop needs
- layering needs
- priority rules
- implementation constraints

## Review Checklist
- Does it strengthen spatial awareness?
- Does it increase tension appropriately?
- Does it pull too much focus?
- Does it support gameplay readability?
- Is it achievable with current production capacity?

## Notes
```

---

# 6. Idea Processing Workflow

Every idea should go through the same pipeline.

## Step 1 — Capture

Dump the idea into an inbox immediately. Do not interrupt active work to build it.

## Step 2 — Clarify

Classify it:

- world
- story
- system
- asset
- production
- research

Then ask:

- does it support the current milestone?
- does it belong now or later?
- is it a canonical doc update, or a task?

## Step 3 — Convert

Turn it into one of these:

- doc update
- task
- asset request
- research note
- cut / later backlog item

## Step 4 — Produce

Use AI or manual work to generate a draft, implementation, or artifact.

## Step 5 — Review

Check whether it is:

- consistent
- useful
- in scope
- ready to merge into canonical source

---

# 7. Weekly Solo Dev Rhythm

Use a lightweight rhythm to avoid drift.

## Weekly Planning Session

Once per week, answer:

- what milestone am I actually in?
- what are the 3 most important outcomes this week?
- what should be cut or delayed?
- what decisions are blocked?

## Daily Loop

At the start of a work session:

- choose 1 main task
- choose 1 backup task
- define what "done today" means

At the end of a work session:

- log progress
- note blockers
- capture new ideas into inbox
- update task status

## Suggested Weekly Format

```md
# Weekly Planning

## Current Milestone

## This Week's Top 3 Outcomes

1.
2.
3.

## Tasks to Cut or Delay

## Biggest Risks

## Decisions Needed
```

---

# 8. AI Usage Model

AI should be assigned specific jobs.

## Best Use Cases

### Programming

Use AI for:

- prototype scaffolding
- editor tools
- boilerplate
- refactoring suggestions
- bug hypothesis generation

Do not rely on AI blindly for:

- core architecture you do not understand
- complex systems without tests
- tightly coupled gameplay logic without review

### Writing

Use AI for:

- NPC variants
- dialogue passes
- quest ideation
- tone exploration
- lore expansion proposals

Do not allow AI to freely expand canon without review.

### Art / Content

Use AI for:

- moodboards
- concept ideation
- prompt exploration
- rough compositions
- variant generation

Do not treat raw generations as final production assets without a style-control process.

---

# 9. AI Pipeline Rules

Document these rules in `17_AI_PIPELINE.md`.

## Rule 1

Human defines the schema first.

## Rule 2

AI generates candidates, not truth.

## Rule 3

Everything important must resolve into one canonical version.

## Rule 4

Every reusable prompt should be stored and versioned.

## Rule 5

Every AI-generated asset must be tagged with source, tool, date, and revision status.

## Rule 6

If AI output creates confusion, reduce freedom and increase structure.

---

# 10. Prompt Library Structure

Store prompts by domain.

```
/prompts
    /code
    /dialogue
    /quests
    /characters
    /worldbuilding
    /art
    /ui
```

Each prompt entry should include:

- name
- purpose
- input format
- expected output format
- examples
- what usually goes wrong
- last updated date

## Prompt Card Template

```md
# Prompt Name

## Purpose

## Inputs Required

## Output Format

## Prompt

## Example Use

## Failure Modes

## Revision Notes
```

---

# 11. Vertical Slice First Rule

Before building more content, prove the full production loop works once.

The slice should cover:

- design intent
- implementation workflow
- AI-assisted content generation
- asset naming and storage
- dialogue integration
- event scripting
- build / test / review loop

If the slice is hard to finish, the full game is currently too large.

---

# 12. Scope Control Rules

Whenever a new idea appears, ask:

1. Does it directly improve the vertical slice?
2. Does it solve a real player problem?
3. Is it essential to the game's identity?
4. Can it be delayed without damaging the slice?

If the answer is "not really," move it to **Later**.

## Things to Delay Aggressively

- large talent trees
- deep equipment systems
- many explorable areas
- multiple endings beyond what the slice needs
- combat complexity unless combat is core identity
- procedural content systems
- cinematic ambitions that blow up production cost

---

# 13. Risk Log

Maintain a simple risk register in `16_RISK_LOG.md`.

## Categories

- scope risk
- technical risk
- art consistency risk
- narrative coherence risk
- burnout risk
- legal / reference risk

See the full template in Section 5 under `16_RISK_LOG.md`.

---

# 14. Recommended Starting Tasks

Start with these in order:

1. Write `01_VISION.md`
2. Write `03_GAME_LOOP.md`
3. Draft `13_VERTICAL_SLICE.md`
4. Create `04_SYSTEMS.md` with only MVP systems
5. Draft `09_STORY_SPINE.md`
6. Create a simple task board
7. Create an empty asset registry
8. Build a graybox prototype using placeholder art

---

# 15. What to Do This Week

## Day 1

- write the one-sentence concept
- define design pillars
- define what the MVP must prove

## Day 2

- define the core loop
- decide what is in and out of the vertical slice

## Day 3

- draft protagonist, conflict, and first scenario
- identify 2–3 key NPCs

## Day 4

- define MVP systems
- create task board structure

## Day 5

- create asset registry schema
- start placeholder-first prototype plan

---

# 16. Final Principle

Your real job is not to "make everything."

Your real job is to continuously transform:

**idea → structure → task → playable result**

That transformation system is the project.

If the system is good, AI will meaningfully multiply your output. If the system is weak, AI will only generate noise faster.

---

# 17. Solo Practical Mode

If the full system feels too heavy, run the project in **Solo Practical Mode**.

This mode reduces the number of active documents, decisions, and tracking surfaces. The rule is simple:

**Only keep the smallest structure that still prevents chaos.**

## Active Docs Only

In active use, keep only these 5 docs open and alive:

1. `VISION.md`
2. `GAME_LOOP.md`
3. `VERTICAL_SLICE.md`
4. `TASK_BOARD.md`
5. `DEV_LOG.md`

Everything else is reference material that can be expanded later.

## What Each One Does

### VISION.md

Defines the game in 1 page.

Contains:

- one-sentence concept
- design pillars
- MVP proof goal
- explicit non-goals

### GAME_LOOP.md

Defines what the player does.

Contains:

- moment-to-moment loop
- short loop
- tension sources
- reward structure

### VERTICAL_SLICE.md

Defines the current target.

Contains:

- the playable scenario
- systems required
- content required
- what counts as done

### TASK_BOARD.md

Defines what to do next.

Contains only:

- this week
- next
- blocked
- later
- done

### DEV_LOG.md

Defines what happened.

Contains:

- what I worked on today
- what got finished
- what is blocked
- what new ideas appeared
- what needs clarification

---

# 18. Solo Weekly Workflow

Use this repeatable loop.

## Monday — Decide

- update `VERTICAL_SLICE.md`
- pick this week's 1 main outcome
- pick up to 3 supporting tasks
- cut anything non-essential

## During the Week — Build

For each session:

- read `VERTICAL_SLICE.md`
- choose 1 task only
- ask AI for help only on that task
- integrate and test immediately
- log results in `DEV_LOG.md`

## Friday — Review

- what moved the slice forward?
- what was fake progress?
- what should be cut?
- what should become a reusable prompt, template, or workflow?

---

# 19. Solo Task Board Format

Do not use a complex board at the beginning. Use this format:

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

## Task Writing Rule

Every task should start with a verb and produce one visible result.

**Good:**

- Implement dialogue box with name and choices
- Draft 3 NPC cards for the opening area
- Create placeholder background for the starting location

**Bad:**

- Work on dialogue
- Think about the story
- Improve atmosphere

---

# 20. Solo Decision Filter

Whenever a new idea appears, run this filter:

## Step 1 — Is it one of these?

- system
- story
- world
- asset
- workflow

## Step 2 — Does it help the current slice?

If no, move to Later.

## Step 3 — Is it a document update or a task?

- If it changes understanding, update a doc.
- If it changes output, create a task.

## Step 4 — Can it be finished in 1 session?

If not, split it.

---

# 21. Interactive Agent Skill Strategy

After the top-level workflow is stable, build one **interactive agent skill per phase**.

Do not try to build one giant all-purpose agent first.

Instead, create a small set of focused skills that match the real development stages.

## Why This Works

A giant project-management agent becomes vague and noisy. A phase-specific skill can:

- ask the right questions
- use the right templates
- produce the right artifacts
- help you make decisions at the right level

---

# 22. Recommended Agent Skills by Phase

## Skill 1 — Concept Architect

Used in: Pre-production

### Job

Turn rough ideas into a clear concept and slice target.

### Inputs

- raw premise
- references
- desired emotional tone
- constraints as a solo developer

### Outputs

- one-sentence concept
- design pillars
- MVP proof statement
- initial world and story framing
- candidate vertical slice concepts

### Interaction Style

The agent should challenge vagueness and force compression. It should repeatedly ask:

- what is the actual player fantasy?
- what makes this game different?
- what is the smallest playable proof?

---

## Skill 2 — Slice Planner

Used in: Pre-production to Prototype transition

### Job

Convert the chosen idea into an actionable vertical slice plan.

### Inputs

- concept docs
- game loop
- early system ideas

### Outputs

- vertical slice spec
- must-have systems list
- content list
- out-of-scope list
- weekly priorities

### Interaction Style

The agent should reduce ambition, identify dependencies, and expose fake scope.

---

## Skill 3 — Systems Co-Designer

Used in: Prototype

### Job

Help define and implement small gameplay systems one by one.

### Inputs

- target system
- current engine setup
- constraints
- codebase conventions

### Outputs

- system spec
- edge cases
- data structures
- implementation checklist
- test checklist

### Interaction Style

The agent should stay concrete and implementation-aware. It should think in terms of:

- player input
- state transitions
- failure cases
- debugability

---

## Skill 4 — Narrative Room

Used in: World / Story / Dialogue production

### Job

Help generate and refine story content while preserving canon.

### Inputs

- canonical story docs
- character cards
- scene purpose
- tone and constraints

### Outputs

- scene outlines
- dialogue candidates
- NPC voice consistency checks
- quest structures
- contradiction warnings

### Interaction Style

The agent should behave like a story room partner, not a free-writing machine. It should prefer structured outputs over long prose dumps.

---

## Skill 5 — Asset Director

Used in: Art / content production

### Job

Turn scene and content requirements into asset briefs.

### Inputs

- scene purpose
- art direction
- gameplay usage
- technical constraints

### Outputs

- asset list
- naming suggestions
- art prompts
- revision checklist
- integration notes

### Interaction Style

The agent should focus on production readiness, not just inspiration.

---

## Skill 6 — Solo Producer

Used in: Ongoing weekly management

### Job

Act as a lightweight producer that helps you stay on the rails.

### Inputs

- current milestone
- this week's progress
- blockers
- open decisions

### Outputs

- trimmed weekly plan
- priority order
- risk reminders
- cut / delay suggestions
- next-step recommendations

### Interaction Style

The agent should be strict about focus and anti-chaos.

---

# 23. Build Order for the Agent Skills

Create them in this order:

1. Concept Architect
2. Slice Planner
3. Solo Producer
4. Systems Co-Designer
5. Narrative Room
6. Asset Director

## Why This Order

Because the biggest early risk is not implementation quality. It is lack of definition and loss of focus.

---

# 24. Agent Skill Design Template

Use this template whenever you create a new interactive skill.

```md
# Skill Name

## Purpose
What this skill helps decide or produce.

## When to Use
Which phase or situation triggers it.

## Inputs
What the user must provide.

## Outputs
What artifacts the skill should produce.

## Boundaries
What the skill should not do.

## Interaction Pattern
What questions it should ask.
What structure it should enforce.

## Default Output Formats
- checklist
- spec
- task list
- character card
- asset brief
- scene sheet

## Failure Modes
- too vague
- too expansive
- duplicates canon
- produces output that is not implementation-ready
```

---

# 25. Practical Rule for Agent Design

Every skill should do one of only three things:

1. Clarify
2. Convert
3. Review

If a skill tries to do all three at once for the entire project, it becomes weak.

---

# 26. Best First Implementation

The best first interactive skill is not the story agent or the coding agent.

It is the **Slice Planner**.

Because right now your biggest leverage is learning how to repeatedly convert:

**idea → slice spec → weekly plan → finished chunk**

That is the bottleneck that determines whether the whole project survives.

---

# 27. Phase-by-Phase Toolchain

Each phase should name:

- the main tool
- the optional supporting tools
- the output artifact
- where the final result is stored canonically

This prevents the workflow from becoming abstract and keeps every step grounded in a real place to work.

## Tool Roles

Use this distinction consistently:

- **Canonical tool:** the source of truth
- **Exploration tool:** used for thinking, branching, sketching, and prototyping
- **Execution tool:** used to build the actual game
- **Agent skill:** used to clarify, convert, or review

---

# 28. Recommended Minimal Toolchain

Start with the lightest workable setup.

## Canon / Project Memory

- **Main tool:** Obsidian
- **Role:** canonical tool
- **Used for:** vision docs, story docs, system docs, task board, dev log, prompt library
- **Canonical storage:** markdown files in the project vault

## Visual Thinking

- **Main tool:** Obsidian Canvas
- **Optional:** Miro
- **Role:** exploration tool
- **Used for:** whiteboards, references, relationship maps, planning sketches
- **Canonical storage:** summarized back into markdown docs

## Narrative Prototyping

- **Main tool:** Twine 2
- **Role:** exploration tool
- **Used for:** branching dialogue prototypes, quest flow tests, pacing checks
- **Canonical storage:** dialogue specs, quest docs, story docs

## Graph / Dependency Mapping

- **Main tool:** yEd
- **Optional use only when needed**
- **Role:** exploration tool
- **Used for:** faction graphs, quest dependencies, location flow, event logic maps
- **Canonical storage:** summarized back into markdown docs

## Task Execution

- **Main tool:** `TASK_BOARD.md` + `DEV_LOG.md`
- **Role:** canonical tool
- **Used for:** weekly planning, daily execution, progress tracking, blockers
- **Canonical storage:** markdown docs

## Game Implementation

- **Main tool:** game engine and code editor
- **Role:** execution tool
- **Used for:** systems, content integration, playtesting, iteration
- **Canonical storage:** source repo

## AI Collaboration

- **Main tool:** phase-specific agent skills
- **Role:** agent skill
- **Used for:** concept clarification, slice planning, systems design, narrative refinement, asset briefing, weekly focus management
- **Canonical storage:** outputs merged into markdown docs and repo assets

---

# 29. Toolchain by Phase

## Phase 0 — Pre-production

### Goal

Turn vague ideas into a coherent game concept and slice target.

### Main Tools

- Obsidian
- Obsidian Canvas

### Optional Tools

- Miro
- reference folders

### Agent Skills

- Concept Architect
- later: Slice Planner

### Outputs

- VISION.md
- GAME_LOOP.md
- early VERTICAL_SLICE.md
- reference boards

### Canonical Storage

All final decisions go back into markdown docs.

### Notes

Do not let ideas remain only in whiteboards. Every important idea must resolve into a written doc.

---

## Phase 1 — Narrative / World Exploration

### Goal

Explore story structure, dialogue rhythm, quest possibilities, and scene logic before heavy implementation.

### Main Tools

- Obsidian
- Twine 2

### Optional Tools

- yEd for relationship maps
- Obsidian Canvas for story clustering

### Agent Skills

- Narrative Room
- Concept Architect for unresolved framing

### Outputs

- character cards
- quest drafts
- dialogue prototypes
- scene structures
- story notes

### Canonical Storage

- character docs
- quest docs
- dialogue rules
- story spine

### Notes

Twine is for simulation and validation, not for being the long-term source of truth. If a Twine experiment is successful, convert it into structured docs.

---

## Phase 2 — Systems Prototype

### Goal

Make the core gameplay loop work in-engine with placeholder content.

### Main Tools

- game engine
- code editor
- Obsidian

### Optional Tools

- debug notes in markdown
- simple diagrams in Canvas

### Agent Skills

- Systems Co-Designer
- Solo Producer

### Outputs

- graybox prototype
- system specs
- implementation checklists
- test notes

### Canonical Storage

- repo for code
- markdown docs for specs and logs

### Notes

Prototype first with placeholder assets. Avoid mixing polished art goals with uncertain systems work.

---

## Phase 3 — Vertical Slice Production

### Goal

Build one short playable section that represents the intended game quality and workflow.

### Main Tools

- game engine
- Obsidian
- `TASK_BOARD.md`
- `DEV_LOG.md`

### Optional Tools

- Twine 2 for dialogue iterations
- Obsidian Canvas for content coordination

### Agent Skills

- Slice Planner
- Narrative Room
- Systems Co-Designer
- Asset Director
- Solo Producer

### Outputs

- playable slice build
- integrated content
- asset lists
- revised scope understanding

### Canonical Storage

- repo for implementation
- asset folders for production content
- markdown docs for final specs and decisions

### Notes

This is the first real proof of the whole production loop. Anything that slows completion without strengthening the slice should be cut.

---

## Phase 4 — Asset Production

### Goal

Generate and integrate the assets needed for the slice or later production.

### Main Tools

- Obsidian
- asset generation and editing tools
- project asset folders

### Optional Tools

- Canvas for art boards
- yEd for dependency-heavy content maps

### Agent Skills

- Asset Director
- Solo Producer

### Outputs

- asset briefs
- prompts
- revision checklists
- updated asset registry

### Canonical Storage

- ASSET_REGISTRY.md
- asset folders in repo or production storage

### Notes

Every asset should have a clear gameplay or narrative use. Track origin and revision state, especially for AI-generated material.

---

## Phase 5 — Ongoing Solo Management

### Goal

Keep the project moving without drowning in ideas or fake progress.

### Main Tools

- `TASK_BOARD.md`
- `DEV_LOG.md`
- Obsidian

### Agent Skills

- Solo Producer

### Outputs

- weekly plan
- trimmed priorities
- blocker list
- cut / delay decisions
- milestone review notes

### Canonical Storage

All management decisions go into markdown logs and planning docs.

### Notes

A simple management loop used consistently beats a complex workflow used rarely.

---

# 30. Tool Selection Rules

When deciding whether to add a tool, ask:

1. Does this tool solve a repeated problem?
2. Does it reduce friction more than it adds overhead?
3. Does it have a clear role: canonical, exploratory, execution, or agent?
4. Do I know where its output will be stored finally?

If these answers are unclear, do not add the tool yet.

---

# 31. Canonical vs Exploratory Rule

This rule is critical.

## Exploratory Tools

Used for:

- branching
- sketches
- experiments
- whiteboards
- prototypes

Examples:

- Twine 2
- Obsidian Canvas
- Miro
- yEd

## Canonical Tools

Used for:

- final decisions
- stable references
- current project truth

Examples:

- markdown docs in Obsidian
- source repo
- asset registry

## Operational Rule

Nothing important is considered "real" until it is merged into a canonical source.

---

# 32. Recommended First Setup

For the first practical version of the project, use only this:

- Obsidian
- Obsidian Canvas
- Twine 2
- markdown task board
- markdown dev log
- game engine + code editor

Only add yEd, Miro, or anything heavier when a specific recurring problem appears.

---

# 33. Toolchain + Agent Skill Pairing

A good rule is:

- **Docs define**
- **Tools explore**
- **Engine proves**
- **Agent skills convert and review**

## Example Pairing

- `Concept Architect` ↔ Obsidian + Canvas
- `Slice Planner` ↔ VISION + GAME_LOOP + TASK_BOARD
- `Narrative Room` ↔ story docs + Twine 2
- `Systems Co-Designer` ↔ systems docs + engine + code editor
- `Asset Director` ↔ asset registry + art direction + generation tools
- `Solo Producer` ↔ task board + dev log

This is the practical shape of the workflow.
