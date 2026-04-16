---
name: create-game-loop
description: >
  Creates the 03_GAME_LOOP.md game design document in an Obsidian vault using the GAME_PROJECT_SYSTEM methodology. Use this skill whenever the user runs `/create-game-loop <vault-path>`, asks to define their game loop, wants to describe what the player does, is working on core gameplay flow, or says things like "help me define my game loop", "what does the player do", "write a game loop doc", "create my core loop", "describe the gameplay cycle", or "I need to figure out my moment-to-moment gameplay". Even if the user hasn't said "game loop" explicitly — if they're trying to articulate what the player repeatedly does in their game, use this skill.
user-invocable: true
---

# Create Game Loop Document

## What This Is

The game loop document (`02_design/03_GAME_LOOP.md`) defines the structural, psychological, and emotional rhythms the player experiences. It answers what the player does, why it matters, and how the game responds.

This is not a systems spec or a features list. It's the heartbeat of the game, captured at five resolutions:

1. **Three-Tiered Loop** — the player's actions at second-to-second, minute-to-minute, and hour-to-hour timescales.
2. **Cognitive Cycle** — how the game communicates with the player's brain: mental model, system rules, feedback.
3. **Chains** — how repeated actions accumulate meaning (value, execution, secret).
4. **Pacing** — how tension and rest alternate.
5. **Goal Connections & Progression** — how short-term goals bridge to long-term ones, and how the game recovers from failure.

If the vision document says *what the game is*, the game loop says *what it feels like to play it, at every timescale*.

Keep it concrete. If a loop can't be acted out in your head, it's too abstract.

## Step 1: Parse the Vault Path

The user invoked this skill as `/create-game-loop <vault-path>`. Extract the vault path from their message. If no path was given, ask for it before continuing:

> "What's the path to your Obsidian vault? (e.g., `~/Vaults/MyGame`)"

Expand `~` to the full home directory path when writing the file.

### Check for Vision Document

Before starting the interview, check whether `<vault-path>/01_vision/01_VISION.md` exists. If it does, read it silently and use it as context throughout the interview — reference the elevator pitch, player fantasy, and emotional tone to ask sharper questions and catch contradictions. Do not recite the vision back to the user; just let it inform your questions.

If the vision document does not exist, proceed normally but mention that defining the vision first (via `/create-vision`) can help anchor the game loop.

## Step 2: Interview the User

Your goal is to fill in all 5 sections of the game loop template. Do this through a natural conversation, not a form. Move through the sections in order — the primary loop constrains the secondary, which constrains the tertiary, and the rest of the document builds on the three-tiered loop. When the user has already answered something implicitly, move on without re-asking.

If the user gives you everything upfront in a single message — a full description covering all five sections — skip the interview entirely and go straight to writing the file.

### 1. The Three-Tiered Loop

Break the core repetitive gameplay down by exact timescale.

- **Primary Loop (second-to-second)** — the fundamental, split-second action the player takes. Jumping, shooting, making a dialogue choice, dragging a card, pressing a button. Push for the actual verb and input, not a genre label. Ask: *"If you recorded the player's hands for three seconds, what would I see happening?"* Capture:
  - the action
  - the input that performs it
  - the intended feel (crunchy, floaty, deliberate, frantic)
  - how we'd know it feels right (a test the user can apply)

  Flag to the user that this loop must be perfected and feel incredibly satisfying to perform before anything else is built — everything else in the game rests on it.

- **Secondary Loop (minute-to-minute)** — how primary actions string together to achieve an immediate goal or overcome an obstacle. Finishing a level, completing a combat encounter, resolving a dialogue scene, clearing a room. Capture:
  - the goal unit (what "one unit of play" looks like)
  - which primary actions combine
  - typical duration
  - the completion signal the player sees

- **Tertiary Loop (hour-to-hour)** — the overarching objective that keeps the player engaged for long sessions. Saving the princess, upgrading a base, completing a story chapter, winning a run. Capture:
  - the long-session driver
  - what progress markers the player accumulates
  - the session hook — the reason to come back tomorrow

If the user struggles to separate the tiers, ask: *"Which tier is the one you'd be sad to lose?"* That usually reveals the identity of the game.

### 2. The Cognitive Cycle (Action & Feedback)

Define how the game communicates with the player's brain to prevent confusion. Walk through the primary action specifically:

- **Mental Model & Action** — what the player thinks they need to do, and the input they provide. This is the player's hypothesis about the game.
- **System Rules** — how the game actually processes that action. Any mismatch between mental model and system rules is a design risk worth naming.
- **Feedback & Interpretation** — the specific visual, audio, and system feedback that tells the player their action worked and lets them learn from it. Ask for all three channels separately — games get this wrong by relying on only one. Also ask: *what is the player meant to learn from this feedback?*

If the user can't say what the player learns from the feedback, the loop won't improve with practice — push on this.

### 3. Chains (Emotional & Meaningful Sequences)

Define how repetitive actions accumulate meaning and emotional weight.

- **Value Chains** — if the player collects resources, what specific highly-desired fantasy or object are they building toward? The thing that makes picking up "junk" feel meaningful. *"If I pick up a rusty nail, what great thing is it eventually part of?"*
- **Execution Chains** — strings of actions that raise emotional stakes as the player tries to complete them in order. Combo systems, multi-step stealth, nested dialogue choices, a clean speedrun of a section.
- **Secret Chains** — hidden, systemic sequences the player can stumble onto that make them feel smart when they piece them together. Emergent interactions, cross-system combinations, discoverable shortcuts.

