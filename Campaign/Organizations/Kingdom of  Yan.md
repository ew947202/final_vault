---
tags:
  - Organization
art: z_Assets/County & Settlements/Duchy of Yan_close.png
organizationtype:
  - Nation
location:
  - "[[Duchy of Yan]]"
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

## Overview

> [!kirk|info] Prompt (Remove me)
> Create an encompassing overview of this organization's essence. Explore its purpose, structure, values, and significance within the world. Highlight the unique traits that define this group, delving into its history, goals, and impact on its members and the surrounding society. What distinguishes this organization, and how does it operate within the larger context of the world?

## Culture

> [!kirk|info] Prompt (Remove me)
> Detail the culture embedded within this organization. What is its mission statement or core philosophy? Explore its code of conduct, values, and ethical guidelines that guide its members. How does this organization recruit new members, and what criteria do they look for? Define the hierarchy or ranks within the group and the significance of each level. Additionally, describe any uniforms, symbols, or insignia that members might wear to signify their affiliation. How do these cultural elements shape the identity and operations of this organization?

## Current Events

> [!kirk|info] Info (Remove me)
> Zoom into the present landscape of this organization. What is currently happening within its ranks? Detail ongoing developments, internal conflicts, or achievements. Is the organization facing challenges, undergoing reforms, or enjoying newfound success? Furthermore, what are its current objectives or endeavors? Explore the immediate goals or missions the organization is striving to accomplish. How are these current events and goals influencing the actions and dynamics within the group?

## History

> [!kirk|info] Info (Remove me)
> Trace the roots and evolution of this organization through time. Explore its founding, pivotal moments, and transformative events that shaped its trajectory. What were the circumstances that led to its creation? Detail significant milestones, challenges, or triumphs that have defined its history. How has the organization adapted to changes, crises, or conflicts over the years? Uncover the legacy and historical narrative that have molded this group into what it is today.

## Notes



