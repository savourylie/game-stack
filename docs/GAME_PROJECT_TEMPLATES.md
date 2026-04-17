# GAME PROJECT TEMPLATES

This document owns the canonical folder structure, filenames, and required sections for each project document.

Use these filenames as the source of truth. Friendly shorthand names from Solo Practical Mode are aliases only.

## 1. Canonical Project Structure

```text
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
        DEV_LOG.md
    /06_ai_pipeline
        17_AI_PIPELINE.md
        18_PROMPT_LIBRARY.md
        19_CONTENT_REVIEW_RULES.md
    /07_assets
        20_ASSET_REGISTRY.md
        21_ART_DIRECTION.md
        22_AUDIO_DIRECTION.md
```

## 2. Canonical Source Rule

- Each topic gets one canonical document.
- Brainstorms, experiments, and AI drafts must eventually resolve into that source.
- Do not maintain parallel versions of the same concept in multiple docs.

## 3. Core Docs First

If you are starting from zero, create only these documents first:

- `01_VISION.md`
- `03_GAME_LOOP.md`
- `04_SYSTEMS.md`
- `13_VERTICAL_SLICE.md`
- `15_TASK_BOARD.md`
- `DEV_LOG.md`

Add the rest only when the project genuinely needs them.

Solo Practical Mode exception:

- you may keep your design pillars inside `01_VISION.md` at first
- split them into `02_DESIGN_PILLARS.md` only when the project needs a separate decision document

## 4. Vision Docs

### 01_VISION.md

Purpose:
- define the game in one page

Required sections:
- Elevator Pitch
- Genre
- Player Fantasy
- Emotional Tone
- Why This Game Exists
- What Makes It Distinct
- MVP Must Prove
- This Game Is Not

Rules:
- keep it short
- use it as a decision filter, not a lore dump
- define the minimum proof, not the dream version
- in Solo Practical Mode, design pillars may live here temporarily until split into `02_DESIGN_PILLARS.md`

### 02_DESIGN_PILLARS.md

Purpose:
- define the small set of principles that guide design, scope, and tradeoffs

Required sections for each pillar:
- Name
- Statement
- Why It Matters
- Design Implications
- What It Encourages
- What It Rejects

Additional sections:
- Conflict Resolution Rule
- Scope Control Rule
- Review Checklist
- Notes

Rules:
- use 3-5 pillars
- every pillar must help reject bad ideas
- pillars should be memorable and actionable
- if you are still in Solo Practical Mode, this file can be created later by splitting the pillar section out of `01_VISION.md`

## 5. Design Docs

### 03_GAME_LOOP.md

Purpose:
- define what the player does, why it matters, and how the game responds

Required sections:
- The Three-Tiered Loop
  - Primary Loop
  - Secondary Loop
  - Tertiary Loop
- Cognitive Cycle
  - Mental Model and Action
  - System Rules
  - Feedback and Interpretation
- Chains
  - Value Chains
  - Execution Chains
  - Secret Chains
- Pacing
  - Tension Sources
  - Moments of Rest
  - Rhythm
- Goal Connections and Progression
  - Short-Term to Long-Term Bridge
  - Fail States

Rules:
- define the exact second-to-second action first
- describe the feedback the player sees, hears, and understands
- name the recovery path after failure

### 04_SYSTEMS.md

Purpose:
- define only the gameplay and support systems needed now

Format rule:
- use one repeated system card per system

Required sections for each system card:
- System Name
- Purpose
- Player Problem Solved
- Player Input
- System Rules
- Feedback
- Success State
- Failure State
- MVP Scope
- Out of Scope for MVP
- Dependencies
- Edge Cases
- Test Checklist
- Notes

Rules:
- begin with slice-critical systems only
- every system must define input, rules, feedback, and tests
- if you cannot explain the system simply, it is probably too large

### 05_PLAYER_EXPERIENCE.md

Purpose:
- define how the game should feel to play, not just what systems exist

Required sections:
- Core Player Fantasy
- Emotional Arc of a Typical Session
- Readability Goals
- Tension and Relief Pattern
- Failure Experience
- Delight Targets
- Frustrations to Avoid
- Accessibility and Usability Rules
- Review Checklist

Rules:
- describe the intended feeling of play in player-facing terms
- include clarity, pacing, and accessibility expectations
- use this doc to catch systems that are technically correct but unpleasant

## 6. World Docs

