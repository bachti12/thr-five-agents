---
tags: [infrastructure, agents, ceo]
aliases: [agents/, agents-root]
associated_with: [ceo-agent, agents-folder, claude-md]
---

# agents/ (שורש הפרויקט)

## What it does
תיקיית הגדרות הסוכנים של המערכת — **שונה מ-`.claude/agents/`**. מכילה קבצי `.md` אחד לכל סוכן. המנכ"ל (CEO Agent) סורק תיקייה זו בתחילת כל משימה ובונה מפת יכולות דינמית. הוספת קובץ חדש מספיקה להרחבת המערכת — אין צורך לעדכן את `ceo_agent.md`.

## Associated with
- [[ceo-agent]] — קורא ומנהל את כל הסוכנים בתיקייה זו
- [[agents-folder]] — `.claude/agents/` — תשתית Claude Code נפרדת, לא קשורה
- [[claude-md]] — מכיל דירקטיבה לקריאת `agents/ceo_agent.md`

## תוכן נוכחי
- `ceo_agent.md` — system prompt של המנכ"ל (orchestrator)
- `agent_template.md` — תבנית לסוכנים עתידיים

## Notes
**הבחנה קריטית:**
- `agents/` (שורש) = הגדרות ה-agents שהמנכ"ל מנהל — **כאן**
- `.claude/agents/` = תשתית Claude Code לhפעלת sub-agents — **לא נוגעים**
