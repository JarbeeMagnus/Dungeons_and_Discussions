
### Recap Tasks:
```dataview
TABLE file.tasks.text as "Tasks"
FROM "Session Recaps"
WHERE file.tasks.text
SORT file.tasks.text DESC
```


### Character Tasks:
```dataview
TABLE file.tasks.text as "Tasks"
FROM "Characters"
WHERE note_type = "NPC" AND file.tasks.text
SORT file.tasks.text DESC
```


### All Other Tasks:
```dataview
TABLE file.tasks.text as "Tasks", note_type
FROM "Locations" or "Organizations" or "Session Events" or "Quests"
WHERE file.tasks.text
SORT file.tasks.text DESC
```
