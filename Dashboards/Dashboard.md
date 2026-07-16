# Recent Recaps

> [!grid]
> [![[169.gif|hsmall cover]]](<Episode 169 - That's Some Mighty NICE Cowpokin' Around, Y'all>)
> [![[170.jpg|hsmall cover]]](<Episode 170 - Can't Stop, Won't Stop the Shenans>)
> [![[171.gif|hsmall cover]]](<Episode 171 - You Had One Job>)
> 
> [![[172.gif|hsmall cover]]](<Episode 172 - Thorny Negotiations>)
> [![[173.jpg|hsmall cover]]](<Episode 173 - Regifted>)
> [![[174.jpg|hsmall cover]]](<Episode 174 - The Favor>)
> 
> [![[175.png|hsmall cover]]](<Episode 175 - Operation Felix Around and Find Out>)
> [![[176.jpg|hsmall cover]]](<Episode 176 - Falling is a Free Action>)
> [![[177.jpg|hsmall cover]]](<Episode 177 - Hurty Words Disguised As Huggy Words>)
> [![[178.jpg|hsmall cover]]](<Episode 178 - Showdown Adjacent to the Luxury Hand Bag Store>)

----

# Open Quests
#### Unstarted:
```dataview
LIST FROM #unstarted and "Quests"
SORT recap_number
```

#### In Progress
```dataview
LIST FROM #in_progress and "Quests"
SORT recap_number
```

#### On Hold
```dataview
LIST FROM #on-hold and "Quests"
SORT recap_number
```

----

# NPC's We've Recently Interacted With (WIP)
```dataview
LIST FROM "Characters"
WHERE note_type = "NPC"
LIMIT 10
```

----

# Current
Location: [[Thunder Junction]]


```dataview
TABLE file.mtime as "Last Modified"
WHERE file.name != this.file.name
SORT file.mtime DESC
LIMIT 50
```

