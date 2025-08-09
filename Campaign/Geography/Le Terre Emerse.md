---
tags:
  - "#Location"
  - "#Geography"
art: MAPPE/le_terre_emerseBASE.png
terrain:
  - Hills
  - Plains
  - Urban
  - River
  - Mountains
  - Desert
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
> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Character OR #Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Terrain** | `VIEW[{terrain}][text]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!kirk|info] Info (Remove me)
> <center><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/8MI5JyiH-Wo?si=G-lpyB0tK_I479FF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></center>


> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[le_terre_emerseBASE.png]]
> lock: true
> recenter: true
> noScrollZoom: false
> ### Use this [LINK](https://docs.google.com/spreadsheets/d/1jKQxktYSUFcCJhEkAAPr1wMVBTqUdpEfA5XveUXI17I/edit?usp=sharing) to work out your map's bounds.
> bounds: [[0,0], [14.57, 14.57]] 
> height: 600px
> width: 640px
> lat: 7.29
> long: 7.29
> minZoom: 1
> maxZoom: 6.5
> defaultZoom: 1
> zoomDelta: 0.5
> unit: miles
> scale: 1
> darkMode: false
> ```

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Settlement")
> SORT nation ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)", join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(location, this.file.link) AND contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

## Cultura

In questo mondo c'è un grande rapporto con il divino. Non ci sono atei, ma solo supportatori o detrattori della divinità.. 

## Territorio

<font color="#00b050">FORESTE</font>: Ricoprono la maggior parte del territorio. Gli alberi hanno nella loro corteccia dei cristalli di sale di varie dimensioni e qualità, questo a causa dell'acqua che assumono. Nonostante ciò i frutti sono privi di acqua salata. Abitate dagli Arboridi 
<font color="#c3d69b">PIANURE</font>: Ricoprono una piccola parte del territorio. Ottime per trovare animali e costruire città. Abitate dai Lapinidi
<font color="#938953">DESERTI DI SALE</font>: Sono pericolose distese di polvere di sale. Il caldo è insopportabile e riesce ad essere abitato solo dagli Elfi del deserto

## Sistema economico

Nelle Terre Emerse si utilizza l'acqua dolce sia per dissetarsi che per effettuare scambi. Ogni mese l'imperatore riceve acqua dolce dal cielo, che viene trasportata a banche che poi si occupano di far funzionare l'economia.



Ci sono tre diverse unità di misura, che corrispondono rispettivamente a monete d'oro, d'argento e di rame:
	-<font color="#ffc000">Mel:</font> l'unità di misura base, equivale ad un bicchiere abbondante d'acqua (200ml)
	-<font color="#bfbfbf">DeciMel:</font> 1/10 di un Mel, equivale a due cucchiai da cucina d'acqua (20ml)
	-<font color="#974806">CentiMel:</font> 1/10 di un DeciMel e 1/100 di Mel, equivale a 20 gocce d'acqua (2ml)

[[Stacia]] creò gli umani con un sistema abbastanza efficiente da necessitare solo <font color="#ffc000">2 Mel</font> di acqua al giorno per vivere.

## Calendario

L'anno delle Terre Emerse è composto da 12 cicli lunari, della durata di 30 giorni l'uno, raggruppati in 4 stagioni

<font color="#00b050">Stagione di Stacia, ossia il risveglio della natura (equivalente della Primavera)</font>
	 -**<font color="#7030a0">Gemmalio:</font>** per l'inizio della gemmazione
	 -**<font color="#7030a0">Aureno:</font>** per la luce del sole come l'oro
	 -**<font color="#7030a0">Florio:</font>** le gemme sbocciano e inizia la fioritura

<font color="#e36c09">Stagione di Solerino, ossia la massima potenza del sole (equivalente dell'Estate)</font>
	 -**<font color="#7030a0">Lucenso:</font>** la luce del sole diventa più intensa
	 -**<font color="#7030a0">Maturio:</font>** i frutti e il frumento vengono raccolti
	 -**<font color="#7030a0">Calente:</font>** il mese in assoluto più calendario

<font color="#c4bd97">Stagione della costruzione, ossia quando si iniziano i preparativi per il freddo</font>
	 -**<font color="#7030a0">Terrafondio:</font>** la natura raduna vicino alle radici tutte le sue risorse
	-**<font color="#7030a0">Artiglio:</font>** mese della raccolta finale, la natura serra i suoi "artigli" e l'uomo si dedica alle costruzioni
	 -**<font color="#7030a0">Fogliaio:</font>** mese dove gli alberi perdono la loro chioma

<font color="#4bacc6">Stagione del freddo (equivalente dell'Inverno)</font>
	 -**<font color="#7030a0">Salino:</font>** le acque si ritirano, mese della raccolta del sale
	 -**<font color="#7030a0">Cristallio:</font>** si formano i cristalli di ghiaccio
	-**<font color="#7030a0">Profondio:</font>** il mese più "tranquillo", quando tutti gli animali sono in letargo e quindi i boschi silenziosi








## Razze

Oltre alle razze giocabili dai giocatori ci sono alcune stirpi che si sono particolarmente isolate dal resto della comunità e che gli avventurieri potranno incontrare

### LAPINIDI
![[LAPINIDE.png]]
- I Lapinoidi sono umanoidi con tratti da coniglio, caratterizzati da lunghe orecchie mobili e morbido pelo che varia dal bianco al marrone chiaro.
- Hanno grandi occhi espressivi e denti anteriori leggermente sporgenti, che donano loro un’aria vivace e curiosa.
- La loro corporatura è snella e agile, con zampe forti progettate per salti potenti e movimenti rapidi.
- Originano da ambienti boschivi e prati aperti, dove vivono in comunità pacifiche legate ai cicli naturali e alle stagioni.
- Le comunità lapinoidi sono organizzate in clan che venerano la Luna e le stagioni, simboli della loro rapidità e sensibilità ai ritmi naturali.
- I riti di passaggio includono prove di agilità e coraggio, come gare di salto e corse attraverso i boschi.
- Indossano abiti leggeri e pratici, spesso decorati con fiori, campanelli e piccoli amuleti naturali, simboli di protezione e fortuna.
- Valorizzano la cooperazione e la prudenza, preferendo la fuga o l’inganno al conflitto diretto, ma non esitano a difendersi con astuzia e velocità.
### ARBORIDI
![[ARBORIDE.png]]
- Gli Arbolidi sono umanoidi dalle fattezze arboree, con pelle simile a corteccia sottile e flessibile, e sottili venature simili a linfa che scorrono sotto la superficie.
- Hanno mani e piedi con dita leggermente affusolate, come radici, ma dall’aspetto perfettamente umanoide. Capelli di muschio, fogliame o licheni ne incorniciano il volto.
- Comunità guidate da “Custodi della Quercia Madre”, druidi-sovrani che preservano l’equilibrio tra crescita e decadimento.
- Templi viventi: radure cerchiate da alberi secolari o antiche rovine inglobate nella vegetazione.
- Valorizzano la pazienza e la resilienza: ogni decisione è ponderata come la crescita lenta di un albero.
- Riti di passaggio: piantare una giovane quercia che cresce insieme al giovane Arbolide, segnando l’età adulta.
### ELFI DEL DESERTO

![[ELFO_DESERTO.png]]
- Vivono nelle vaste distese di deserti di sabbia e sale.
- Sono nomadi: si spostano in carovane familiari alla ricerca di oasi e fonti di sale.
- Indossano abiti larghi e velati per proteggersi dal sole e dalle tempeste di polvere.
- I loro insediamenti sono tende e accampamenti smontabili, decorati con motivi geometrici e talismani protettivi.
- Venerano antichi spiriti del vento e della sabbia.
- Tramandano la loro storia oralmente attorno ai fuochi notturni.
- Sono abili esploratori, esperti nell’orientarsi con le stelle.
- Maestri nel raccogliere e conservare ogni stilla d’acqua.



### I DIMENTICATI !!NON RIVELARE!!

![[DIMENTICATO.png]]
- Un popolo antico, ormai perso nella memoria delle altre civiltà, che vive ai margini del mondo conosciuto: rovine, catacombe, zone d’ombra tra i piani.
- Non hanno un aspetto fisso: la loro carne porta i segni del tempo e dell’oblio — pelle pallida o traslucida, occhi opachi come nebbia, voci sussurrate come eco lontane.
- Non ricordano appieno la loro origine; ogni Dimenticato cerca frammenti di memoria, raccogliendo reliquie e segreti.
- Si nutrono di ricordi: attraverso rituali o contatti, possono leggere o consumare memorie altrui, ma a costo di dimenticare qualcosa di loro stessi.
- Si spostano in silenzio, temuti come presagi o spiriti vaganti. Alcuni diventano oracoli o veggenti, altri guardiani di conoscenze proibite.
- Venerano divinità dell’oblio, del sonno o delle soglie tra mondi.
- I Dimenticati vedono il tempo come un ciclo frantumato: per loro, presente, passato e futuro si mescolano nei sogni.

## History

Un tempo esisteva solo il mare. Poi la dea [[Stacia]] decise di far emergere i cristalli di sale che si trovavano sul fondale. Creò il sole, poi le piante, gli animali e infine l'uomo, partendo da sale a cui diede il dono della vita. 

## Scala della mappa

Un foglio A4 misura in pixel 2480 in larghezza e 3508 in altezza a 300 ppi. In centimetri invece misura 21 x 29.7. Facendo la seguente proporzione

21cm : 2480px = 1cm : x  --> ogni centimetro su un foglio A4 equivale a circa 118px a 300ppi
