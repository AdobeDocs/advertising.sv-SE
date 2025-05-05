---
title: Översikt över Campaign Management i Advertising DSP
description: Lär dig mer om kampanjhanteringshierarkin och komponenter.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Översikt över Campaign Management i Advertising DSP

DSP har följande hierarki:

* Campaign
   * Paket
      * Placering(ar)
         * Annons(er)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Kampanjer](/help/dsp/campaign-management/campaigns/campaign-about.md) är det övergripande ramverket för flyginställningar. Varje kampanj är konfigurerad med en annonsörer, start- och slutdatum, en övergripande budget, ett alternativ för målinriktning mellan olika enheter och standardfrekvens samt rapporteringsalternativ för visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering. Alla inställningar på kampanjnivå gäller automatiskt för varje paket och placering i kampanjen.

## [!UICONTROL Packages]

Varje kampanj kan innehålla ett eller flera [paket](/help/dsp/campaign-management/packages/package-about.md), som vart och ett innehåller en uppsättning placeringar.

Använd paket för att gruppera placeringar för leverans till en fast budget, prestationsmål och anpassad paketeringsstrategi. DSP optimerar paket genom att flytta budgeten till de bästa placeringarna i paketet. Du kan ordna paket efter placeringsformat, lagertyp, dataleverantör, persona eller andra särskiljbara egenskaper.

Paket är valfria men rekommenderas.

## [!UICONTROL Placements]

En [placering](/help/dsp/campaign-management/placements/placement-about.md) lagrar målparametrar för en eller flera annonser av samma annonstyp. Du kan skapa en placering för en enskild kampanj eller ett paket och sedan tilldela annonser till den.

## [!UICONTROL Ads]

[Ads](/help/dsp/campaign-management/ads/ad-about.md) innehåller kreativa resurser och URL:er för spårning. Du kan överföra tredjepartsannonser som servar taggar individuellt eller gruppvis med hjälp av partnertaggmallar eller mallen för bulktaggar. Du kan också skapa inbyggda displayannonser manuellt för DSP.

När annonserna har konfigurerats måste du bifoga varje annons till en plats för att börja köra annonsen. Du kan bifoga en annons till en eller flera ersättningar.

Alla aktiva, godkända annonser i en aktiv placering i en aktiv kampanj kan köras baserat på parametrarna för riktade placeringar.

>[!MORELIKETHIS]
>
>* [Om Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Om pakethantering](/help/dsp/campaign-management/packages/package-about.md)
>* [Om placeringshantering](/help/dsp/campaign-management/placements/placement-about.md)
>* [Om annonshantering](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checklista för kampanjstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Bästa metoder för att konfigurera prestandakampanjer](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Typer av prestandarapporter i Campaign Management-vyer](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Hantera dina kampanjdatavyer](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP och användargränssnitt](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=sv-SE)
