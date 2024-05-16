---
title: Hantera delade sitelinks
description: Lär dig hur du skapar och hanterar delade tillägg för sitelink.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: c3b8e387cfc38d195e77761791e689fd094d8f39
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Hantera delade sitelinks

*[!DNL Google Ads]och [!DNL Microsoft Advertising] endast*

Skapa och hantera delade länkar på kontonivå för synkroniserade [!DNL Google Ads] eller [!DNL Microsoft Advertising] konto från [!UICONTROL Extensions] > [!UICONTROL Sitelinks] bibliotek.

## Skapa en delad platshållare

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange [delade inställningar för sitelink](#shared-sitelink-settings).

1. Klicka på **[!UICONTROL Post]**.

När du har skapat en länk kan du [tilldela det till ett konto, en kampanj eller en annonsgrupp](sitelink-extension-associate.md).

## Redigera inställningar för delade länkar

Du kan redigera en delad platshållare åt gången.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Markera kryssrutan bredvid den platslänk som ska redigeras.

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [delade inställningar för sitelink](#shared-sitelink-settings).

1. Klicka på **[!UICONTROL Post]**.

## Ta bort delade länkar

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Markera kryssrutan bredvid varje delad platslänk som du vill ta bort.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på i verktygsfältet ![Mer](/help/search-social-commerce/assets/more.png "Mer") och markera **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]**.

## Inställningar för delad sitelink {#shared-sitelink-settings}

Om du vill ha ytterligare profiler och orsaker till att du inte godkänner sitelink går du till [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) och [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) krav för sitelink-tillägg.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Den text som ska visas för länken. Den kan innehålla upp till 25 enkelbyte- eller 12 dubbelbyte-tecken. Länktexten måste vara unik inom kontot eller kampanjen.

>[!NOTE]
>
>([!DNL Google Ads]) Befintlig text med 35 tecken visas i annonser på datorer och surfplattor, men inte på mobila enheter.

**[!UICONTROL Status]:** Sitelänkens visningsstatus:  *[!UICONTROL Active]* eller *[!UICONTROL Deleted]* (endast befintliga sitelinks). Standardinställningen för nya sitelinks är *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Extra text som sökmotorn kan visa under länktexten. Om du vill ta med en beskrivning anger du värden för båda beskrivningsfälten. Varje beskrivningsfält kan innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.

**[!UICONTROL Start Date]:** (Campaigns with existing legacy sitelinks or no sitelinks only; optional) The first date on which the sitelink may be displayed with ads in the campaign. Standardvärdet för nya sitelinks är den aktuella dagen. Om du vill ange ett framtida startdatum anger du ett datum i formatet MM/DD/ÅÅÅÅ eller M/D/ÅÅÅ, eller klickar och väljer ett datum.

**[!UICONTROL End Date]:** (Valfritt) Det sista datum då platshållaren kan visas med annonser i kampanjen. Som standard kan sitelänken visas i oändlighet. Om du vill ange ett slutdatum anger du ett datum i formatet MM/DD/ÅÅÅÅ eller M/D/ÅÅÅ, eller klickar och väljer ett datum.

**[!UICONTROL Mobile Preference]:** (Valfritt) Tillåter nätverket att försöka visa annonstillägget för användare av mobila enheter i stället för för för dator- eller surfplatteanvändare. Som standard är alternativet inte aktiverat och tillägget visas på alla enhetstyper.

>[!NOTE]
>
>Nätverket garanterar inte att annonseringstillägget visas på den önskade enhetstypen.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen. Inkludera eventuella parametrar som bestämmer sidans innehåll. Om du anger ett värde åsidosätter det annonsens bas-URL.

När du har sparat posten innehåller bas-URL:en eventuella tilläggsparametrar som har konfigurerats för kampanjen eller kontot.

>[!NOTE]
>
>* (Konton med slutliga URL:er) Bas-URL:en kan innehålla omdirigeringar inom landningssidans domän eller underdomän, men inga omdirigeringar utanför landningssidans domän. Annonsnätverket extraherar domänen från den här URL:en och lägger till valfria visningssökvägar för annonsen för att skapa annonsens URL.
>* ([!DNL Google Ads]) Varje sitelink i en kampanj eller annonsgrupp måste ha en unik landningssida, och innehållet för varje sitelink-landningssida måste ha ungefär 80 % unikt innehåll. Du kan t.ex. inte ha länkar till flera ankarpunkter på samma sida.
>* ([!DNL Google Ads]) Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

**[!UICONTROL Tracking Template]:** (Valfritt) Spårningsmallen eller spårnings-URL, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar även in URL:en för sista sidan/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` för att inkludera en omdirigering.

* För spårning av konvertering till Adobe Advertising, som används när kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]&quot; och &quot;Auto Upload&quot;, Search, Social och Commerce prefix automatiskt sin egen klickspårningskod när du sparar posten.

* Information om vilka parametrar som stöds för att bädda in den slutliga URL:en finns i[!DNL Microsoft Advertising] endast) [[!DNL Microsoft Advertising] dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) eller ([!DNL Google Ads] endast) parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängligt&quot; [!DNL ValueTrack] Parametrar&quot; i [[!DNL Google Ads] dokumentation](https://support.google.com/google-ads/answer/6305348).

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel `{lpurl}?matchtype={matchtype}&device={device}`.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

>[!NOTE]
>
>* När kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]och &quot;[!UICONTROL Auto Upload],&quot; Search, Social och Commerce prefixerar automatiskt sin egen omdirigerings- och spårningskod när du sparar posten.
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* ([!DNL Google Ads]) Om du uppdaterar en spårningsmall på sitelink- eller nyckelordsnivå skickas relevanta annonser om för granskning. Du kan uppdatera dina spårningsmallar på konto-, kampanj- eller annonsgruppsnivå utan att skicka in dina annonser på nytt för godkännande.
>* ([!DNL Microsoft Advertising]) Du kan uppdatera dina spårningsmallar på vilken nivå som helst utan att skicka in dina annonser för godkännande på nytt.
>* För [!DNL Google Ads]bör du undvika att använda makron, som inte ersätts med klick från källor som möjliggör parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

>[!MORELIKETHIS]
>
>* [Om tillägg för sitelink](sitelink-extension-about.md)
>* [Associera delade sitelinks med konton, kampanjer och annonsgrupper](sitelink-extension-associate.md)
