---
tags:
  - "#Character"
  - "#Player"
art: IMMAGINI/PERSONE & ORGANIZZAZIONI/CALLIOPE.jpg
playedby: Chiara
pronounced: Calliope
condition: Healthy
whichparty:
  - "[[I figli di Stacia]]"
location:
  - "[[Base a Lierna]]"
ownedlocation:
  - "[[Base a Lierna]]"
occupation:
  - Noble
  - Mage
ancestry: Human
aliases:
  - Stregone
heritage: 
age: Young Adult
pronouns: She/Her
gender: Female
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
> ###### Played By: `VIEW[{playedby}][text]`
> ###### Bio
>  |
> ---|---|
> **Classe** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> ###### Info
>  |
> ---|---|
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!kirk|info] Handout (Remove me)
[Player Handout](https://docs.google.com/document/d/1_eFTuK3teRJSAVbd2QSZxjDTgE_RZH54zZg-3Eoo4Hk/edit?usp=sharing)

> [!metadata|charactersheet]- Character Sheet
> ```custom-frames
frame: Demiplane
style: height: 700px;
>```

> [!metadata|servicerequests]- Service Requests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(customer, this.file.link) AND contains(tags, "Service") AND !contains(status, "✅") AND !contains(status, "❌")
> SORT file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

## Ideals

- **"La vera nobiltà non risiede nel sangue, ma nel cuore e nelle azioni."**
- Vuole un mondo più equo, dove conoscenza e opportunità siano accessibili a tutti.
- Crede in una forza che bilancia il bene e il male, ma non è religiosa.

### Loves

- Studio, lettura, biblioteche
- Aiutare gli altri
- Erbe magiche e pozioni
- La bibliotecaria Tiphi (figura affettiva e mentore)
- Gatti
- La musica (suonava la lira da piccola)

### Hates

- Le formalità nobili
- Il buio
- I fratellastri Nulhin e Rodak (senza un motivo specifico)
- Il mago oscuro che ha liberato inconsapevolmente
- Il padre (rappresenta un conflitto interiore, desidera approvazione ma lo disprezza)

## Goals

### Short-term

- Rafforzarsi per affrontare il mago oscuro liberato da bambina 
- Dimostrare al padre di essere degna della sua attenzione
- Fuggire dalle aspettative nobiliari che la soffocano

### Long-term

- Aprire una scuola pubblica per condividere conoscenza
- Entrare in politica per abbattere le barriere sociali
- Rimediare al proprio errore giovanile (liberazione del mago oscuro)

## History
### Birth Location

Nata a [[PRIMALUNA]] in una casa nobiliare, poi spostata a [[DALICO]]

### Childhood

- Rimasta orfana di madre a 4 anni
- Cresciuta da un padre freddo che l’ha usata come trofeo
- Ha sviluppato una doppia personalità: quella autentica e quella "da figlia modello"

### Journey

- Da autodidatta ha imparato la magia nei libri
- Ha vissuto un'esperienza cruciale in una biblioteca pubblica, dove ha scoperto il valore del sapere libero
- Ha aiutato per errore un mago oscuro a fuggire, evento che la perseguita ancora oggi
- Esplora i boschi per cercare erbe magiche

### Worship

Non segue una religione precisa, ma crede in una forza superiore che regola il bene e il male

## Notes

- Quando si appassiona a un argomento, gesticola e dimentica ogni formalità
- Lavora bene in gruppo, è empatica e ascolta, ma inizialmente è riservata