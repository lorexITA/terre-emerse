---
tags:
  - "#Letter"
quicknote: ""
holder: "[[Theldor Ulrik]]"
recipient:
  - "[[Theldor Ulrik]]"
status: ✅
servicecost: 1M$
sentdate: 5 Maturio 812
deliverydate: 7 Maturio 812
sender:
  - "[[Tilda Stonefoot]]"
sentfrom:
  - "[[Locanda dell'Alce Zoppa]]"
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
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>> **Holder** | `INPUT[Null][suggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):holder]` |
>> **Letter Sender** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):sender]` |
>> **Sent From Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):sentfrom]` |
>> **Recipient Of Letter** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):recipient]` |
>> **Sent To Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):sentto]` |
>> **Cost** |  `INPUT[textArea:servicecost]`
>> **Sent Date** |  `INPUT[textArea:sentdate]` |
>> **Estimated Delivery Date** |  `INPUT[textArea:deliverydate]` |
>> **Previous Letter** | `INPUT[inlineListSuggester(optionQuery(#Letter AND !"z_Templates"), useLinks(partial)):previous]` |
>> **Next Letter** | `INPUT[inlineListSuggester(optionQuery(#Letter AND !"z_Templates"), useLinks(partial)):next]` |
>> **Letter Status** | `INPUT[Status][:status]` |

> [!infobox]
> #### Letter Info
>  |
> ---|---|
> **Sent Date** | `VIEW[{sentdate}]` |
> **Estimated Delivery** | `VIEW[{deliverydate}]` |
> **Status** | `VIEW[{status}]` |
> **Owner** | `VIEW[{holder}][link]` |
> **Previous Letter** | `VIEW[{previous}][link]` |
> **Next Letter** | `VIEW[{next}][link]` |

# **To:** `VIEW[{recipient}][link]`  <span style="font-size: medium">**Location:** `VIEW[{sentto}][link]`</span> 
Letter contents that has been sent to the Character.

- **From:** `VIEW[{sender}][link]` <span style="font-size: small">**Location:** `VIEW[{sentfrom}][link]` </span> 

> Caro Theldor,
> 
 Finalmente è arrivato il momento di entrare in azione. Ti chiedo di infiltrarti nel [[TEMPIO A STACIA]] come un comune studioso. Il tuo obbiettivo è creare quanto più scompiglio possibile: hai carta bianca sul come. Dobbiamo distrarre i [[Cavalieri di Stacia]] e spargere terrore nel popolo. In cambio riceverai la promozione che tanto volevi.
> 
> Cordiali Saluti
> 
> Volpe Nera






## Notes

Quando si legge la lettera **<font color="#ff0000">NON</font>** bisogna dire il nome di [[Tilda Stonefoot]], ma usare il soprannome Volpe Nera
Invece si **<font color="#00b050">DEVE</font>** dire al party che la lettera è stata spedita dalla [[Locanda dell'Alce Zoppa]]
