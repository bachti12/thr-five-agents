# The 5 Agents — Vault Index

מפת ידע הפרויקט. כל קובץ בפרויקט מתועד כאן עם לינקים לקבצים קשורים.

---

## Project Config
קבצי הגדרות ברמת שורש הפרויקט → `vault/project-config/`

| Node | קובץ מקור | תיאור |
|------|-----------|-------|
| [[claude-md]] | `CLAUDE.md` | הוראות ל-Claude Code |
| [[env-config]] | `.env` / `.env.example` | משתני סביבה ומפתחות |
| [[gitignore]] | `.gitignore` | חרגות מה-git |

---

## Infrastructure
תשתית Claude Code תחת `.claude/` → `vault/infrastructure/`

| Node | קובץ מקור | תיאור |
|------|-----------|-------|
| [[agents-folder]] | `.claude/agents/` | הגדרות sub-agents (ריק כרגע) |
| [[skills-folder]] | `.claude/skills/` | כל הסקילים הזמינים |
| [[commands-folder]] | `.claude/commands/` | slash commands (ריק כרגע) |
| [[superpowers-plugin]] | `.claude/skills/*/` | 14 סקילים מ-superpowers v5.1.0 |
| [[obsidian-vault-workflow-skill]] | `.claude/skills/obsidian-vault-workflow/` | ⭐ חובה בכל סשן |

---

## Skills
כל הסקילים הזמינים → `vault/skills/`

| Node | מטרה |
|------|-------|
| [[obsidian-vault-workflow-skill]] | ⭐ ניהול vault — חובה בתחילת כל סשן |
| [[brainstorming]] | עיצוב לפני קוד |
| [[writing-plans]] | כתיבת תכנית מימוש |
| [[subagent-driven-development]] | ביצוע תכנית עם agents + ביקורת |
| [[executing-plans]] | ביצוע תכנית בסשן נפרד |
| [[dispatching-parallel-agents]] | agents מקבילים למשימות עצמאיות |
| [[test-driven-development]] | TDD |
| [[systematic-debugging]] | debugging שיטתי |
| [[verification-before-completion]] | אימות לפני הכרזת סיום |
| [[requesting-code-review]] | ביקורת קוד על ידי sub-agent |
| [[receiving-code-review]] | קבלת משוב ביקורת |
| [[using-git-worktrees]] | עבודה מבודדת |
| [[finishing-a-development-branch]] | סיום ואינטגרציה של ענף |
| [[using-superpowers]] | מדריך שימוש בסקילים |
| [[writing-skills]] | יצירת סקילים חדשים |

---

## Session Log
יומן סשנים → `vault/Meeting Notes/`

| Session | תאריך | סטטוס |
|---------|--------|-------|
| [[bootstrap-project-structure]] | 2026-05-06 | shipped |
| [[file-documentation-vault]] | 2026-05-06 | shipped |