### 06_WORLD.md

Purpose:
- capture the world only at gameplay-relevant resolution

Required sections:
- Time Period
- Political and Social Atmosphere
- Daily Life
- Themes the Player Feels
- Game-Relevant Setting Details
- Recurring Motifs

Rules:
- do not write an encyclopedia
- keep world details tied to play, story, and art direction

### 07_FACTIONS.md

Purpose:
- align factions across story, quests, world logic, and gameplay consequences

Required sections for each faction:
- Faction ID
- Name
- Public Identity
- Real Nature
- Goals
- Methods
- Resources
- Relationship to Protagonist
- Relationship to Other Factions
- Presence in the World
- Gameplay Function
- Narrative Function
- Escalation Path
- Notes

Rules:
- define what the faction does in play, not just in lore
- each faction should influence access, information, pressure, or choice

### 08_LOCATIONS.md

Purpose:
- describe locations as production-ready spaces for gameplay, story, and asset planning

Required sections for each location:
- Location ID
- Name
- Type
- Summary
- Atmosphere
- Narrative Purpose
- Gameplay Purpose
- Key NPCs
- Key Interactables
- Entry Conditions
- Exit and Transition Links
- Required Assets
- Reusable Motifs
- Risks and Constraints
- Notes

Rules:
- locations must justify themselves in both narrative and production terms
- call out anything expensive, unique, or hard to reuse

## 7. Story Docs

### 09_STORY_SPINE.md

Purpose:
- define the story structure without writing a full screenplay too early

Required sections:
- Protagonist
- What They Want
- What They Fear
- Core Conflict
- Inciting Incident
- Major Turning Points
- Climax Direction
- Ending Space

Rules:
- keep it structural
- define the pressures that drive the slice and the later game

### 10_CHARACTERS.md

Purpose:
- describe important characters using one consistent card format

Required sections for each character:
- Name
- Role
- Public Persona
- Private Truth
- Wants
- Fears
- Relationship to Protagonist
- Speech Pattern
- Visual Notes
- Gameplay Function
- Story Function

Rules:
- each important character should affect both story and play
- voice and behavior should be production-usable, not literary-only

### 11_DIALOGUE_RULES.md

Purpose:
- keep dialogue consistent across human writing, AI drafting, and implementation

Required sections:
- Global Tone
- Writing Principles
- Dialogue Do
- Dialogue Don't
- Character Voice Rules
- Choice Design Rules
- Information Control Rules
- Formatting Rules
- Review Checklist
- Notes

Rules:
- choices should differ in attitude, risk, or value
- avoid exposition dumps
- preserve implementation clarity alongside tone

### 12_QUESTS.md

Purpose:
- define quests in a way that is compact, testable, and implementation-friendly

Required sections for each quest:
- Quest ID
- Title
- Narrative Purpose
- Player Goal
- Entry Condition
- Steps
- Success End State
- Failure or Abort Cases
- Key NPCs
- Key Dialogue
- Required Systems
- Required Assets
- Reward and Consequence
- Flags Set and Cleared
- Test Checklist

Rules:
- every quest needs a clear success condition
- every quest needs a recovery or abort rule if the path breaks
- if a quest is mostly lore and not actionable, rewrite it

## 8. Production Docs

### 13_VERTICAL_SLICE.md

Purpose:
- define one short playable section that proves the game and the workflow

Required sections:
- Target Scope and Scenario
- Game-Timeline Position
- Feature Balance
- Narrative and Progression
- Loop and Chain Validation
- Required MVP Systems
- Required Content and Assets
- Out of Scope
- Layer Coverage
- Workflow and Pipeline Proof
- Internal Proof Gate
- External Showcase Gate

Rules:
- target 15-30 minutes
- place the slice at a representative midpoint, not a tutorial-only state
- define the internal proof gate first
- treat the external showcase gate as optional until internal proof passes
- beginners should finish the internal gate before optimizing for screenshots, trailers, or pitch use

### 14_PRODUCTION_PLAN.md

Purpose:
- define the project by phase using the unified phase model

Required sections for each phase:
- Goals
- Deliverables
- Not Included
- Done Criteria

Required phases:
- Phase 0: Pre-production
- Phase 1: Narrative and World Exploration
- Phase 2: Systems Prototype
- Phase 3: Vertical Slice Production
- Phase 4: Replan Based on Reality

Rules:
- keep the plan honest about what is excluded
- use done criteria that can be tested

