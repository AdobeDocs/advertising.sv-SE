---
title: Valfria spårningsparametrar för klickspårnings-URL:er
description: Läs mer om parametrar för sökning, social spårning och Commerce-spårning samt nätverksspecifika spårningsparametrar som du kan lägga till i dina klickspårnings-URL:er.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Valfria spårningsparametrar för klickspårnings-URL:er

Endast *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan] och [!DNL Yandex] konton*

I stället för att bara använda standardspårningsparametrarna för en slutlig URL eller mål-URL kan du lägga till fler parametrar för att spåra specifika data för ett annonsnätverkskonto. Du kan lägga till valfri kombination av följande parametrar i kontoinställningarna eller kampanjinställningarna:

* Du kan lägga till en statisk textsträng som en parameter i bas-URL:erna för kontot/kampanjen.

* Du kan lägga till Adobe Advertising- och annonsspecifika parametrar i bas-URL:erna för kontot/kampanjen för att spåra fler data:

   * Parametrarna Adobe Advertising är halvstatiska. Adobe Advertising infogar ett datavärde när den överför bas-URL:en till annonsnätverket. När du till exempel lägger till `campaign={ef_campaign}` till bas-URL:en ersätter Adobe Advertising `{ef_campaign}` med det faktiska kampanjnamnet (till exempel &quot;Back-to-school-Campaign&quot;) när URL:en överförs.

     **Obs!** När värdena har infogats förblir de statiska. Om du flyttar ett nyckelord eller en annons till en annan annonsgrupp, eller flyttar annonsgruppen till en annan kampanj, uppdateras inte parametern {ef_adgroup} eller {ef_campaign} automatiskt, så du måste generera en ny mål-URL eller bas-URL manuellt.

   * De nätverksspecifika parametrarna är dynamiska och sökmotorn infogar ett datavärde när användaren klickar på en annons. När du till exempel lägger till `{param1}` till bas-URL:en ersätts annonsnätverket med det faktiska {param1}-värdet när en slutanvändare klickar på annonsen.

>[!NOTE]
>
>* Separera flera parametrar med kommatecken eller et-tecken (`&`).
>* Följande parametrar är inte skiftlägeskänsliga.
>* Specialtecken i de tillagda parametrarna ersätts enligt följande i den genererade mål-URL:en eller bas-URL:en (final):
>  * `=` ersätts med `%3D`
>  * `?` ersätts med `%26`
>  * ett tomt utrymme ersätts med `%2B`
>  Om du till exempel lägger till parametern `campaign={ef_campaign}` i bas-URL:en http://www.example.com för ett nyckelord, genereras bas-URL:en för det nyckelordet som `http://www.example.com/campaign%3D{ef_campaign}`.

## Statiska parametrar för sökning, sociala medier och Commerce

Du kan använda följande parametrar för konton i valfritt annonsnätverk och kombinera dem med parametrar för ett specifikt annonsnätverk efter behov. Vissa av dessa parametrar duplicerar de parametrar som läggs till automatiskt för specifika annonsnätverk när kontots spårningsmetod är [!UICONTROL EF Direct].

Alla följande parametrar måste anges som ett nyckelvärdepar. Du kan inkludera flera parametrar för ett värdepar. Om du till exempel vill infoga kampanjnamnet använder du `<your_parameter_name>={ef_campaign}`, till exempel `campaign={ef_campaign}`. Om du vill infoga matchningstypen med angivna matchningstypnamn använder du `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, till exempel `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. De ej tillämpliga matchningstyperna visas inte i den resulterande URL:en.

