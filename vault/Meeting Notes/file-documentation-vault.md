# File Documentation Vault

## Overview
יצירת vault מסמכים בסגנון Obsidian המתעד כל קובץ בפרויקט: מה הוא עושה, למי הוא משויך, ולינקים לקבצים קשורים. הוגדר גם סקיל `obsidian-vault-workflow` שמחייב קריאה/כתיבה לvault בתחילת וסוף כל משימה.

## Open Questions
- none

## Session Log

### 2026-05-06 — Build initial vault [shipped]
- **What was done:** יצירת כל תיקיות ה-vault (`project-config/`, `infrastructure/`, `skills/`, `Meeting Notes/`), קובץ `00-INDEX.md`, ו-MD לכל קובץ/סקיל בפרויקט. עדכון CLAUDE.md להפניה לסקיל.
- **Decisions:** ארגון לפי קטגוריות (config / infrastructure / skills) ולא לפי שם קובץ. שימוש ב-`[[wikilinks]]` לחיבורים בין צמתים.
- **Notes / Caveats:** הסקיל `obsidian-vault-workflow` כבר קיים ב-`.claude/skills/` עם תוכן מפורט — לא נדרס.
- **Related:** [[obsidian-vault-workflow-skill]], [[bootstrap-project-structure]]
