---
tags:
  - Organization
art: z_Assets/Misc/PlaceholderImage.png
organizationtype:
  - Cult
  - Mercenary
head:
  - "[[Drezzard]]"
location:
  - "[[Yinping]]"
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[OrganizationType][inlineListSuggester:organizationtype]` |
> **Hierarchy** | `INPUT[Null][suggester(optionQuery("Campaign/Organizations/Hierarchies"), useLinks(partial)):hierarchy]` | 
> **Head** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):head]` |
> **Steward** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):steward]` |
> **Parent Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Worship** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):worship]` |
> **HQ** | `INPUT[Null][suggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):hq]` |
> **Operating Areas** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> ###### `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
> | |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{organizationtype}][text]` |
> **Hierarchy** | `VIEW[{hierarchy}][link]` |
> **Head** | `VIEW[{head}][link]` |
> **Steward** | `VIEW[{steward}][link]` |
> **Parent Organization** | `VIEW[{organization}][link]` |
> **Worship** | `VIEW[{worship}][link]` |
> **HQ** | `VIEW[{hq}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!kirk|info] Info (Remove me)
> Organization: Organizations can be anywhere from a small band of misfits to an entire Nation.

> [!metadata|geography]- Geography
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Geography") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|county]- County
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "County") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Settlement") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|district]- Districts
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "District") AND econtains(organization, this.file.link)
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE contains(tags, "POI") AND econtains(organization, this.file.link)
> SORT poitype ASC, file.name ASC

> [!metadata|organizations]- Child Organizations
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "Organization") AND econtains(organization, this.file.link)
> SORT organizationtype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE without id file.link AS "Name", join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(organization, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

> [!metadata|rumour]- Rumours
> ```dataview
> TABLE without id file.link AS "Name", accuracy AS Accuracy, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(subject, this.file.link) AND contains(tags, "Rumour")
> SORT file.name ASC

## Overview

A mercanry group that is the militant arm of the Cult of Purification, started by [[Drezzard]]. They believe that all life is conflict and that through conflict the weak are culled, thus purifying the world of those that do not deserve life.


## Culture

While working with the Red Hands can be effective it's equally as dangerous. [[Drezzard]] rarely distinguishes between friend and foe on the battlefield, and there is always the fear that he'll turn on his employers.

### Example
## Acquaintances

> [!kirk|info] Prompt (Remove me)
> Map out the network of relationships this organization maintains with other groups and individuals. Who are their allies, rivals, or adversaries? Detail the nature of these connections, whether they're alliances based on shared interests, longstanding rivalries, or uneasy truces. What events or conflicts have shaped these relationships? Furthermore, explore the interactions and dealings this organization has with influential individuals or entities outside its circle. How do these connections influence the organization's operations and goals?

## Current Events

> [!kirk|info] Info (Remove me)
> Zoom into the present landscape of this organization. What is currently happening within its ranks? Detail ongoing developments, internal conflicts, or achievements. Is the organization facing challenges, undergoing reforms, or enjoying newfound success? Furthermore, what are its current objectives or endeavors? Explore the immediate goals or missions the organization is striving to accomplish. How are these current events and goals influencing the actions and dynamics within the group?

## History

During the Xia reign, [[Drezzard]] and his fleet would mercilessly exterminate entire regions and cull pipulaces for the sake of removing weakness from the empire. [[Drezzard|Drezzar]] and a large portion of his fleet were also involved in the *Battle of Nadis* during the eastern invasion and were driven back when they received word of Xagaros's death.


## Notes