Not every game has all three, but most good games have at least two. If the user says "none of these apply," push gently — value chains in particular are almost always present somewhere. If a chain genuinely does not apply, record that as an explicit design decision rather than silently skipping it.

### 4. Pacing: Action vs. Rest

Continuous tension leads to exhaustion. Map the rhythm.

- **Tension Sources** — what actively challenges the player: combat, puzzles, narrative stakes, social pressure, time pressure, resource scarcity, information gaps. Push for both mechanical tension (fail states, difficulty, resource management) and narrative tension (dramatic stakes, unanswered questions, characters at risk).
- **Moments of Rest** — where the player pauses, reflects on a victory or failure, breathes, and builds anticipation for the next challenge. Bonfires, base camps, cutscenes, safe rooms, hub towns, dialogue breathers.
- **Rhythm** — how tension and rest alternate over a typical session. A rough sketch is fine ("three tense encounters, then a hub visit, then a scripted narrative beat").

If the user describes only tension, ask where the rest lives. If they describe only rest, ask what the player actually recovers from.

### 5. Goal Connections and Progression

- **Short-Term to Long-Term Bridge** — how achieving an immediate goal naturally sets up the next one. At any moment there should be at least one clear goal pulling the player forward — the "one more turn" or "one more day" feeling. Ask: *"When the player finishes one secondary-loop unit, what pulls them into the next one without them having to stop and think?"*
- **Fail States** — what happens when the loop breaks by failure, and how the game invites the player back in. Capture the failure trigger, the consequence, the recovery path, and the re-engagement hook. If the user says "there are no fail states," push on what creates friction — every game has something that resists the player, and the game has to handle that resistance gracefully.

**Tone:** Be direct. Game loops are where vagueness is most dangerous — "the player explores and has fun" is not a loop. If an answer is abstract, ask for the specific sequence of actions. If a loop sounds identical to another game's loop, ask what makes this version distinct.

## Step 3: Write the File

Once you have enough to fill all 5 sections, write the file to `<vault-path>/02_design/03_GAME_LOOP.md`.

Use this exact template structure:

```md
# Game Loop

## 1. The Three-Tiered Loop

### Primary Loop (Second-to-Second)

[The fundamental split-second action — what the player does with their hands every few seconds.]

- Action:
- Input:
- Intended feel:
- How we know it feels right:

### Secondary Loop (Minute-to-Minute)

[How primary actions string together into one "unit of play" — a level, a fight, a scene.]

- Goal unit:
- Actions combined:
- Typical duration:
- Completion signal:

### Tertiary Loop (Hour-to-Hour)

[The overarching objective that carries a long session — the reason to stay engaged for an hour or more.]

- Long-session driver:
- Progress markers:
- Session hook:

## 2. The Cognitive Cycle (Action & Feedback)

### Mental Model & Action

[What the player thinks they need to do, and the input they provide.]

### System Rules

[How the game actually processes that action.]

### Feedback & Interpretation

- Visual feedback:
- Audio feedback:
- System / state feedback:
- What the player is meant to learn:

## 3. Chains (Emotional & Meaningful Sequences)

### Value Chains

[What "junk" resources are building toward — the fantasy that makes pickup feel meaningful. If not applicable, state that explicitly and why.]

### Execution Chains

[Sequences of actions that raise emotional stakes as the player tries to complete them in order.]

### Secret Chains

[Hidden, systemic sequences the player can stumble onto that make them feel smart when they piece them together.]

## 4. Pacing: Action vs. Rest

### Tension Sources

- [Mechanical tension source]
- [Narrative tension source]
- [At least 3 items total]

### Moments of Rest

- [Where and how the player rests]
- [At least 2 items]

### Rhythm

[One short paragraph or sequence sketching how tension and rest alternate in a typical session.]

## 5. Goal Connections and Progression

### Short-Term to Long-Term Bridge

[How one immediate goal naturally sets up the next — the "one more turn" hook.]

### Fail States

- Failure trigger:
- Consequence:
- Recovery path:
- Re-engagement hook:
```

**Writing rules:**

- Write in plain, declarative prose — no marketing language
- Every section must be filled; nothing blank or left as a placeholder
- The Primary Loop's action / input / feel block must name concrete verbs and inputs, not genres
- The Cognitive Cycle's three feedback channels (visual, audio, system / state) must each have an entry — no "TBD" on feedback
- For Chains: if a chain type genuinely does not apply to this game, write one sentence explaining why rather than deleting the section — absence is itself a design decision worth recording
- Tension Sources needs at least three items — push for both mechanical and narrative tension
- Moments of Rest needs at least two items
- Fail States must have all four fields filled — trigger, consequence, recovery path, re-engagement hook
- Total document length: aim for 80–150 lines. If it's much longer, move system-implementation details to `04_SYSTEMS.md`; if it's much shorter, the loops are probably underspecified
- If a vision document exists, the game loop must be consistent with it — but do not repeat information that belongs in the vision

After writing the file, confirm the path to the user and mention that this defines the core gameplay rhythm for all other design docs in `02_design/` (next up: `04_SYSTEMS.md`, which details the individual systems that make these loops work).
