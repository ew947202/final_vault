---
tags:
  - "#Party"
art: z_Assets/Player Characters/Krillum.jpg
---

![[PartyDashboardBackground.png|banner-fade]]

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
>> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Aliases** | `INPUT[list:aliases]` |
>> **Journey Board** | `INPUT[Null][suggester(optionQuery("Campaign/Parties/Journey Boards"), useLinks(partial)):journeyboard]` | 

# <center> **`=this.file.name`** </center>
> [!metadata|characters] Characters
>> [!cards|dataview 5] **Parties**
>>```dataview
>> TABLE WITHOUT ID
>>	embed(link(art)) AS "Art",
>>     "<span style='display: block; text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title
>> FROM "Campaign"
>> WHERE econtains(whichparty, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
>> SORT tags DESC, file.name ASC
>>```

> [!metadata|sessionlogs]- Session Logs `VIEW[{journeyboard}][link]`
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + sessiondate + "</span>" AS SessionDate,
>>	quicknote AS "QuickNotes"
>> FROM "Campaign"
>> WHERE econtains(whichparty, this.file.link) AND contains(tags, "SessionNote")
>> SORT date(sessiondate, "dd/MM/yyyy") DESC LIMIT 9
>>```
>>

>[!metadata|county]- County
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion", join(link(location), ", ") AS "Locations"
> FROM "Campaign"
> WHERE contains(tags, "County")
> SORT dominion ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion", join(link(location), ", ") AS "Locations"
> FROM "Campaign"
> WHERE contains(tags, "Settlement")
> SORT dominion ASC, file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type, hq AS HQ
> FROM "Campaign"
> WHERE contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations", join(link(location), ", ") AS "Locations"
> FROM "Campaign"
> WHERE contains(tags, "NPC")
> SORT tags DESC, file.name ASC

> [!metadata|quests]- Quests
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, quicknote AS Notes, status AS Status
> FROM "Campaign"
> WHERE econtains(tags, "Quest")
> SORT file.name ASC
## NPC Relations

> [!column|3 no-title]
>
>> [!metadata|family] Family
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Family") AND !contains(condition, "Dead")
>> SORT file.name ASC
> 
>> [!metadata|ally] Ally
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Ally") AND !contains(condition, "Dead")
>> SORT file.name ASC
>
>> [!metadata|friend] Friends
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Friend") AND !contains(condition, "Dead")
>> SORT file.name ASC
>
>> [!metadata|like] Like
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Like") AND !contains(condition, "Dead")
>> SORT file.name ASC
> 
>> [!metadata|dislike] Dislike
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Dislike") AND !contains(condition, "Dead")
>> SORT file.name ASC
> 
>> [!metadata|enemy] Enemy
>> ```dataview
>> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases
>> FROM "Campaign"
>> WHERE econtains(party1relation, "Enemy") AND !contains(condition, "Dead")
>> SORT file.name ASC
> 

## Notes

