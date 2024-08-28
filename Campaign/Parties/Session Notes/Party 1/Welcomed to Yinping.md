---
tags:
  - "#SessionNote"
whichparty: "[[Krillium Krew]]"
sessiondate: 20/08/2024
quicknote: Party arrives at Yinping
characters:
  - "[[Yuan Shang]]"
  - "[[Ma Mei]]"
  - "[[Ma Lianli]]"
  - "[[Ma Chao]]"
  - "[[Drezzard]]"
locations:
  - "[[Campaign/Settlements/Yinping.md|Yinping]]"
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

We sorted/identified all the loot [[Ketti Barques]] and [[Kuma Kabutomushi]]  were able to get from the slave caravan. We learned that [[Dong Zhuo]] killed [[Yuan Fang]] according to [[Wu Shen Jiao]] . We finished traveling to [[Yinping]] and as we docked found four Nataloid ships. The party meets with [[Yuan Shang]] and he immediately let's us in on all his problems he's been having while in [[Yinping]]. The most crucial one is that [[Ma Teng]] will not be back home until next week. We learn that [[Yuan Shang]] is supposed to be married off to [[Ma Lianli]] which is one of the twins daughters of [[Ma Teng]]. Unfortunately, [[Yuan Shang]] has been sleeping with both the daughters and got one of them pregnant.

We are invited to a dinner at [[Ma Teng]]'s palace. There were representatives from the [[Grand Duchy of Song]] and a religious cult of Xagaros called the [[Red Hands]] . The leader of this cult [[Drezzard]] spoke to Kuma during the dinner and asked him how much for [[Althaea Moffet]] and [[Wu Shen Jiao]] , presumably to eat them.

We ended the dinner by making formal introductions to the [[Ma Teng]] family and hoping to get closer to them and find out which of the twins are pregnant.

### Downtime Summary 

> [!kirk|info]+ [[Kuma Kabutomushi]]  & [[Jurian Flintfoot]]  Downtime 
Kuma and Jurian discuss how much he has been dying and why Jurian feels the need to insert himself where a wizard has no place going.


> [!kirk|info]+ [[Ketti Barques]]  & [[Jurian Flintfoot]]  Downtime 
Ketti & Jurian finally go on there date for the spell scroll Ketti got him. During the lunch date they discuss [[Yuan Tan]]  and how Ketti doesn't trust him and thinks he doesn't value our party.  
Jurian attempts to learn more about Ketti's past, but it seems that he doesn't remember much of anything.


> [!kirk|info]+ [[Wu Shen Jiao]]  & [[Jurian Flintfoot]]  Downtime 
> >Jurian recieved three scrolls from [[Yuan Tan]]: *Comprehend Language*, *Dispel Magic*, *Counter Spell*.
> 
> [[Jurian Flintfoot]] asks [[Wu Shen Jiao]] about [[Yuan Tan]] and how she would describe him: *[[Yuan Tan]]  is an ambitious person. No being rises to power or remains thus without driving ambition, particularly in these tumultuous times. [[Yuan Tan]] can be ruthless. He send his armies against his rivals, resulting in many deaths. To not act in such a manner in this time of civil war is to wait for death to come for you are your people.*
> [[Jurian Flintfoot]] learns that [[Wu Shen Jiao]] is all-consumed by her research of the hobgoblin race and they vow to help each other reach their personal goals.


### Recap of Last Session 

> [!kirk|info] Prompt (Remove me)
Use this section to consolidate and expand upon any spontaneous creations made during the session. After reviewing your During Session notes, use this area to flesh out and detail any new elements, characters, locations, or concepts that emerged. Provide additional information, backgrounds, and intricacies to bring these creations to life. This section serves as a post-session development space, ensuring that any improvisations made during the session can be refined and integrated seamlessly into your campaign world.

### Log

[[Ketti Barques]]brings back a large amount of loot from the slave camp
	- Things needing to be *Identified* 
		- Single long spear/pike (+2 pike)
		- Set of splint armor (+1 Mithril Splint Armor) "Armor of the Cavalry Champion"
		- ornate bow ()"Ancestral Bow of Hegen" Long bow that once per long rest you can cast *Haste* on yourself
		- spell scroll (Summon Fey) 
			- Has been copied into [[Jurian Flintfoot]]  Spellbook
- [[Dong Zhuo]] killed [[Yuan Fang]]  ([[Yuan Shao]] father) 
	- Supposedly according to Shen Jiao
- [[Ketti Barques]]  hands out 8 healing potions to each person


*We arrive in [[Yinping]] (Capital of [[Liang Confederation]] 
- Four Nautiloid are posted as we enter [[Yinping]]
- We land and get the remainder of our payment from [[Yin Beihu]]
	- 3,000 shards - 500 shards a piece
- Shi Shi a minister in the city of [[Yinping]] and is leading us while we are in the palace 

Problems given from [[Yuan Shang]]
1. [[Ma Teng]] (19 or 20 - half elf drow 6'9)is not in [[Yinping]](lots of pork, beef, and fish in the palace) and should be coming back in a week he's currently campaigning 
	1. [[Ma Chao]] is [[Ma Teng]] son and is a stubborn prick according to [[Yuan Shang]] "all he cares about is fighting"
2. [[Yuan Shao]] wants [[Yuan Shang]](hobgoblin) to marry one of [[Ma Teng]] daughters... he has two and they are twins 
	1. [[Yuan Shang]] got one of the daughter's pregnant and doesn't know which one cause he has slept with both
		1. [[Ma Lianli]](full drow) - greater amount of food in front of her
		2. [[Ma Mei]] (full drow) - slightly more pale (slightly more indicator that shes pregs)

- At dinner there is 7 illathids and a beholder
	- It is the right hand man of [[Drezzard]] (Illathid)
		- worked for the god King - was the High Admiral for the enter natiloid army
		- After Xia empire fell, he separated himself from the Xia and created a mercenary fleet called the Red Hand - a religious cult of Xagaros  
- [[Han Sui]](hobgoblin) General for [[Kingdom of Zhong]]  
- [[Li Ru]] (hobgoblin) Zhong
	- Has illusion magic all over him
- [[Han Sui]](elf drow and wood elf, male) 
	- [[Ma Chao]] uncle
	- brother of [[Ma Teng]]
	- Mostly talking to misters and other people at his table
	- Amulet of magic, school of magic unknown.
- 
[[Jurian Flintfoot]] makes an Arcana check
- notices that the servers are using small amounts of magic in the food
- he casts detect magic focusing on the food traces of evocation magic
	- all the illathids and beholder have strong VERY strong magical aura about them

[[Kuma Kabutomushi]]  makes a Wisdom saving throw
- hears a voice in his head from [[Drezzard]] "how much would you like for your human"