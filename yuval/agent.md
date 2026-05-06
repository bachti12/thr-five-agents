# yuval — Agent Pointer Doc

This file is for humans navigating the repo. It is **not** parsed by Claude Code.

## Canonical agent definitions

| Location | Purpose |
|----------|---------|
| [`agents/yuval.md`](../agents/yuval.md) | Discovered by the CEO orchestrator (`agents/*.md` scan) |
| [`.claude/agents/yuval.md`](../.claude/agents/yuval.md) | Loaded by Claude Code as a sub-agent |

Both files contain identical content.

## Working directories

| Directory | Purpose |
|-----------|---------|
| `yuval/reference/` | Drop inspiration images here (PNG, JPG, JPEG, WEBP). Yuval reads them before generating. |
| `yuval/outputs/` | Generated images land here, named `YYYY-MM-DD-<slug>.png` with a sibling `.txt` prompt log. |
