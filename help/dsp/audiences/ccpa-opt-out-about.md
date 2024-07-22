---
title: Om [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter
description: Lär dig hur du skapar segment för att spåra ID:n från CCPA-förfrågningar om att avanmäla sig från försäljning och hur du hämtar rapporter om ID:n.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Om [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter

Du kan spåra användar-ID:n från förfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA), genom att [skapa och implementera ett avanmälningssegment för CCPA](ccpa-opt-out-segment-create.md). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar Adobe Advertising samla in en pool med ID:n för annonsörens räkning.

## Rapporter om avanmälan till konsumenter

Adobe Advertising genererar månadsrapporter om ID:n som kunder har skickat in för att avanmäla sig från försäljning för kontot. Data konsoliderar begäranden som samlats in med CCPA-segment för avanmälan från försäljning som skapats i DSP och alla inskickade data via Privacy Service-API.  Rapporterna skapas den första i varje månad för föregående månad. Till exempel är användarlistan för juni tillgänglig den 1 juli.

Varje rapport är tillgänglig som en tabbseparerad textfil komprimerad till GZIP-format. Användar-ID:n som används i CCPA-segment för avanmälan identifieras av segment och annonsörer.

Du kan [hämta länkar till månadsrapporterna](ccpa-opt-out-segment-report-retrieve.md) som skapades de senaste tre månaderna, antingen från DSP eller med DSP [!DNL Trafficking API]. Varje länk gäller i sju dagar, men uppdateras varje gång en kund försöker hämta en länk.

>[!MORELIKETHIS]
>
>* [Stöd för Adobe Advertising i Kaliforniens konsumentsekretesslag: Stöd för konsumentavanmälan](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Skapa och implementera ett [!UICONTROL CCPA Opt-Out-of-Sale] segment ](ccpa-opt-out-segment-create.md)
>* [Hämta rapporter om konsumentens avanmälan från försäljning](ccpa-opt-out-segment-report-retrieve.md)
>* [Om målgruppshantering](audience-about.md)
