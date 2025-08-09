---
tags:
  - "#Character"
  - "#Player"
art: IMMAGINI/PERSONE & ORGANIZZAZIONI/NICO_BEIL.png
whichparty:
  - "[[I figli di Stacia]]"
condition: Healthy
ownedlocation:
  - "[[Base a Lierna]]"
location:
  - "[[Base a Lierna]]"
occupation:
  - Adventurer
  - Mercenary
playedby: Leo
pronounced: Nico Beil
ancestry: Dwarf
gender: Male
pronouns: He/Him
age: Adult
aliases:
  - Monaco
---

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
>>---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>>---|---|
>> **Played By** |  `INPUT[textArea:playedby]`
>> **Character Sheet** |  `INPUT[textArea:charactersheet]`
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Razza** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Sottorazza** | `INPUT[Heritage][suggester:heritage]` |
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]`
>> **Age** | `INPUT[Age][:age]` |
>
>> [!metadata|metadataoption]- Info
>> #### Player Info
>>  |
>>---|---|
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Which Party** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Condition** | `INPUT[Condition][:condition]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Giocato da: `VIEW[{playedby}][text]`
> ###### Bio
>  |
> ---|---|
> **Alias** | `VIEW[{aliases}][text]` |
> **Razza** | `VIEW[{ancestry}]` |
> **Sottorazza** | `VIEW[{heritage}]` |
> **Genere** | `VIEW[{gender}]` |
> **Pronomi** | `VIEW[{pronouns}]` 
> **Età** | `VIEW[{age}]` |
> ###### Info
>  |
> ---|---|
> **Occupazione** | `VIEW[{occupation}][text]` |
> **Organizzazione** | `VIEW[{organization}][link]` |
> **Religione** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>


> [!metadata|servicerequests]- Servizi
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(customer, this.file.link) AND contains(tags, "Service") AND !contains(status, "✅") AND !contains(status, "❌")
> SORT file.name ASC

> [!metadata|letters]- Lettere
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Letteratura
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

## Ideali
### Ama

- La famiglia
- La moglie (ora defunta)
- Il vino di sua produzione
- Il cristallo di sale che porta sempre con sé
- Il cibo in quanto esperienza
- La felicità vera

### Odia

- Chi non rispetta la forza e il combattimento
- Le ingiustizie (ad es. la perdita della moglie lo ha segnato profondamente)
- In generale, non ha indicato odi particolari, ma si incazza facilmente per cose specifiche

## Obbiettivi
### Breve termine

- Continuare a proteggere il suo villaggio
- Cercare serenità nella vita quotidiana

### Lungo termine

- Trovare la vera felicità
- Vivere una bella vita

## Storia
### Nascità

- Nato a [[ROCCASPARVERA]], in una famiglia di viticoltori (famiglia Beil)
- <font color="#92cddc">Genitori</font>: Lenor e Franco (ex soldato)
- <font color="#92cddc">Fratelli</font>: Pino e Fender

### Gioventù

- Cresciuto addestrandosi al combattimento col padre
- Entrato nel piccolo esercito del villaggio
- Ha sviluppato amicizie lì

### Viaggio


### Religione


## Note

