# game-stack

A collection of Claude skills for solo game developers, built around the [GAME_PROJECT_SYSTEM](docs/GAME_PROJECT_SYSTEM.md) methodology — a practical, AI-assisted workflow for turning vague game ideas into structured, finishable projects.

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

```
$skill-installer install https://github.com/savourylie/game-stack/tree/main/.agents/skills/create-vertical-slice
```

```
$skill-installer install https://github.com/savourylie/game-stack/tree/main/.agents/skills/upgrade-game-stack
```

No `$skill-installer`? Open the SKILL.md files in `skills/` and paste their contents into your system prompt or at the start of your conversation.

---

## Skills

| Skill | What it does | Usage |
|-------|-------------|-------|
| `/create-vision` | Creates your game's one-page vision document in Obsidian | `/create-vision <vault-path>` |
| `/create-game-loop` | Creates the gameplay rhythm document (moment-to-moment → full arc) | `/create-game-loop <vault-path>` |
| `/create-vertical-slice` | Scopes your first playable target — the 15–30 min slice that proves the game and the workflow | `/create-vertical-slice <vault-path>` |
| `/upgrade-game-stack` | Pulls the latest skills from GitHub and updates your local install | `/upgrade-game-stack` |

---

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
  - Three-Tiered Loop (primary / secondary / tertiary)
  - Cognitive Cycle (action and feedback)
  - Chains (value / execution / secret)
  - Pacing (tension vs. rest)
  - Goal Connections and Progression

**Example:**
```
/create-game-loop ~/Vaults/MyGame
```

### `/create-vertical-slice`

Guides you through creating `05_production/13_VERTICAL_SLICE.md` in your Obsidian vault — the scoped definition of one short, playable section that proves both the game (core loop, systems, feel) and the workflow (solo + AI production pipeline, end to end).

**Usage:**
```
/create-vertical-slice <path-to-obsidian-vault>
```

**What it does:**
- Reads your vision and game loop docs (both required) for context
- Interviews you to lock the slice scope, validate loop and chain claims, and identify must-have systems and out-of-scope features (or skips straight to writing if you describe everything upfront)
- Pushes back on common slice mistakes — building a tutorial instead of a midpoint, vague acceptance criteria, missing layers in the "slice of cake"
- Creates `<vault>/05_production/13_VERTICAL_SLICE.md` with all required sections filled in:
  - Target Scope & Scenario (duration, location, characters, midpoint position, 60/40 feature balance, narrative beats)
  - Loop & Chain Validation
  - Required Implementation (must-have systems, content, explicit out-of-scope list)
  - Layer Coverage ("slice of cake" — art, UI, sound, mechanics, narrative at shipping fidelity)
  - Workflow & Pipeline Proof
  - Acceptance Criteria (Internal Proof Gate + optional External Showcase Gate)
- Optionally seeds `<vault>/05_production/15_TASK_BOARD.md` with the first slice-critical tasks so work can begin the same day

**Example:**
```
/create-vertical-slice ~/Vaults/MyGame
```

### `/upgrade-game-stack`

Pulls the latest skills from GitHub and updates your local installation. Works with both Claude Code plugin installs and direct git clones. Run this whenever new skills are added to the repo.

**Usage:**
```
/upgrade-game-stack
```

**What it does:**
- Detects whether you installed via the Claude Code plugin marketplace or a git clone
- Runs `git pull` to fetch the latest skills
- Syncs the plugin cache (for marketplace installs)
- Reports what changed, and reminds you to restart Claude Code if needed

---

## Reference

The methodology starts at [`docs/GAME_PROJECT_SYSTEM.md`](docs/GAME_PROJECT_SYSTEM.md) and is split into an index, a full system guide, a canonical template reference, a solo practical mode guide, and a skill-creation guide.
