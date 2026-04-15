# game-stack

A collection of Claude skills for solo game developers, built around the [GAME_PROJECT_SYSTEM](docs/GAME_PROJECT_SYSTEM.md) methodology — a practical, AI-native workflow for turning vague game ideas into structured, finishable projects.

---

## Installation

### Claude Code

```
/plugin marketplace add savourylie/game-stack
/plugin install game-stack@savourylie
```

### Codex / Claude.ai

```
$skill-installer install https://github.com/savourylie/game-stack/tree/main/.agents/skills/create-vision
```

No `$skill-installer`? Open `skills/create-vision/SKILL.md` and paste its contents into your system prompt or at the start of your conversation.

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

---

## Reference

The underlying methodology lives in [`docs/GAME_PROJECT_SYSTEM.md`](docs/GAME_PROJECT_SYSTEM.md) — a full guide covering document structure, development phases, AI pipeline rules, and solo workflow patterns for story-driven 2D games.
