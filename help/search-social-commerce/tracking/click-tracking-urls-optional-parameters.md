---
title: Valfria spårningsparametrar för klickspårnings-URL:er
description: Lär dig mer om parametrar för sökning, social spårning och handelsuppföljning samt om nätverksspecifika spårningsparametrar som du kan lägga till i dina klicknings-spårnings-URL:er.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: cc312009303f86a2f9eddcc98f33d7e2c22fcb85
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# Valfria spårningsparametrar för klickspårnings-URL:er

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo Native], [!DNL Yahoo! Japan]och [!DNL Yandex] endast konton*

I stället för att bara använda standardspårningsparametrarna för en slutlig URL eller mål-URL kan du lägga till fler parametrar för att spåra specifika data för ett annonsnätverkskonto. Du kan lägga till valfri kombination av följande parametrar i kontoinställningarna eller kampanjinställningarna:

* Du kan lägga till en statisk textsträng som en parameter i bas-URL:erna för kontot/kampanjen.

* Du kan lägga till Adobe Advertising- och annonsspecifika parametrar i bas-URL:erna för kontot/kampanjen för att spåra fler data:

   * Parametrarna Adobe Advertising är halvstatiska. Adobe Advertising infogar ett datavärde när den överför bas-URL:en till annonsnätverket. När du t.ex. lägger till `campaign={ef_campaign}` Adobe Advertising ersätter bas-URL:en `{ef_campaign}` med det faktiska kampanjnamnet (t.ex. &quot;Back-to-school-Campaign&quot;) när URL:en överförs.

     **Obs!** När värdena har infogats förblir de statiska. Om du flyttar ett nyckelord eller en annons till en annan annonsgrupp, eller flyttar annonsgruppen till en annan kampanj, kan du  {ef_adgroup} eller {ef_campaign} parametern uppdateras inte automatiskt, så du måste generera en ny mål-URL eller en ny bas-URL (slutlig) manuellt.

   * De nätverksspecifika parametrarna är dynamiska och sökmotorn infogar ett datavärde när användaren klickar på en annons. När du t.ex. lägger till `{param1}` till bas-URL:en ersätter annonsnätverket den med den faktiska {param1} när en slutanvändare klickar på annonsen.

>[!NOTE]
>
>* Separera flera parametrar med kommatecken eller et-tecken (`&`).
>* Följande parametrar är inte skiftlägeskänsliga.
>* Specialtecken i de tillagda parametrarna ersätts enligt följande i den genererade mål-URL:en eller bas-URL:en (final):
>  * `=` ersätts med `%3D`
>  * `?` ersätts med `%26`
>  * ett tomt utrymme ersätts med `%2B`
>  När du t.ex. lägger till parametern `campaign={ef_campaign}` till bas-URL:en http://www.example.com för ett nyckelord genereras bas-URL:en för det nyckelordet som `http://www.example.com/campaign%3D{ef_campaign}`.

## Statiska spårningsparametrar för sökning, sociala medier och handel

Du kan använda följande parametrar för konton i valfritt annonsnätverk och kombinera dem med parametrar för ett specifikt annonsnätverk efter behov. Vissa av dessa parametrar duplicerar de parametrar som läggs till automatiskt för specifika annonsnätverk när kontots spårningsmetod är &quot;[!UICONTROL EF Direct].&quot;

Alla följande parametrar måste anges som ett nyckelvärdepar. Du kan inkludera flera parametrar för ett värdepar. Om du till exempel vill infoga kampanjnamnet använder du `<your_parameter_name>={ef_campaign}`, till exempel `campaign={ef_campaign}`. Om du vill infoga matchningstypen med angivna matchningstypnamn använder du `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, till exempel `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. De ej tillämpliga matchningstyperna visas inte i den resulterande URL:en.

