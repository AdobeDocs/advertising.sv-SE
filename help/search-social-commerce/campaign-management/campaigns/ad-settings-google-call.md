---
title: '[!DNL Google Ads] annonsinställningar endast för anrop'
description: Referera inställningarna för  [!DNL Google Ads] annonser som bara är för samtal.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Annonsinställningar för endast [!DNL Google Ads] samtal

Du kan skapa textannonser som bara kan användas för samtal för kampanjer som använder söknätverket.

Sökning, sociala medier och Commerce spårar annonser som bara kan anropas med landningssidans suffix och spårningsmall på kontonivå, men du kan även åsidosätta spårning på kontonivå på annonsnivå i [!DNL Google Ads] Manager.

Se hjälpen för [!DNL Google Ads] för [annonsbegränsningar per konto](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Företagets namn. Maxlängden är 25 eller 12 dubbelbyte-tecken.

**[!UICONTROL Country]:** (Valfritt) Det land där företaget finns.

**[!UICONTROL Phone Number]:** Telefonnumret för företaget. Exempel: (124) 123-4567, 12345678901, +41234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Den första och andra raden i annonsen. Den maximala längden för varje rad är 35 eller 17 dubbelbyte-tecken.

Syntaxen för nyckelordsersättning räknas inte in i maxlängden. Till exempel behandlas `{Description1: Free Account Analysis!}` som 22 tecken (endast delen&quot;Analys av kostnadsfritt konto\!&quot;).

>[!NOTE]
>
>Beskrivningsfälten får inte innehålla telefonnummer.

**[!UICONTROL Display URL]:** Den URL som visas i annonsen. URL:en måste matcha en domän som är kopplad till ditt företag, men annonsen skickar inte personer till en landningssida.

Den maximala längden är 35 enkelbyte- eller 17 dubbelbyte-tecken. Syntaxen för nyckelordsersättning räknas inte in i maxlängden. Till exempel behandlas `{DisplayURL: example.com}` som 11 tecken (endast delen&quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Valfritt) En webbsida där annonsens telefonnummer visas som text, så att [!DNL Google Ads] kan verifiera att telefonnumret är giltigt. Den måste ha samma domän som annonsens URL.

**[!UICONTROL Is Tracked]:** Aktiverar samtalsspårning och endast samtalskonverteringar.

**[!UICONTROL Count calls as phone call conversions]:** (När [!UICONTROL Is Tracked] har valts, valfritt) Attribuerar alla anrop som kommer från annonsen till en viss typ av konvertering av telefonsamtal, när ett sådant har angetts. I annat fall skapar [!DNL Google Ads] en standardkonverteringsåtgärd med namnet [!UICONTROL Calls from ads] när minst en konvertering från dina vidarebefordringsnummer registreras och sedan attributanrop till den.

**[!UICONTROL Count Action]:** (När [!UICONTROL Count calls as phone call conversions] har valts, valfritt) Den befintliga konverteringsåtgärden som anrop tilldelas till.

Du kan skapa och hantera konverteringsåtgärder inom [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Om annonser](ad-about.md)
>* [Hantera annonser](ad-manage.md)
>* [[!DNL Google Ads] utökade inställningar för dynamisk sökning och annonser](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Inställningar för responsiv sökannonsering](ad-settings-google-rsa.md)
