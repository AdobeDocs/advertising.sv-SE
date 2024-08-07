---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Fältet Spårningsmall för Google Ads-enheter

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Valfritt) Spårningsmallen eller spårnings-URL:en, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar även in URL:en för sista sidan/landningssidan i en [!DNL ValueTrack] -parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` som ska inkludera en omdirigering.

För spårning av Adobe Advertising-konvertering, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], prefix automatiskt för Sökning, Socialt och Commerce för sin egen omdirigerings- och spårningskod när du sparar posten.

* Information om parametrar som stöds för att bädda in den slutliga URL:en finns i [[!DNL Google Ads] dokumentationen för de  [!DNL ValueTrack] format](https://support.google.com/google-ads/answer/6305348) som stöds. (Gå till parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängliga [!DNL ValueTrack]-parametrar&quot;.)

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel {lpurl}?matchtype={matchtype}&amp;device={device}.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

>[!NOTE]
>
>* Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Om du uppdaterar en spårningsmall på annons-, sitelink- eller nyckelordsnivå skickas relevanta annonser om för granskning. Du kan uppdatera dina spårningsmallar på konto-, kampanj- eller annonsgruppsnivå utan att skicka in dina annonser på nytt för godkännande.
