# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A multi-agent content-creation system. A **CEO agent** orchestrates a team of specialised content agents, delegating tasks and synthesising their output into a final deliverable. The individual agents and their roles will be defined as the project evolves.

## Claude Configuration

Custom agents, skills, and slash commands for this project live under `.claude/`:

| Folder | Purpose |
|--------|---------|
| `.claude/agents/` | Sub-agent definitions (system prompts, tool configs) |
| `.claude/skills/` | Reusable skill files invoked by agents |
| `.claude/commands/` | Project-specific slash commands |
