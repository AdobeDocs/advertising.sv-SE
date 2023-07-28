---
title: '''[!DNL Google Ads] annonsinställningar som bara kan anropas'
description: Referera inställningarna för [!DNL Google Ads] annonser som bara kan användas på samtal.
exl-id: 1f810c2b-9c30-43c6-bda6-07609423ef79
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] annonsinställningar som bara kan anropas

Du kan skapa textannonser som bara kan användas för samtal för kampanjer som använder söknätverket.

Sökning, sociala medier och handel spårar endast anropsannonser med hjälp av landningssidans suffix och spårningsmall på kontonivå, men du kan även åsidosätta spårning på kontonivå på annonsnivå i [!DNL Google Ads] Chef.

Se [!DNL Google Ads] hjälp för [annonsbegränsningar per konto](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Företagets namn. Maxlängden är 25 eller 12 dubbelbyte-tecken.

**[!UICONTROL Country]:** (Valfritt) Det land där företaget är beläget.

**[!UICONTROL Phone Number]:** Telefonnumret till företaget. Exempel: (124) 123-4567, 12345678901, +41234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Den första och andra raden i annonsen. Den maximala längden för varje rad är 35 eller 17 dubbelbyte-tecken.

Syntaxen för nyckelordsersättning räknas inte in i maxlängden. Till exempel &quot;`{Description1: Free Account Analysis!}`&quot; behandlas som 22 tecken (endast delen &quot;kostnadsfri kontoanalys\!&quot;).

>[!NOTE]
>
>Beskrivningsfälten får inte innehålla telefonnummer.

**[!UICONTROL Display URL]:** Den URL som visas i annonsen. URL:en måste matcha en domän som är kopplad till ditt företag, men annonsen skickar inte personer till en landningssida.

Den maximala längden är 35 enkelbyte- eller 17 dubbelbyte-tecken. Syntaxen för nyckelordsersättning räknas inte in i maxlängden. Till exempel &quot;`{DisplayURL: example.com}`&quot; behandlas som 11 tecken (endast delen &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Valfritt) En webbsida där annonsens telefonnummer visas som text, så att [!DNL Google Ads] kan verifiera att telefonnumret är giltigt. Den måste ha samma domän som annonsens URL.

**[!UICONTROL Is Tracked]:** Aktiverar samtalsspårning och endast samtalskonverteringar.

**[!UICONTROL Count calls as phone call conversions]:** (När &quot;[!UICONTROL Is Tracked]&quot; är valt; valfritt) Attributerar alla anrop som är ett resultat av annonsen till en viss typ av telefonsamtalskonvertering, när ett sådant har angetts. I annat fall [!DNL Google Ads] skapar en standardkonverteringsåtgärd med namnet &quot;[!UICONTROL Calls from ads]&quot; när den registrerar minst en konvertering från dina vidarebefordringsnummer och sedan attributar anrop till den.

**[!UICONTROL Count Action]:** (När &quot;[!UICONTROL Count calls as phone call conversions]&quot; är markerat; valfritt) Den befintliga konverteringsåtgärden som anrop tilldelas till.

Du kan skapa och hantera konverteringsåtgärder i [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Om annonser](ad-about.md)
>* [Hantera annonser](ad-manage.md)
>* [[!DNL Google Ads] expanderade dynamiska sökannonsinställningar](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] inställningar för responsiv sökning och](ad-settings-google-rsa.md)
