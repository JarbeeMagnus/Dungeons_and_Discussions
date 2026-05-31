There are 6 types of notes I want to reference:
- Characters (PC & NPC)
- Locations
- Organizations
- Quests
- Events
- Recaps

---
Recaps will be the most manual since I'll be linking everything within.

Current use case is pulling "Appears in" from the Recaps folder
This is done by the following dataview code:

>LIST FROM "Session Recaps"
>WHERE contains(metadata_field,"title of this page")

Because the "current page" will already be linked in the body of the recap, so there will be a line between the two notes in the graph (which I like)

HOWEVER - this means I need to have the metadata fields listed in the front matter of the recap note. This would mean, after typing and linking the recap, that I would need to comb through and list out the following into the front matter of the recap note:
1. NPC's mentioned
2. Organizations mentioned
3. Locations mentioned
4. Quests & Events mentioned

Now this may not be a big deal. However, I don't think the any dataview stuff refreshes if a note changes name. So both the *"Goth Mommy" value in the "NPC" metadata field in the recap note* AND the *dataview table of the "Goth Mommy" page* would need to be updated once I know her name.

I feel like I'm doing too much. Too many metadata fields that aren't really necessary once I realized the Obsidian graph doesn't update with this info.
The only *real* use case for the fields are for dashboards - but I'm not even sure how I would want to do those and (again) am probably doing too much. Do I really need to see the members in an org on the dashboard?
**I think I want to delete the metadata fields except for note_type and aliases for all notes (& the session # for recaps for sorting) and then see what happens...**

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