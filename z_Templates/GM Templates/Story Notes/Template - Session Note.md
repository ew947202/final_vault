---
tags:
  - "#SessionNote"
---
> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Which Party** | `INPUT[Null][suggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Session Date** | `INPUT[datePicker:sessiondate]`
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>
>> [!metadata|metadataoption]- Quick References
>> #### Quick References
>>  |
>> ---|---|
>> **Character** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):characters]` |
>> **Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates")):locations]` |
>> **Miscellaneous** | `INPUT[inlineListSuggester(optionQuery("" AND !"z_Templates")):misc]` |

#  `=link(this.whichparty)` `=this.file.name` "`=this.aliases`"

### Quick References

> [!kirk|info] Info (Remove me)
This is a list of links to various notes within your Vault. Use this to give yourself quick ways to find any relevant information you need on hand for your session.

> [!column|3 no-title]
>> [!metadata|characters] People
>> `VIEW[{characters}][link]`
>
>> [!metadata|location] Locations
>> `VIEW[{locations}][link]`
>
>> [!metadata|misc] Misc
>> `VIEW[{misc}][link]`

### Session Summary

> [!kirk|info] Prompt (Remove me)
Use this area to track the party's travel and rest activities during the session. Note down the duration of their travels, including any notable encounters or events that occur during the journey. Additionally, record periods of rest, whether short breaks or longer rests, and indicate how time passes in-game. This section helps you maintain a coherent timeline, manage resources, and ensure a consistent flow of time within the session.

### Downtime Summary 

> [!kirk|info] Prompt (Remove me)
Use this space to record all loot, rewards, and purchases obtained by the party during the session. Document any valuable items, treasures, or magical artifacts they acquire. Note down rewards for completing quests or overcoming challenges. Additionally, keep track of any purchases the party makes, detailing items, costs, and relevant information. This section serves as a consolidated record of the party's wealth and acquisitions, aiding in resource management and future gameplay decisions.

### Recap of Last Session 

> [!kirk|info] Prompt (Remove me)
Use this section to consolidate and expand upon any spontaneous creations made during the session. After reviewing your During Session notes, use this area to flesh out and detail any new elements, characters, locations, or concepts that emerged. Provide additional information, backgrounds, and intricacies to bring these creations to life. This section serves as a post-session development space, ensuring that any improvisations made during the session can be refined and integrated seamlessly into your campaign world.

### Log

> [!kirk|info] Prompt (Remove me)
> Note down the in-game time and date that your session ended on.