---
tags:
  - "#Hub"
---


![[HubBackground.png|banner-fade]]

# <center>**Vault Hub**</center>

> [!kirk|info] Guide (Remove me)
Please have a read through the [[README]] 

> [!metadata|party] Parties
>> [!cards|dataview 5] **Party**
>> ```dataview
>> TABLE WITHOUT ID
>> "<span style='display: block; text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>> embed(link(art)) AS "Art"
> FROM !"z_Templates"
>> WHERE contains(tags, "Party")
>> SORT file.name asc
>> ```

> [!metadata|geography]- Geography
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion", join(link(location), ", ") AS "Location"
> FROM "Campaign"
> WHERE contains(tags, "Geography")
> SORT dominion ASC, file.name ASC

> [!metadata|county]- County
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

> [!metadata|district]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type, join(link(location), ", ") AS "Location"
> FROM "Campaign"
> WHERE contains(tags, "District")
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)", join(link(location), ", ") AS "Locations"
> FROM "Campaign"
> WHERE contains(tags, "POI")
> SORT poitype ASC, file.name ASC

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
> WHERE contains(tags, "Character")
> SORT tags DESC, file.name ASC

> [!metadata|servicerequests]- Service Requests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE contains(tags, "Service")
> SORT file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE contains(tags, "Literature")
> SORT file.name ASC

## Random Notes
> [!cards|dataview 7]
> ```dataview
> TABLE WITHOUT ID
> "<span style='display: block; text-align: center; margin-bottom: 2px;'>" + link(file.link, Aliases) + "</span>" AS Aliases,
> embed(link(art)) AS "Art"
> FROM "Campaign"
> FLATTEN [ [(seed) => (seed * 1103515245 + 12345) % 2147483648]] AS random
> FLATTEN [number(dateformat(date("now"), "x"))] AS seed
> SORT random[0](seed + file.size)
> LIMIT 21



