---
tags: [config, secrets]
aliases: [.env, .env.example]
associated_with: [gitignore]
---

# Environment Configuration

## What it does
שני קבצים משלימים:
- **`.env`** — המפתחות האמיתיים (לא עולה ל-git). מכיל `ANTHROPIC_API_KEY` ו-`CLAUDE_MODEL`.
- **`.env.example`** — תבנית ריקה לשיתוף עם צוות. עולה ל-git.

## Associated with
- [[gitignore]] — `.env` מוחרג על ידי `.gitignore`
- [[claude-md]] — `CLAUDE_MODEL` קובע את המודל שבו משתמשים ה-agents

## Notes
`ANTHROPIC_API_KEY` חובה למשימות כל ה-agents. ברירת המחדל של המודל: `claude-sonnet-4-6`.