### 15_TASK_BOARD.md

Purpose:
- track near-term work in a form simple enough to update constantly

Starter sections:
- This Week
- Next
- Blocked
- Later
- Done

Optional metadata for more complex projects:
- ID
- parent item
- owner
- status
- priority
- milestone
- estimate
- dependencies
- definition of done
- notes

Upgrade rule:
- start with the simple board
- add hierarchy only when multiple workstreams or collaboration make it necessary

Task writing rule:
- each task starts with a verb
- each task produces one visible result

### 16_RISK_LOG.md

Purpose:
- keep real project risks visible and reviewed

Required fields for each risk:
- Risk ID
- Title
- Description
- Category
- Probability
- Impact
- Mitigation
- Trigger or Warning Signs
- Owner
- Review Date
- Status
- Notes

Recommended categories:
- scope
- technical
- narrative
- art consistency
- workflow
- burnout
- legal and reference

Rules:
- record the trigger signs, not just the fear
- review risks regularly, not only when things go wrong

### DEV_LOG.md

Purpose:
- keep a running record of what actually happened during development

Suggested entry format:
- Date
- Planned Work
- What I Finished
- What Is Blocked
- New Ideas Captured
- Questions or Clarifications Needed
- Next Session Start Point

Rules:
- update it at the end of each work session
- use it to reduce restart friction and fake progress

## 9. AI Pipeline Docs

### 17_AI_PIPELINE.md

Purpose:
- define what AI may do, may not do, and how outputs move into canon

Required sections:
- Purpose
- Core Principle
- Approved Use Cases
- Disallowed or Cautious Use Cases
- Workflow
- Input Requirements
- Output Requirements
- Validation Rules
- File and Asset Tagging Rules
- Notes

Rules:
- human defines schema first
- AI output is candidate material until reviewed
- asset tagging must include tool, date, purpose, and status

### 18_PROMPT_LIBRARY.md

Purpose:
- store prompts as reusable project assets instead of rewriting them repeatedly

Required sections for each prompt:
- Prompt ID
- Name
- Purpose
- When to Use
- Required Inputs
- Output Format
- Prompt
- Example Input
- Example Output Summary
- Failure Modes
- Revision Notes
- Status

Rules:
- store only prompts that are reused
- revise prompts when they fail in predictable ways

### 19_CONTENT_REVIEW_RULES.md

Purpose:
- give AI outputs and human-created content a shared review standard

Required sections:
- Purpose
- Review Dimensions
- Review Questions
- Pass Rules
- Revise Rules
- Reject Rules
- Special Rules for AI Output
- Review Checklist
- Notes

Rules:
- reject content that is merely interesting but not useful
- require canon consistency and implementation value

## 10. Asset Docs

### 20_ASSET_REGISTRY.md

Purpose:
- track every production asset with enough metadata to use, replace, or ship it safely

Required fields:
- Asset ID
- Name
- Type
- Usage
- Location or Chapter
- Source Origin
- Tool or Author
- Rights Status
- Shipping Status
- AI Generated (Yes or No)
- Current Status
- Owner
- File Path
- Needs Revision (Yes or No)
- Notes

Recommended asset types:
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

Rules:
- every asset must have a clear use
- rights status must be explicit before the asset is considered shippable

### 21_ART_DIRECTION.md

Purpose:
- define the visual rules that guide production, review, and revision

Required sections:
- Art Pillars
- Overall Style
- Shape Language
- Color Logic
- Lighting Logic
- Texture and Surface Rules
- Character Visual Rules
- Environment Visual Rules
- UI Visual Rules
- Animation Feel
- Reference Anchors
- Do
- Don't
- Review Checklist
- Notes

Rules:
- art direction must be reproducible, not just inspirational
- avoid visual ambition that exceeds slice needs

### 22_AUDIO_DIRECTION.md

Purpose:
- define how sound supports story, space, tension, and gameplay readability

Required sections:
- Audio Pillars
- Music Strategy
- Ambience Strategy
- SFX Strategy
- Dialogue Audio Rules
- Silence Rules
- Location-Based Audio Notes
- Event Audio Notes
- Technical Notes
- Review Checklist
- Notes

Rules:
- sound should strengthen readability, not only mood
- define when silence is the right choice

## 11. Maintenance Rule

If you need to change what a project doc contains, update this file rather than restating the schema elsewhere.
