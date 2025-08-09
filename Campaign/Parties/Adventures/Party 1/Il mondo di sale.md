---
tags:
  - "#Adventure"
art: IMMAGINI/PERSONE & ORGANIZZAZIONI/MONDO DI SALE.png
aliases:
  - Prima avventura
whichparty: "[[I figli di Stacia]]"
status: ❌
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
>> **Which Party** | `INPUT[Null][suggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Status** | `INPUT[Status][:status]` |

> [!infobox]
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> #### Adventure Info
>  |
> ---|---|
> **Party** | `VIEW[{whichparty}][link]` |
> **Status** | `VIEW[{status}]` |

# **`=this.file.name`**

> [!metadata|quests]- Quests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes, status AS Status
> FROM "Campaign"
> WHERE econtains(tags, "Quest") AND econtains(adventure, this.file.link)
> SORT file.name ASC

## Overview

- Gli avventurieri vengono chiamati insieme a molti altri gruppi per capire l'origne della peste a [[DALICO]]
- 

## Notes