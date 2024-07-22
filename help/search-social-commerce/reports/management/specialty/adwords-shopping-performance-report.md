---
title: '[!UICONTROL AdWords Shopping Performance Report]'
description: Läs mer om [!UICONTROL AdWords Shopping Performance Report].
exl-id: 891c8940-bf92-455c-a6f3-92e2a0122b4a
feature: Search Reports, Search Specialty Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# [!UICONTROL AdWords Shopping Performance Report]

Endast *[!DNL Google Ads]konton*

[!UICONTROL AdWords Shopping Performance Report] innehåller kostnads-, klicknings- och visningsdata, konverterade klicknings- och konverteringsdata som spåras av [!DNL Google Ads Conversion Optimizer] och (valfritt) konverteringsdata som spåras av [!DNL Adobe] och härledda mätdata som aggregerats på produkt-ID-nivå för en eller flera annonsgrupper i shoppingkampanjer. Som standard innehåller data en rad för varje produkt-ID och produktkategori per annonsgrupp för varje tidsenhet i det angivna datumintervallet. Raderna placeras i stigande ordning efter kontonamn, kampanjnamn och sedan som standard efter gruppnamn.

Du kan visa data för de senaste två månaderna. Data före den 21 september 2018 kan visas på två rader: en rad med kostnads- och klickdata och en rad med konverteringsdata som spåras av Adobe. Efterföljande data visas på en rad.

>[!NOTE]
>
>* Om produkten innehåller kolumnen [!UICONTROL Product Category], och en produkt visas i flera kategorier, visas produkten i flera rader och antalet konverteringar dupliceras i var och en av de tillämpliga raderna. Eftersom konverteringsdatasummorna inte är korrekta kan du bara sortera data per kategori för att få en allmän förståelse för hur konverteringar sker per kategori.
>* Data för den här rapporten hämtas för föregående dag kl. 23.00 varje dag. Exempelvis hämtas data för 17 juni kl. 23.00 den 18 juni. Om du kör rapporten den 19 juni kl. 9.00 - innan data för 18 juni hämtas - innehåller rapporten data fram till 17 juni kl. 23.00.

## Standardkolumner

Beskrivningar av alla standardkolumner och anpassade kolumner finns i [Rapportera kolumner för specialrapporter](specialty-report-columns.md).

* [!UICONTROL Account Name]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Product ID]
* [!UICONTROL Category (1st level - 5th level)]
* [!UICONTROL Product Type (1st level - 5th level)]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Google Converted Clicks]
* [!UICONTROL Google Conversions]
* [!UICONTROL CTR]
* [!UICONTROL CPC]

>[!MORELIKETHIS]
>
>* [Om specialrapporter](specialty-report-about.md)
>* [Generera en specialrapport](specialty-report-generate.md)
>* [Inställningar för specialrapport](specialty-report-settings.md)
