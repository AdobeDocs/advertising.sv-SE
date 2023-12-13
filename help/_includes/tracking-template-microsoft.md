---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Fältet Spårningsmall för Microsoft Advertising entities

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Valfritt, inte tillgängligt för alla enheter) Spårningsmallen eller spårnings-URL, som anger alla omdirigeringar och spårningsparametrar utanför landningsdomänen och även bäddar in URL:en för sista sidan/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` för att inkludera en omdirigering.

För spårning av konvertering till Adobe Advertising, som används när kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]och &quot;[!UICONTROL Auto Upload],&quot; Sökning, sociala medier och handel prefixar automatiskt sin egen omdirigerings- och spårningskod när du sparar posten.

* Information om vilka parametrar som stöds för att bädda in den slutliga URL:en finns i [[!DNL Microsoft Advertising] dokumentation om parametrar för att ange den slutliga URL:en](https://help.ads.microsoft.com/#apex/3/en/56799).

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel {lpurl}?matchtype={matchtype}&amp;device={device}.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Du kan uppdatera dina spårningsmallar på vilken nivå som helst utan att skicka in dina annonser på nytt för godkännande.
