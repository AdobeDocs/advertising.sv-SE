---
title: Använder [!DNL Roku] lager
description: Lär dig mer om att DSP partnerskap med  [!DNL Roku], inklusive lageralternativ, godkända tredjepartsspårningsleverantörer och metodtips för  [!DNL Roku]-specifika placeringar.
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Använder [!DNL Roku]-lager

Advertising DSP tillhandahåller funktioner för annonsering på [!DNL Roku].

## Målgruppsmatchning

Kopplingen [!DNL Roku] och DSP matchar dina [!DNL DSP]-målgrupper med [!DNL Roku] ID:n för 1:1-deterministisk målgruppsanpassning på [!DNL Roku]-lagret.

## [!DNL Roku] lageralternativ

Du kan antingen a) konfigurera privata avtal-ID:n direkt med [!DNL Roku] och sedan ange data för avtal-ID i DSP eller b) gå till [!DNL On Demand] Gallery för att prenumerera på [!DNL Roku]-profiler:

>[!NOTE]
>
>[!DNL Roku] lager är inte tillgängligt på öppna marknadsplatser och börser.

* För dina privata avtal [ställer du in information om erbjudande-ID:n i DSP](/help/dsp/inventory/deal-id-create.md) och sedan anger [!UICONTROL Roku Network - Audience] och [!UICONTROL The Roku Channel - Audience] som mål i [!DNL Roku]-placeringar.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Du kan [prenumerera på följande [!DNL Roku] lager i  [!DNL On Demand] galleriet](/help/dsp/inventory/on-demand-inventory-subscribe.md) och sedan rikta in dig på något av de godkända erbjudandena på [!DNL Roku]-platser:

   * &quot;[!UICONTROL Roku Network - Audience]&quot; för inventering i hela [!DNL Roku]-ekosystemet med partners för premiuminnehåll, som [!DNL The CW], [!DNL ABC] och [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; för [!DNL Roku] ägt och styrt (O&amp;O) appinnehåll.

### Fördelar med att anpassa privata marknadsplatser med [!DNL Roku]

Med privata avtal kan ni anpassa avtalsparametrarna efter era behov.

* **Förhandlat pris:** Arbeta med säljteamet [!DNL Roku] för att förhandla och strukturera ett avtal som uppfyller era kampanjbehov.

* **Skalprioritet:** Privata marknadsplatser (PMP) får högre prioritet än alltid aktiverade erbjudanden (till exempel [!DNL On Demand] erbjudanden).

* **Frekvenshantering:** Standardfrekvensbegränsningen [!DNL Roku] är en (1) och en (30) minut per användare, men du kan anpassa ändpunkten efter timme, dag, vecka, månad eller hela flygperioden.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Datamål:** [!DNL Roku] målgrupper byggs från [!DNL Roku] enhets- och tv-signaler, data som spåras av [!DNL The Roku Channel] (till exempel tv-genre, beteende för direktuppspelad TV och kabelprenumerationsstatus) och ytterligare data från CRM-systemet ([!DNL Roku] customer relationship management). 

* **[!DNL Roku]Målgruppsinriktning:** Privata avtal kan rikta in appar efter genre, program med blockeringslista, säsongs- och interpoleringshändelser och program endast visas i [!DNL The Roku Channel].

## [!DNL Roku] placeringar

I DSP-kampanjer [skapar [!DNL Roku]-specifika placeringar](/help/dsp/campaign-management/placements/placement-create.md) med placeringstypen [!UICONTROL Connected TV (Roku)]. Inkludera [!DNL Roku] placeringar i [!DNL Roku]-specifika paket med definierade mål.

Varje [!DNL Roku]-placering måste ha minst en [!DNL Roku]-affär eller källa som mål. Om du vill använda DSP målgruppsmatchning med [!DNL Roku] inkluderar du ett eller flera målgruppssegment som kan matchas mot den [!DNL Roku] (insticksprogram) deterministiska datamängden.

### [!DNL Roku]-Godkända tredjepartsleverantörer för spårning

[!DNL Roku]-placeringar kan innehålla händelsepixlar från tredje part och konverteringspixlar från följande leverantörer: [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] och [!DNL Research Now].

### Bästa praxis efter placeringsstrategi

Nedan följer de rekommenderade metoderna för [!DNL Roku]-specifika placeringar.

Så här maximerar du inkrementell räckvidd:

* Utelämna exponerade målgrupper på [!DNL Roku O&O] genom att exkludera målgrupper som du redan har nått med [!DNL The Roku Channel].

* Utelämna exponerade målgrupper på [!DNL All Roku] genom att utesluta målgrupper som du redan har nått på [!DNL Roku]-plattformen.

För snabbaste konfiguration:

* Använd befintliga, alltid aktiverade erbjudanden för [!DNL The Roku Channel] i [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) för att snabbt få åtkomst till [!DNL Roku] ägda och hanterade lager.
* Rikta befintliga, alltid aktiverade erbjudanden för [!DNL Roku Network] i [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) för att snabbt uppnå skalbarhet på hela [!DNL Roku]-plattformen.

Till maximal skala:

* Anpassa en [!DNL Roku] privat marknadsplats för prioriterad åtkomst till [!DNL Roku]-leverans till ett förhandlat pris.

>[!MORELIKETHIS]
>
>* [Skapa information om avtal-ID manuellt](/help/dsp/inventory/deal-id-create.md)
> * [Prenumerera och begär åtkomst till [!DNL On Demand] Premium Inventory Deals](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Skapa en placering](/help/dsp/campaign-management/placements/placement-create.md)
