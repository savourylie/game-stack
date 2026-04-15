---
name: "upgrade-game-stack"
description: "Use when the user explicitly asks to upgrade game-stack to the latest version from GitHub. Prefer explicit invocation with $upgrade-game-stack."
---

# Upgrade game-stack

Pull the latest game-stack skills from GitHub and update the local installation. Treat this as an explicit workflow skill. Do not trigger it just because a user mentioned upgrading in passing.

## Workflow

1. Detect the game-stack install type by checking these locations in order:
   - `$HOME/.claude/plugins/marketplaces/game-stack/.git` — if this directory exists, the install type is **plugin-marketplace** and the game-stack root is `$HOME/.claude/plugins/marketplaces/game-stack`.
   - The current git repo root (via `git rev-parse --show-toplevel`) with a remote URL containing `game-stack` — if this matches, the install type is **git-clone** and the game-stack root is the repo root.
   - If neither is found, report that no game-stack git installation was found. Suggest installing via the Claude Code plugin marketplace or cloning from `https://github.com/savourylie/game-stack`.

2. Record the current commit hash before upgrading:
   ```
   git -C <GAME_STACK_DIR> rev-parse HEAD
   ```

3. Pull the latest version:
   ```
   cd <GAME_STACK_DIR> && git fetch origin && git pull origin main
   ```
   If already up to date, say so and stop.

4. For **plugin-marketplace** installs only: sync the updated files to the plugin cache directory at `$HOME/.claude/plugins/cache/game-stack/game-stack/<version>/` (excluding `.git`).

5. Show the user what changed:
   - Previous commit vs new commit (short hashes)
   - `git log --oneline <OLD_HEAD>..HEAD`
   - For plugin-marketplace installs: note that a Claude Code restart may be needed.

## Safety Rules

- Do not modify any files outside the game-stack installation directory.
- Do not force-push or reset. Use `git pull` only.
- If the pull fails due to local changes, report the error and stop instead of discarding changes.
