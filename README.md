# game-stack

A collection of Claude skills for solo game developers, built around the [GAME_PROJECT_SYSTEM](docs/GAME_PROJECT_SYSTEM.md) methodology — a practical, AI-native workflow for turning vague game ideas into structured, finishable projects.

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

## Installation

### Claude Code

Project-local skills in `.claude/skills/` are loaded automatically when Claude Code is running inside this directory. Clone the repo and the skills are available immediately.

```bash
git clone <this-repo> game-stack
cd game-stack
# Open Claude Code here — skills load automatically
```

Then invoke any skill from the Claude Code prompt:
```
/create-vision ~/Vaults/MyGame
```

### Codex / Claude.ai

Codex doesn't auto-load project skills, but you can use the skill manually by uploading or pasting the skill file's contents into your conversation. Each skill lives in `.claude/skills/<skill-name>/SKILL.md`.

1. Open `.claude/skills/create-vision/SKILL.md`
2. Paste its contents into the system prompt or at the start of your conversation
3. Then use the skill as described above

---

## Reference

The underlying methodology lives in [`docs/GAME_PROJECT_SYSTEM.md`](docs/GAME_PROJECT_SYSTEM.md) — a full guide covering document structure, development phases, AI pipeline rules, and solo workflow patterns for story-driven 2D games.
