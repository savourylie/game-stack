---
name: create-vision
description: >
  Creates the 01_VISION.md game design document (and optionally 02_DESIGN_PILLARS.md) in an Obsidian vault using the GAME_PROJECT_SYSTEM methodology. Use this skill whenever the user runs `/create-vision <vault-path>`, asks to create a game vision document, wants to define their game concept, wants to capture design pillars for their game, is starting a new game project and needs to capture the vision, or says things like "help me define my game", "write a vision doc", "create a game concept document", "define my game's pillars", or "I want to document what my game is about". Even if the user hasn't said "vision document" or "pillars" explicitly — if they're trying to articulate what their game is or what principles should govern its design, use this skill.
user-invocable: true
---

# Create Vision Document

## What This Is

This skill produces up to two files in the `01_vision/` folder of an Obsidian vault:

- **`01_VISION.md`** — always created. The one-page definition of your game. Not a design bible — a **decision filter**. Every other document in the project flows from it. When you're unsure whether to add a feature or cut one, you check this page.
- **`02_DESIGN_PILLARS.md`** — optional, offered after the vision is written. The 3–5 principles that help you reject bad ideas and resolve close calls. Can be deferred and added later once the concept has settled.

Keep both short. Density beats length.

## Step 1: Parse the Vault Path

The user invoked this skill as `/create-vision <vault-path>`. Extract the vault path from their message. If no path was given, ask for it before continuing:

> "What's the path to your Obsidian vault? (e.g., `~/Vaults/MyGame`)"

Expand `~` to the full home directory path when writing files.

## Step 2: Interview for the Vision

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

## Step 3: Write the Vision File

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

Confirm the vision file path to the user, then move to Step 4.

## Step 4: Offer Pillars (or Defer)

After the vision file is written, ask whether to also define design pillars now:

> "Want to capture your design pillars now? These are the 3–5 principles you'll use to reject bad ideas when scope creeps and to resolve close calls. You can also defer this and add them later once the concept settles — just say 'skip' or 'later'."

If the user defers, stop here. Confirm the vision is done and let them know `02_DESIGN_PILLARS.md` can be added later by running `/create-vision` again or by editing the file directly.

If the user wants to continue, move to Step 5.

## Step 5: Interview for the Pillars

Design pillars are the 3–5 principles that:

- help reject bad ideas when scope creeps
- resolve close calls when two designs compete
- are concrete enough to be actionable, not vague values

**Target: 3–5 pillars.** Fewer than 3 and you don't have a real filter. More than 5 and they can't be held in the head during real decisions.

For each pillar, draw out:

- **Name** — A short, memorable label. Not abstract ("Quality") — pointed ("Every System Teaches").
- **Statement** — One sentence that states the principle clearly. Example: "The player should always understand why they lost."
- **Why It Matters** — The trap this pillar protects against. What would break if it were ignored.
- **Design Implications** — How this pillar actually changes decisions in practice. Be concrete.
- **What It Encourages** — The kinds of features, systems, or content this pillar welcomes.
- **What It Rejects** — The kinds of ideas this pillar blocks. **If a pillar rejects nothing, it's a slogan, not a pillar.**

Then, across all the pillars together:

- **Conflict Resolution Rule** — When two pillars point in different directions, how do you decide? Example: "When readability and depth conflict, readability wins."
- **Scope Control Rule** — How do the pillars govern scope? Example: "Any feature that doesn't serve at least two pillars is out of scope."
- **Review Checklist** — 3–5 questions the developer will ask when reviewing a new feature, system, or piece of content against the pillars.
- **Notes** — Anything else worth remembering: origins, revisions, open questions.

**Tone:** Be direct. Push back on any proposed pillar that doesn't reject something concrete. A pillar that only welcomes ideas isn't a pillar — it's a mission statement.

## Step 6: Write the Pillars File

Once the pillars are defined, write the file to `<vault-path>/01_vision/02_DESIGN_PILLARS.md`.

Use this exact template structure:

```md
# Design Pillars

## Pillar 1: [Name]

**Statement:** [One sentence]

**Why It Matters:** [The trap this avoids]

**Design Implications:** [How this changes decisions in practice]

**What It Encourages:**
- [Item]
- [Item]

**What It Rejects:**
- [Item]
- [Item]

## Pillar 2: [Name]

[same structure]

## Pillar 3: [Name]

[same structure]

## Conflict Resolution Rule
[When pillars compete, how you decide]

## Scope Control Rule
[How pillars govern scope]

## Review Checklist
- [ ] [Question 1]
- [ ] [Question 2]
- [ ] [Question 3]

## Notes
[Anything else worth remembering]
```

**Writing rules:**
- Use 3–5 pillars. No fewer, no more.
- Every pillar must reject something concrete — if the "What It Rejects" section is empty or vague, the pillar isn't doing work.
- Pillars should be memorable and actionable, not aspirational.
- Keep each pillar tight: a few lines per section, not paragraphs.

After writing the pillars file, confirm both paths to the user and note that the `01_vision/` folder foundation is now complete. The next canonical doc is `03_GAME_LOOP.md`, which can be created with `/create-game-loop`.
