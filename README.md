# game-stack

A collection of Claude skills for solo game developers, built around the [GAME_PROJECT_SYSTEM](docs/GAME_PROJECT_SYSTEM.md) methodology — a practical, AI-native workflow for turning vague game ideas into structured, finishable projects.

---

## Installation

### Claude Code

**Step 1** — add the marketplace:
```
/plugin marketplace add savourylie/game-stack
```

**Step 2** — install the plugin:
```
/plugin install game-stack@savourylie
```

### Codex / Claude.ai

```
$skill-installer install https://github.com/savourylie/game-stack/tree/main/.agents/skills/create-vision
```

```
$skill-installer install https://github.com/savourylie/game-stack/tree/main/.agents/skills/create-game-loop
```

No `$skill-installer`? Open the SKILL.md files in `skills/` and paste their contents into your system prompt or at the start of your conversation.

---

## Skills

### `/create-vision`

Guides you through creating `01_vision/01_VISION.md` in your Obsidian vault — the one-page definition of your game that everything else flows from.

**Usage:**
```
/create-vision <path-to-obsidian-vault>
```

**What it does:**
- Interviews you conversationally to draw out your game concept (or skips straight to writing if you describe everything upfront)
- Creates `<vault>/01_vision/01_VISION.md` with all required sections filled in:
  - Elevator Pitch, Genre, Player Fantasy, Emotional Tone
  - Why This Game Exists, What Makes It Distinct
  - MVP Must Prove (checklist), This Game Is Not

**Example:**
```
/create-vision ~/Vaults/MyGame
```

### `/create-game-loop`

Guides you through creating `02_design/03_GAME_LOOP.md` in your Obsidian vault — defines what the player actually does, from second-to-second actions to the full-game arc.

**Usage:**
```
/create-game-loop <path-to-obsidian-vault>
```

**What it does:**
- Reads your vision doc (if it exists) for context
- Interviews you to define the gameplay rhythm (or skips straight to writing if you describe everything upfront)
- Creates `<vault>/02_design/03_GAME_LOOP.md` with all required sections filled in:
  - Moment-to-Moment Loop, Short Loop, Long Loop
  - Sources of Tension, Rewards

**Example:**
```
/create-game-loop ~/Vaults/MyGame
```

---

## Reference

The underlying methodology lives in [`docs/GAME_PROJECT_SYSTEM.md`](docs/GAME_PROJECT_SYSTEM.md) — a full guide covering document structure, development phases, AI pipeline rules, and solo workflow patterns for story-driven 2D games.
