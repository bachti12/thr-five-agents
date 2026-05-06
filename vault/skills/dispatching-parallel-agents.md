---
tags: [skill, agents, parallelism]
aliases: [dispatching-parallel-agents]
associated_with: [subagent-driven-development, executing-plans]
---

# Skill: dispatching-parallel-agents

## What it does
מפעיל agents מקבילים כאשר יש 2+ משימות עצמאיות. כל agent מקבל context מדויק ומבודד (לא יורש את הסשן הנוכחי). מתאים כאשר אין תלות בין הכשלונות/המשימות. לאחר הסיום — בדיקת קונפליקטים ואינטגרציה.

## Associated with
- [[subagent-driven-development]] — גישה חלופית לביצוע מקבילי
- [[executing-plans]] — לביצוע תכניות בסשן נפרד
- [[superpowers-plugin]] — חלק מחבילת superpowers

## Notes
אין להשתמש כאשר הכשלונות קשורים זה לזה, או כאשר agents עלולים לערוך אותם הקבצים.
