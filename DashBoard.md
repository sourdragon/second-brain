---
sticker: lucide//home
---
### Habits
```dataview
TABLE WITHOUT ID
  file.link as Date,
  choice(woke-up > 0, "✅", "❌") as "Woke Up",
  choice(put-a-schedule > 0, "✅", "❌") as "Schedule",
  choice(talked-to-dad > 0, "✅", "❌") as Highlights,
  choice(hydration > 0, "✅", "❌") as Hydration,
  choice(posture > 0, "✅", "❌") as Posture
FROM "journal"
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7days)
SORT file.day ASC 
```