| Parameter | Beskrivning |
| ---- | ---- |
| <code>{custom_code}</code> | Infoga data från kolumnen Anpassad URL-parameter i en överförd kalkylbladsfil i spårnings-URL:en. {custom_code} kan bara användas i slutet av värdet för ett eller flera nyckelvärdepar i spårnings-URL:en. Exempel:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Obs!</b> Om du vill infoga det anpassade värdet från kalkylbladsfilen i spårnings-URL:en överför du kalkylbladsfilen med alternativet Generera spårnings-URL:er. Mer information om hur du använder kalkylbladsfiler finns i &quot;[Hantera kampanjdata med hjälp av kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| <code>{ef_uniqueid}</code> | Infoga det unika ID som skapats av Adobe Advertising. Tillagd automatiskt när spårningsmetoden är &quot;EF-omdirigering&quot;. |
| <code>{ef_userid}</code> | Infoga det unika användar-ID som Adobe Advertising tilldelar annonsören. |
| <code>{ef_sid}</code> | Så här infogar du det numeriska ID som tilldelas annonsnätverket i Search, Social och Commerce: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft®® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (borttagen), eller <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (föråldrat). |
| <code>{ef_searchengine}</code> | Infoga annonsnätverksnamnet. |
| <code>{ef_campaign}</code> | Infoga kampanjnamnet. |
| <code>{ef_campaignid}</code> | Infoga kampanj-ID. <b>Obs!</b> ID:t för en ny kampanj skapas inte förrän kampanjen har publicerats i annonsnätverket. Om kontot använder &quot;[!UICONTROL EF Redirect]Alternativ för &quot; och &quot;AutoUpload&quot;, infogar Adobe Advertising automatiskt kampanj-ID i relevanta mål-URL:er eller slutliga URL:er nästa dag. Om kontot inte använder[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; och du vill infoga kampanj-ID i relevanta mål-URL:er eller slutliga URL:er måste du skapa kampanjen, hämta en kalkylbladsfil för den nya kampanjen med alternativet&quot;Generera URL:er för spårning&quot; och sedan skicka filen till annonsnätverket. |
| <code>{ef_adgroup}</code> | Infoga annonsgruppens namn. |
| <code>{ef_adgroupid}</code> | Infoga annonsgruppens ID. <b>Obs!</b> ID:t för en ny annonsgrupp skapas inte förrän annonsgruppen har bokförts i annonsnätverket. Om kontot använder &quot;[!UICONTROL EF Redirect]och alternativen &quot;AutoUpload&quot; infogar Adobe Advertising automatiskt annonsgrupps-ID:t i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; och du vill infoga annonsgruppens ID i de relevanta mål-URL:erna eller de slutliga URL:erna, måste du skapa annonsgruppen, hämta en kalkylbladsfil för den nya annonsgruppen med alternativet&quot;Generera URL:er för spårning&quot; och sedan skicka filen till annonsnätverket. |
| <code>{ef_keyword}</code> | Infoga nyckelordet. |
| <code>{ef_keywordid}</code> | Infoga nyckelords-ID. <b>Obs!</b> ID:t för ett nytt nyckelord skapas inte förrän nyckelordet har publicerats i annonsnätverket. Om kontot använder &quot;[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; infogar Adobe Advertising automatiskt nyckelords-ID:t i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; och om du vill infoga nyckelords-ID i de relevanta mål-URL:erna eller de slutliga URL:erna måste du skapa nyckelordet, hämta en kalkylbladsfil för det nya nyckelordet med alternativet&quot;Generera URL:er för spårning&quot; och sedan skicka filen till annonsnätverket. |
| <code>{ef_matchtype}</code> | Om du vill infoga nyckelordsmatchningstypen som &quot;Bred&quot;, &quot;Exakt&quot; eller &quot;Fras&quot;. Ingår automatiskt i [!DNL Google Ads] och [!DNL Microsoft® Advertising] med &quot;[!UICONTROL EF Redirect]&quot; spårningsmetod. |
| <code>{ef_adid}</code> | Infoga annons-ID. <b>Obs!</b> ID:t för en ny annons skapas inte förrän annonsen har publicerats i annonsnätverket. Om kontot använder &quot;[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; infogar Adobe Advertising automatiskt annons-ID i de relevanta mål-URL:erna eller de slutliga URL:erna nästa dag. Om kontot inte använder[!UICONTROL EF Redirect]&quot; och [!UICONTROL Auto Upload]&quot; och du vill infoga annons-ID i de relevanta mål-URL:erna eller de slutliga URL:erna måste du skapa annonsen, hämta en kalkylbladsfil för den nya annonsen med alternativet&quot;Generera URL:er för spårning&quot; och sedan skicka filen till annonsnätverket. |

## [!DNL Google Ads] dynamiska spårningsparametrar

Se [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft® Advertising] dynamiska spårningsparametrar

Se [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

&lt;&lt;&lt;&lt;&lt;&lt; Uppdaterat uppströms
## [!DNL Yahoo Native] dynamiska spårningsparametrar

Se [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## [!DNL Yahoo! Japan Ads] dynamiska spårningsparametrar
=======
## Yahoo! Japan lägger till dynamiska spårningsparametrar
>>>>>>>>>>Streckade ändringar
> 
Se [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] dynamiska spårningsparametrar

Se [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
* [Om URL-format för klickspårning för tjänsten för spårning av konvertering i Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
