# claude

My personal Claude Code setup: global instructions, settings and skills.

| File | Purpose |
|---|---|
| `CLAUDE.md` | Global instructions for every session |
| `RTK.md` | Notes on rtk, the token saving CLI proxy, loaded from `CLAUDE.md` |
| `settings.json` | Claude Code settings and the rtk hook |
| `skills/clear-writing` | Writes prose in Simplified Technical English |

## Install

```sh
git clone git@github.com:yamafaktory/claude.git ~/dev/claude
ln -sf ~/dev/claude/CLAUDE.md ~/.claude/CLAUDE.md
ln -sf ~/dev/claude/RTK.md ~/.claude/RTK.md
ln -sfn ~/dev/claude/skills/clear-writing ~/.claude/skills/clear-writing
cp ~/dev/claude/settings.json ~/.claude/settings.json
```

Copy `settings.json` instead of linking it, because Claude Code rewrites the file at runtime.
