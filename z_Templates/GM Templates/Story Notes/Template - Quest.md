---
tags:
  - Quest
art: z_Assets/Misc/PlaceholderImage.png
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
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>> **Adventure** | `INPUT[Null][suggester(optionQuery(#Adventure AND !"z_Templates"), useLinks(partial)):adventure]` |
>> **Status** | `INPUT[Status][:status]` |

> [!infobox]
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> #### Quest Info
>  |
> ---|---|
> **Adventure** | `VIEW[{adventure}][link]` |
> **Status** | `VIEW[{status}]` |

# **`=this.file.name`**

## Summary
> [!kirk|info] Prompt (Remove me)
> Provide an overarching overview of this adventure. What is the central theme or conflict driving the narrative? Outline the potential quests or objectives that the players may embark on. Consider the variety of challenges, encounters, or tasks they might face. Additionally, describe how the adventure begins. What inciting incident or call to action propels the players into the unfolding storyline? Use this section to set the stage, introduce key elements, and establish the initial motivations that will guide the players throughout the adventure.

## Notes