| Parameter | Beskrivning |
| ---- | ---- |
| <code>{custom_code}</code> | Infoga data från kolumnen Anpassad URL-parameter i en överförd kalkylbladsfil i spårnings-URL:en. {custom_code} får endast användas i slutet av värdet för ett eller flera nyckel/värde-par i spårnings-URL:en. Exempel: <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Obs!</b> Om du vill infoga det anpassade värdet från kalkylbladsfilen i spårnings-URL:en överför du kalkylbladsfilen med alternativet Generera spårnings-URL:er. Mer information om hur du använder kalkylbladsfiler finns i &quot;[Hantera kampanjdata med hjälp av kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;. |
| <code>{ef_uniqueid}</code> | Infoga det unika ID som skapats av Adobe Advertising. Tillagd automatiskt när spårningsmetoden är &quot;EF-omdirigering&quot;. |
| <code>{ef_userid}</code> | Infoga det unika användar-ID som Adobe Advertising tilldelar annonsören. |
| <code>{ef_sid}</code> | Så här infogar du det numeriska ID som Search, Social och Commerce tilldelar annonsnätverket: <i>[!UICONTROL 3]</i> för [!DNL Google Ads], <i>[!UICONTROL 10]</i> för [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> för [!DNL Meta], <i>[!UICONTROL 86]</i> för [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> för [!DNL Naver], <i>[!UICONTROL 88]</i> för [!DNL Baidu], <i>[!UICONTROL 90]</i> för [!DNL Yandex], <i>[!UICONTROL 94]</i> för [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> [!DNL Yahoo Native] för  (utgått) eller <i>[!UICONTROL 106]</i> för [!DNL Pinterest] (utgått). |
| <code>{ef_searchengine}</code> | Infoga annonsnätverksnamnet. |
| <code>{ef_campaign}</code> | Infoga kampanjnamnet. |
| <code>{ef_campaignid}</code> | Infoga kampanj-ID. <b>Obs!</b> ID:t för en ny kampanj skapas inte förrän kampanjen har publicerats i annonsnätverket. Om kontot använder alternativen [!UICONTROL EF Redirect] och AutoUpload infogar Adobe Advertising automatiskt kampanj-ID i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] och du vill infoga kampanj-ID i relevanta mål-URL:er eller slutliga URL:er, måste du skapa kampanjen, hämta en kalkylbladsfil för den nya kampanjen med alternativet Generera URL:er för spårning och sedan skicka filen till annonsnätverket. |
| <code>{ef_adgroup}</code> | Infoga annonsgruppens namn. |
| <code>{ef_adgroupid}</code> | Infoga annonsgruppens ID. <b>Obs!</b> ID:t för en ny annonsgrupp skapas inte förrän annonsgruppen är registrerad i annonsnätverket. Om kontot använder alternativen [!UICONTROL EF Redirect] och AutoUpload infogar Adobe Advertising automatiskt annonsgrupps-ID i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] och du vill infoga annonsgruppens ID i de relevanta mål-URL:erna eller de slutliga URL:erna, måste du skapa annonsgruppen, hämta en kalkylbladsfil för den nya annonsgruppen med alternativet Generera URL:er för spårning och sedan publicera filen i annonsnätverket. |
| <code>{ef_keyword}</code> | Infoga nyckelordet. |
| <code>{ef_keywordid}</code> | Infoga nyckelords-ID. <b>Obs!</b> ID:t för ett nytt nyckelord skapas inte förrän nyckelordet har publicerats i annonsnätverket. Om kontot använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] infogar Adobe Advertising automatiskt nyckelords-ID i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] och du vill infoga nyckelords-ID i relevanta mål-URL:er eller slutliga URL:er, måste du skapa nyckelordet, hämta en kalkylbladsfil för det nya nyckelordet med alternativet Generera URL:er för spårning och sedan skicka filen till annonsnätverket. |
| <code>{ef_matchtype}</code> | Om du vill infoga nyckelordsmatchningstypen som &quot;Bred&quot;, &quot;Exakt&quot; eller &quot;Fras&quot;. Ingår automatiskt för [!DNL Google Ads] och [!DNL Microsoft Advertising] med spårningsmetoden [!UICONTROL EF Redirect]. |
| <code>{ef_adid}</code> | Infoga annons-ID. <b>Obs!</b> ID:t för en ny annons skapas inte förrän annonsen har publicerats i annonsnätverket. Om kontot använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] infogar Adobe Advertising automatiskt annons-ID i relevanta mål-URL:er eller slutliga URL:er nästa dag. Om kontot inte använder alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] och du vill infoga annons-ID i relevanta mål-URL:er eller slutliga URL:er, måste du skapa annonsen, hämta en kalkylbladsfil för den nya annonsen med alternativet Generera URL:er för spårning och sedan skicka filen till annonsnätverket. |

## [!DNL Google Ads] parametrar för dynamisk spårning

Se [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] parametrar för dynamisk spårning

Se [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Japan lägger till dynamiska spårningsparametrar

Se [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] parametrar för dynamisk spårning

Se [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för tjänsten för spårning av konvertering av Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
