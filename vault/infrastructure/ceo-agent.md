---
tags: [agent, orchestrator, ceo]
aliases: [ceo_agent, CEO Agent, מנכ"ל]
associated_with: [agents-root-folder, claude-md, agents-folder]
---

# CEO Agent (מנכ"ל)

## What it does
ה-orchestrator המרכזי של מערכת ה-5 agents. מנתח כל משימה שמגיעה מהמשתמשת, מגלה סוכנים זמינים על ידי סריקת `agents/*.md`, ממפה צעדים לסוכנים, ומפעיל אותם בסדר סדרתי. **אינו מבצע משימות עצמאית** — רק מנהל ומתאם. מדווח למשתמשת רק ב-3 מצבים: סיום / החלטה קריטית / כישלון.

## Associated with
- [[agents-root-folder]] — `agents/ceo_agent.md` הוא הקובץ הגדרת המנכ"ל
- [[claude-md]] — CLAUDE.md מחייב קריאת `agents/ceo_agent.md` בכל סשן
- [[agents-folder]] — `.claude/agents/` נפרד — תשתית Claude Code

## פרוטוקולים מרכזיים
| פרוטוקול | תיאור |
|----------|-------|
| קבלת משימה (6.1) | זיהוי מטרה → פירוק → גילוי סוכנים → מיפוי → ביצוע |
| גילוי סוכנים (6.2) | סריקת `agents/*.md` + קריאת headers → מפת יכולות |
| הפעלת סוכן (6.3) | context + משימה ספציפית + output מצופה |
| דיווח (6.4) | רק סיום / החלטה קריטית / כישלון |
| שגיאות (7) | תיעוד → 2-3 חלופות → דיווח עם המלצה |

## Notes
עיקרון הרחבה: הוספת `agents/agent_XX.md` חדש אינה מחייבת שינוי ב-`ceo_agent.md`.
