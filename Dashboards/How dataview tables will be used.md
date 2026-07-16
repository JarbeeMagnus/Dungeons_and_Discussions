There are 6 types of notes I want to reference:
- Characters (PC & NPC)
- Locations
- Organizations
- Quests
- Events
- Recaps

----

#### Recaps
Current use case is pulling "Appears in" from the Recaps folder into other note types. This is done by the following dataview code:

>LIST FROM "Session Recaps"
>WHERE contains(metadata_field,"title of this page")

Because the "current page" will already be linked in the body of the recap, so there will be a line between the two notes in the graph (which I like)

#### OUTGOING LINKS DATAVIEW BLOCK

>LIST FROM "Session Recaps"
>WHERE contains(file.outlinks,link(this.file.name))
>SORT recap_number

---
Another dataview formula I've figured out is pulling the list of members in an organization into a table on the organization page - BUT THIS DOES NOT LINK THEM so what's the point?
>TABLE note_type AS "PC or NPC", link(Current_Location) AS "Current Location"
>FROM "Characters"
>WHERE icontains(list(organization),"Ru Crew")

#help