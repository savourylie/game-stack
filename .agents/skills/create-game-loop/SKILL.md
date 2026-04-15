---
name: create-game-loop
description: >
  Creates the 03_GAME_LOOP.md game design document in an Obsidian vault using the GAME_PROJECT_SYSTEM methodology. Use this skill whenever the user runs `/create-game-loop <vault-path>`, asks to define their game loop, wants to describe what the player does, is working on core gameplay flow, or says things like "help me define my game loop", "what does the player do", "write a game loop doc", "create my core loop", "describe the gameplay cycle", or "I need to figure out my moment-to-moment gameplay". Even if the user hasn't said "game loop" explicitly — if they're trying to articulate what the player repeatedly does in their game, use this skill.
user-invocable: true
---

# Create Game Loop Document

## What This Is

The game loop document (`02_design/03_GAME_LOOP.md`) defines what the player actually does — second to second, session to session, and across the whole game. It's not a systems spec or a features list. It's the heartbeat of the game: the repeating actions, the tension that makes those actions matter, and the rewards that pull the player back in.

If the vision document says *what the game is*, the game loop says *what it feels like to play it*.

Keep it concrete. If a loop can't be acted out in your head, it's too abstract.

## Step 1: Parse the Vault Path

The user invoked this skill as `/create-game-loop <vault-path>`. Extract the vault path from their message. If no path was given, ask for it before continuing:

> "What's the path to your Obsidian vault? (e.g., `~/Vaults/MyGame`)"

Expand `~` to the full home directory path when writing the file.

### Check for Vision Document

Before starting the interview, check whether `<vault-path>/01_vision/01_VISION.md` exists. If it does, read it silently and use it as context throughout the interview — reference the elevator pitch, player fantasy, and emotional tone to ask sharper questions and catch contradictions. Do not recite the vision back to the user; just let it inform your questions.

If the vision document does not exist, proceed normally but mention that defining the vision first (via `/create-vision`) can help anchor the game loop.

## Step 2: Interview the User

Your goal is to fill in all 5 sections of the game loop template. Do this through a natural conversation, not a form. Ask about a few things at once when they naturally connect. Listen for what the user has already answered implicitly.

If the user gives you everything upfront in a single message — a full description of their game's loops, tension, and rewards — skip the interview entirely and go straight to writing the file.

**What to draw out:**

- **Moment-to-Moment Loop** — What does the player do every few seconds? This is the most granular level: move, look, interact, talk, fight, solve, hide, build — whatever the core verbs are. The methodology suggests defaults (Move, Observe, Interact, Converse, Solve/evade/discover) as a starting point for exploration-style games. Use those to prompt the user if their game leans that way, but replace them entirely with whatever fits their game. If their game is a deckbuilder, the moment-to-moment loop is drawing, playing, and resolving cards — not walking and observing. Push for the actual verbs, not genre labels.

- **Short Loop** — What does one play session or one quest feel like as a cycle? This is the "mission-level" or "chapter-level" rhythm. Examples: receive a lead, investigate a location, confront an NPC, make a choice, see consequences. Or: enter a dungeon, explore rooms, fight a boss, collect loot, return to town. The short loop should describe a complete arc the player repeats many times throughout the game. If the user describes a one-time event, push for the repeating pattern underneath it.

- **Long Loop** — What is the arc across the whole game? How does the player's situation change from beginning to end? This covers progression: unlocking areas, gaining abilities, building relationships, uncovering the central mystery, shifting the world state. The long loop is what gives the short loop meaning over time. If the user struggles here, ask: "If you watched someone play your game from start to finish on fast-forward, what would you see changing?"

- **Sources of Tension** — What makes the player care? What creates stakes, pressure, or uncertainty? This is not just "enemies can kill you." Tension can come from time pressure, social consequences, moral dilemmas, resource scarcity, information gaps, fragile relationships, or the threat of losing progress. Ask for both mechanical tension (fail states, resource management, difficulty) and narrative tension (dramatic stakes, unanswered questions, characters at risk). If the user says "there are no fail states," push on what creates difficulty or friction — every game has something that resists the player.

- **Rewards** — What does the player get for engaging with the loops? Cover both extrinsic rewards (items, abilities, new areas, story reveals, relationship progress) and intrinsic rewards (the satisfaction of solving something, the emotional payoff of a conversation, the pleasure of mastering a system). If the user only lists loot, ask what the *emotional* reward is. If they only describe feelings, ask what the *concrete* reward is. A good reward structure has both.

**Tone:** Be direct. Game loops are where vagueness is most dangerous — "the player explores and has fun" is not a loop. If an answer is abstract, ask for the specific sequence of actions. If a loop sounds identical to another game's loop, ask what makes this version distinct.

## Step 3: Write the File

Once you have enough to fill all 5 sections, write the file to `<vault-path>/02_design/03_GAME_LOOP.md`.

Use this exact template structure:

```md
# Game Loop

## Moment-to-Moment Loop

- [Core verb 1]
- [Core verb 2]
- [Core verb 3]
- [Core verb 4]
- [Core verb 5 — add or remove items to match the game]

## Short Loop

[One paragraph or a short sequence describing the repeating session-level cycle. What does the player do from the start of a "unit of play" to its resolution?]

## Long Loop

[One paragraph or a short sequence describing how the game evolves across its full arc. What changes, what accumulates, what shifts?]

## Sources of Tension

- [Mechanical or narrative tension source]
- [Another tension source]
- [At least 3 items]

## Rewards

- [Extrinsic reward]
- [Intrinsic reward]
- [At least 3 items covering both types]
```

**Writing rules:**
- Write in plain, declarative prose — no marketing language
- Every section must be filled; nothing blank or left as a placeholder
- Moment-to-Moment Loop should have 3–7 concrete verbs or actions, not vague categories
- Short Loop and Long Loop should each be 2–5 sentences or a clear sequence — enough to be useful, short enough to scan
- Sources of Tension needs at least three items — push for both mechanical and narrative tension
- Rewards needs at least three items — push for both extrinsic and intrinsic rewards
- Total document length: aim for 25–50 lines. If it's longer, the loops are probably overspecified — move system details to `04_SYSTEMS.md`
- If a vision document exists, the game loop should be consistent with it — but do not repeat information that belongs in the vision

After writing the file, confirm the path to the user and mention that this defines the core gameplay rhythm for all other design docs in `02_design/` (next up: `04_SYSTEMS.md`, which details the individual systems that make these loops work).
