---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Fragment

## Fältet Spårningsmall för Google Ads-enheter {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

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

## Spårningsmallfält för [!DNL Microsoft Advertising] entiteter {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Valfritt) Spårningsmallen eller spårnings-URL:en, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar även in URL:en för slut-/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` som ska inkludera en omdirigering.

För spårning av Adobe Advertising-konvertering, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], prefix automatiskt för Sökning, Socialt och Commerce för sin egen omdirigerings- och spårningskod när du sparar posten.

* Information om parametrar som stöds för att bädda in den slutliga URL:en finns i [[!DNL Microsoft Advertising] dokumentationen om parametrar för att ange den slutliga URL:en](https://help.ads.microsoft.com/#apex/3/en/56799).

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel {lpurl}?matchtype={matchtype}&amp;device={device}.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Du kan uppdatera dina spårningsmallar på vilken nivå som helst utan att skicka in dina annonser på nytt för godkännande.

## Text och mall - Obs! Hur man infogar en dynamisk parameter {#inventory-feed-template-insert-dynamic-parameter}

Om du vill infoga ett kolumnnamn eller en modifieringsgrupp som en dynamisk parameter, klickar du i indatafältet och sedan på ett kolumnnamn i kolumnlistan eller ett [modifierarnamn](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) i listan Modifierare. Om du vill infoga variabeln [!DNL Param1] eller [!DNL Param2] anger du värdet `{param1:default text}` eller `{param2:default text}`, där&quot;standardtext&quot; är text som används om parameterkolumnen i matningsfilen är tom för en annonsrad.

## Text- och annonsmall - Observera hur du infogar en annonsanpassare {#inventory-feed-template-insert-ad-customizer}

Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`
