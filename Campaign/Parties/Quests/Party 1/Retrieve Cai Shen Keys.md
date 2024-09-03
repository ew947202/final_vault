---
tags:
  - Quest
art: z_Assets/Misc/PlaceholderImage.png
quicknote: Yuan Tan wants more information regarding Cai Shen's lost keys
status: ⏳
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
Our mission is to collect all the keys of [[Cai Shen]] in the hopes of being able to bring him back. It is said the person who brings back [[Cai Shen]]  will have one wish granted to them.

## Notes
- [x] We were given a princess to retrieve by [[Yuan Tan]] as she may have some ideas of where the map to the first key may be
- [x] The party successfully captured the princess, but she had no idea about anything regarding the keys or [[Cai Shen]]
	- [x] Turns out she had a map magically etched onto her back that showed the rough location of the first key
- [x] We followed the map to an underground temple of [[Cai Shen]]  and found the first key and retrieved it after fighting the Skaven
	- [x] After returning from the temple the party gave the key to [[Yuan Tan]] and was told the second key is likely somewhere in the [[Liang Confederation]].
	- [ ] The group made it to [[Liang Confederation]] and have found out that there are multiple Ma families and this one may not have information regarding the second key. [[Krillium Krew]] does remember that [[Ma Yunlei]] may have some information regarding the key... do we head back to [[Chang'an]]???