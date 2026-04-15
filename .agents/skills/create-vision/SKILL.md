---
name: create-vision
description: >
  Creates the 01_VISION.md game design document in an Obsidian vault using the GAME_PROJECT_SYSTEM methodology. Use this skill whenever the user runs `/create-vision <vault-path>`, asks to create a game vision document, wants to define their game concept, is starting a new game project and needs to capture the vision, or says things like "help me define my game", "write a vision doc", "create a game concept document", or "I want to document what my game is about". Even if the user hasn't said "vision document" explicitly — if they're trying to articulate what their game is, use this skill.
user-invocable: true
---

# Create Vision Document

## What This Is

The vision document (`01_vision/01_VISION.md`) is the one-page definition of your game. It's not a design bible — it's a **decision filter**. Every other document in the project flows from it. When you're unsure whether to add a feature or cut one, you check this page.

Keep it short. Density beats length.

## Step 1: Parse the Vault Path

The user invoked this skill as `/create-vision <vault-path>`. Extract the vault path from their message. If no path was given, ask for it before continuing:

> "What's the path to your Obsidian vault? (e.g., `~/Vaults/MyGame`)"

Expand `~` to the full home directory path when writing the file.

## Step 2: Interview the User

Your goal is to fill in all 8 sections of the vision template. Do this through a natural conversation, not a form. Ask about a few things at once when they naturally connect. Listen for what the user has already answered implicitly.

If the user gives you everything upfront in a single message — a full description of their game — skip the interview entirely and go straight to writing the file.

**What to draw out:**

- **Elevator Pitch** — What is this game in one or two sentences? Not a genre label, but the actual concept. Push for specificity: "a puzzle game" isn't enough; "a puzzle game where you rewind a city block one minute at a time to prevent a murder" is.

- **Genre** — The formal genre label(s). This isn't a creative question — it's for orientation. 2D platformer, top-down RPG, narrative adventure, etc.

- **Player Fantasy** — What does the player get to *feel* or *be*? Not what they do mechanically, but the emotional role they inhabit. The powerful detective who always has one more lead. The last survivor who learns to trust. If the user gives you a mechanical answer, probe for the fantasy underneath it.

- **Emotional Tone** — The mood of the world. Not "fun" (that's too vague) — something like "melancholy, curious, tense" or "darkly comedic with moments of genuine warmth."

- **Why This Game Exists** — The honest reason it's being made. What drew the developer to this idea? What itch does it scratch? This is about motivation and meaning, not marketing.

- **What Makes It Distinct** — What's the specific angle that sets it apart? This should be concrete. "It's like X but with Y" is fine if it's accurate.

- **MVP Must Prove** — What must the vertical slice demonstrate? Offer the default items as a starting point and ask what else this specific game needs to prove.

- **This Game Is Not** — Explicit scope rejections. Help the user think about what they're *not* building. "Not an open world." "Not a combat-focused game." "Not a simulation." These are commitments that protect against scope creep.

**Tone:** Be direct. If an answer is vague, say so and ask a sharper follow-up. The vision document only works if it's honest and specific.

## Step 3: Write the File

Once you have enough to fill all 8 sections, write the file to `<vault-path>/01_vision/01_VISION.md`.

Use this exact template structure:

```md
# Vision

## Elevator Pitch
[1–2 sentences. The concept, not a genre label.]

## Genre
[Genre labels]

## Player Fantasy
[The emotional role the player inhabits]

## Emotional Tone
[The mood — specific, not generic]

## Why This Game Exists
[The honest motivation]

## What Makes It Distinct
[The specific angle]

## MVP Must Prove
- [ ] The setting is compelling
- [ ] The core loop works
- [ ] The art and writing direction feel coherent
- [ ] The solo + AI workflow is sustainable
[Add game-specific proof points from the interview]

## This Game Is Not
- [Explicit non-goal or scope rejection]
- [Another thing it's not]
```

**Writing rules:**
- Write in plain, declarative prose — no marketing language
- Every section must be filled; nothing blank or left as a placeholder
- "This Game Is Not" needs at least two items — push for three if the scope is ambitious
- The MVP checklist should have the four defaults plus any game-specific additions the user identified
- Total document length: aim for 20–40 lines. If it's longer, something is probably a design doc that belongs elsewhere

After writing the file, confirm the path to the user and mention that this is the foundation for all other docs in the `01_vision/` folder (next up: `02_DESIGN_PILLARS.md`).
