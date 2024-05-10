---
title: Om målgrupper
description: Lär dig mer om alternativ för att spåra, skapa och hantera [!DNL Google Ads] och [!DNL Microsoft Advertising] målgrupper.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Om hantering [!DNL Google Ads] och [!DNL Microsoft Advertising] målgrupper i sökningar, sociala medier och Commerce

*[!DNL Google Ads]och [!DNL Microsoft Advertising] endast*

I publikbiblioteket visas alla dina [!DNL Google Ads] kunddatabaserade, marknadsinterna och liknande målgrupper och era [!DNL Microsoft Advertising] återmarknadsföring och dynamisk återmarknadsföring, anpassad marknadsföring, kundmatchning, marknadsinriktade och liknande målgrupper. Du kan använda någon av [!DNL Google Ads] målgrupper [!DNL Google Ads] mål och undantag på kampanjnivå och annonsnivå, och du kan använda vilken som helst av [!DNL Microsoft Advertising] målgrupper [!DNL Microsoft Advertising] mål på kampanjnivå och annonsnivå och (endast för dynamisk återmarknadsföring) undantag. Du kan lägga till eller redigera en anbudsjustering för alla målgrupper.

Du kan också skapa och hantera målgrupper med hjälp av segment eller e-postlistor från dina befintliga Adobe Experience Cloud-målgrupper och från olika typer av kunddata från CRM-systemet:

* **Adobe målgruppssegment:** Annonsörer med Adobe Audience Manager- eller Adobe Analytics-konton kan skapa [!DNL Google Ads] matchar kunderna målgrupper utifrån deras [!DNL Adobe] segment:

   * (Annonsörer med [!DNL Analytics] konton som inte har Audience Manager) Du kan skapa [!DNL Google Ads] kundmatcha målgrupper med användar-ID från [!DNL Analytics] segment som delas med Adobe Experience Cloud.

   * (Annonsörer med Audience Manager-konton) Du kan skapa [!DNL Google Ads] som matchar målgrupper med användar-ID:n från Audience Manager-segment som har Search, Social och Commerce som mål. Detta kan omfatta Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapats med Adobe Experience Cloud Audience Library.

  För att skapa kundmatchande målgrupper måste annonsören [!DNL Google Ads] kontot måste [kan få anpassad matchning](https://support.google.com/adspolicy/answer/6299717) och har valt [användar-ID-segment](https://support.google.com/google-ads/answer/9199250). Annonsörskontot i Search, Social och Commerce måste också konfigureras så att kundmatchande målgrupper kan skapas.

  [!DNL Adobe] segmentdata och cookie-synkroniseringsfiler för kunddatabaserade målgrupper synkroniseras till [!DNL Google Ads] varje dag.

* **Adobe Campaign e-postlistor:** Kontoteamet på Adobe kan hjälpa dig att konfigurera ett arbetsflöde för att skapa och uppdatera en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista inom [!DNL Campaign].

* **Kunddatalistor:** Annonsörer med [!DNL Google Ads] eller [!DNL Microsoft Advertising] konton som är berättigade till kundmatchning kan skapa och uppdatera en annonsspecifik kunddatabaserad målgrupp &lt;!>- eller dynamisk publik för återmarknadsföring - ingår i kunddatabaserade målgrupper, åtminstone för [!DNL Google Ads]?—> genom att överföra en CSV-fil med primära identifierare.

* **Dynamiska remarketing-listor:** Annonsörer med [!DNL Microsoft Advertising] konton kan skapa och hantera dynamiska återmarknadsföringsmålgrupper, som ni kan använda för att omdirigera potentiella kunder som nyligen har interagerat med era produkter på ett av flera olika sätt (som produktvisningsprogram eller tidigare köpare). Målgrupper med dynamisk återmarknadsföring kräver att ni använder annonsnätverkets JavaScript-konvertering och målgruppsspårningstagg på era webbsidor. Använd dynamiska ommarknadsföringslistor med shoppingkampanjer i sök- och målgruppsnätverk för att omdirigera målgrupper med produktannonser, samt med sökkampanjer för att omdirigera målgrupper med textannonser och dynamiska sökannonser. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Anbudsmodifierare för målgrupper för dynamisk återmarknadsföring optimeras inte i portföljer med &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social, &amp; Commerce lagrar inte kunddata som du överför eller från [!DNL Adobe] segment som används för att skapa eller redigera en [!DNL Google Ads] eller [!DNL Microsoft Advertising] målgrupp.

>[!MORELIKETHIS]
>
>* [Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera kundmatchande målgrupper med hjälp av kunddatalistor](audience-from-customer-data-list.md)
>* [Hantera målgrupper för dynamisk återmarknadsföring](audience-dynamic-remarketing-manage.md)
>* [Hantera målgruppsmål för kampanjer och annonsgrupper](audience-targets-manage.md)
>* [Hantera publikundantag för kampanjer och annonsgrupper](audience-exclusions-manage.md)
