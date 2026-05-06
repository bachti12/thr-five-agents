# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## הוראה קריטית

בכל שיחה, בכל משימה, בכל בקשה — קרא תמיד את `agents/ceo_agent.md` ופעל לפי הוראותיו. המנכ"ל הוא נקודת הכניסה היחידה לכל פעולה במערכת.

## Project Overview

A multi-agent content-creation system. A **CEO agent** orchestrates a team of specialised content agents, delegating tasks and synthesising their output into a final deliverable. The individual agents and their roles will be defined as the project evolves.

## Session Protocol

**At the start of every session and after every significant command:** invoke the `.claude/skills/obsidian-vault-workflow` skill.
This skill reads `vault/00-INDEX.md` to load project context, and writes a dated session entry to `vault/Meeting Notes/` when the task completes.

## Claude Configuration

Custom agents, skills, and slash commands for this project live under `.claude/`:

| Folder | Purpose |
|--------|---------|
| `.claude/agents/` | Sub-agent definitions (system prompts, tool configs) |
| `.claude/skills/` | Reusable skill files invoked by agents |
| `.claude/commands/` | Project-specific slash commands |
