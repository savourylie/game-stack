# GAME PROJECT SKILL CREATION

This document defines how to design AI skills that fit the GAME_PROJECT_SYSTEM.

It does not redefine the project workflow. Use:

- [GAME_PROJECT_FULL_SYSTEM.md](GAME_PROJECT_FULL_SYSTEM.md) for the phase model
- [GAME_PROJECT_TEMPLATES.md](GAME_PROJECT_TEMPLATES.md) for canonical docs
- [GAME_PROJECT_SOLO_PRACTICAL_MODE.md](GAME_PROJECT_SOLO_PRACTICAL_MODE.md) for the lightweight day-to-day mode

## 1. Purpose

Skills should help a solo developer do one of three things well:

1. Clarify
2. Convert
3. Review

If a skill tries to run the entire project at once, it usually becomes vague and noisy.

## 2. Core Design Rule

Build focused, phase-specific skills instead of one giant generalist agent.

Why:

- the questions are different in each phase
- the needed output format is different in each phase
- the right level of pushback is different in each phase
- smaller skills are easier to trust, test, and revise

## 3. Skill Boundaries

Each skill should have a clear job and a clear boundary.

It should know:

- when it is allowed to act
- which canonical docs it reads
- which artifacts it is allowed to create or update
- what it must not decide on its own

Skills should not invent parallel project memory outside the canonical docs and repo.

## 4. Canon Integration Rule

Every skill must respect the canonical source rule.

That means:

- read from canonical docs when grounding context
- return outputs in a format that can be merged into canonical docs
- avoid creating duplicate sources of truth
- mark draft material clearly until the human accepts it

If a skill produces something useful, the next step is to merge it into canon, not to keep it floating in chat forever.

## 5. Recommended Skills by Phase

### Concept Architect

Used in:
- Phase 0

Job:
- turn rough ideas into a clear concept and initial slice target

Inputs:
- raw premise
- references
- emotional tone
- constraints

Outputs:
- one-sentence concept
- design pillars
- MVP proof statement
- early slice candidates

### Slice Planner

Used in:
- late Phase 0
- Phase 3 planning

Job:
- convert the chosen idea into an actionable slice

Inputs:
- vision
- game loop
- early systems

Outputs:
- slice spec
- must-have systems
- content list
- out-of-scope list
- weekly priorities

### Systems Co-Designer

Used in:
- Phase 2

Job:
- define and implement gameplay systems one by one

Inputs:
- target system
- engine context
- constraints
- codebase conventions

Outputs:
- system spec
- edge cases
- state transitions
- implementation checklist
- test checklist

### Narrative Room

Used in:
- Phase 1
- Phase 3 content work

Job:
- generate and refine story content while preserving canon

Inputs:
- canonical story docs
- character cards
- scene purpose
- tone constraints

Outputs:
- scene outlines
- dialogue candidates
- quest structures
- contradiction warnings

### Asset Director

Used in:
- Phase 3
- later production

Job:
- turn scene and content needs into production-ready asset briefs

Inputs:
- gameplay use
- art direction
- technical constraints
- slice needs

Outputs:
- asset lists
- naming suggestions
- prompts or briefs
- revision checklists
- integration notes

### Solo Producer

Used in:
- all phases, especially weekly planning

Job:
- keep the developer focused on the slice and current milestone

Inputs:
- current milestone
- recent progress
- blockers
- open decisions

Outputs:
- trimmed weekly plan
- priority order
- cut suggestions
- risk reminders
- next steps

## 6. Recommended Build Order

Create skills in this order:

1. Concept Architect
2. Slice Planner
3. Solo Producer
4. Systems Co-Designer
5. Narrative Room
6. Asset Director

Reason:

- the biggest early failure is lack of definition, not lack of implementation power
- the Slice Planner is the highest-leverage first skill because it teaches the project how to repeatedly convert idea into slice, slice into plan, and plan into finished chunk

## 7. Interaction Style Rules

Each skill should match its job.

Examples:

- Concept Architect should challenge vagueness and force compression
- Slice Planner should cut fake scope and expose dependencies
- Systems Co-Designer should think in terms of input, state, failure, and testability
- Narrative Room should prefer structured outputs over prose dumps
- Asset Director should focus on production readiness, not inspiration alone
- Solo Producer should be strict about focus and anti-chaos

## 8. Skill Design Template

Use this template when creating a new skill:

```md
# Skill Name

## Purpose
What this skill helps decide or produce.

## When to Use
Which phase or situation triggers it.

## Reads From Canon
Which project docs or repo areas it should inspect first.

## Inputs
What the user must provide.

## Outputs
What artifacts the skill should produce.

## Writes or Updates
Which canonical docs or files it may update.

## Boundaries
What the skill must not do.

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

## Review Checklist
- Did it read the right canonical context?
- Did it stay inside its boundary?
- Did it produce something mergeable into canon?
- Did it reduce ambiguity rather than add it?
```

## 9. Review Rules for Skills

A good skill should:

- read the minimum relevant canon before acting
- ask the right questions for its phase
- return structured outputs
- support direct merging into docs or tasks
- surface contradictions explicitly

A bad skill usually:

- tries to own too many phases
- writes long generic prose
- ignores canonical context
- creates new terminology or file structures casually
- produces output with no clear next action

## 10. Practical First Implementation

If you build only one skill first, build `Slice Planner`.

It sits on the biggest leverage point in the whole system:

`idea -> slice spec -> weekly plan -> finished chunk`

If that conversion loop works, the project survives. If it does not, better writing or better code generation will not rescue it.
