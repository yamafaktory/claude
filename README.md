# claude

My personal Claude Code setup: global instructions, settings and skills.

| File | Purpose |
|---|---|
| `CLAUDE.md` | Global instructions for every session |
| `settings.json` | Claude Code settings and the rtk hook |
| `skills/clear-writing` | Writes prose in Simplified Technical English |

## Install

Install [rtk](https://github.com/rtk-ai/rtk) first. The hook in `settings.json` calls it, and `rtk init -g` writes the `RTK.md` that `CLAUDE.md` loads.

```sh
git clone git@github.com:yamafaktory/claude.git ~/dev/claude
ln -sf ~/dev/claude/CLAUDE.md ~/.claude/CLAUDE.md
ln -sfn ~/dev/claude/skills/clear-writing ~/.claude/skills/clear-writing
cp ~/dev/claude/settings.json ~/.claude/settings.json
rtk init -g
```

Copy `settings.json` instead of linking it, because Claude Code rewrites the file at runtime.
