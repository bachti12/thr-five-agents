# gpt-image-gen Skill & Yuval Agent

## Overview

`gpt-image-gen` is a reusable skill that wraps the OpenAI Images API (`gpt-image-2`), handling the curl call, base64 decode (with Python fallback for Git Bash on Windows), and file write. `yuval` is the project's creative agent — it scans `yuval/reference/` for visual inspiration, extracts style/palette/composition, crafts a coherent prompt, calls the skill, and saves the result to `yuval/outputs/` with a sibling `.txt` prompt log. Both live in `.claude/agents/yuval.md` (Claude Code sub-agent) and `agents/yuval.md` (CEO auto-discovery).

## Open Questions

- `gpt-image-2` model name used per user spec — verify this is the correct model ID if API returns 404.
- `yuval/reference/` is currently empty; visual consistency behavior is untested until first reference image is added.

## Session Log

### 2026-05-06 — Add gpt-image-gen skill and yuval creative agent [shipped]
- **What was done:** Created `.claude/skills/gpt-image-gen/SKILL.md` with curl + Python fallback commands. Created yuval agent definition at both `.claude/agents/yuval.md` and `agents/yuval.md` (identical content, hybrid design). Created `yuval/reference/` and `yuval/outputs/` directories (gitkeep) and pointer docs. Updated `agents/ceo_agent.md` with "סוכנים תחת פיקודך" section (yuval + trigger keywords) and יצירה ויזואלית domain row. Added `OPENAI_API_KEY` comment to `.env` and `.env.example`.
- **Decisions:** Hybrid file placement (`.claude/agents/` for Claude Code, `agents/` for CEO scan) keeps both discovery paths working without duplication logic. Python fallback added because `jq` is not reliably present in Git Bash on Windows.
- **Notes / Caveats:** `OPENAI_API_KEY` was already present in `.env` with a value — no key was added, only a section comment. Vault update deferred to final session step per obsidian-vault-workflow protocol.
- **Related:** [[ceo-agent-implementation]], [[bootstrap-project-structure]]
