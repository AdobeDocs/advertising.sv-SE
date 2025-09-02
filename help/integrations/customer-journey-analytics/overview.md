---
title: Översikt över integrationen mellan Adobe Advertising och Adobe Customer Journey Analytics
description: Läs om hur du kan integrera Adobe Advertising med Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: ca039c91a976d79ed732ad7e0435566d58f3f843
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Översikt över integrationen mellan Adobe Advertising och Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Annonsörer med Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising är integrerat med Adobe Customer Journey Analytics för dubbelriktad datadelning och rapportering. Det finns två alternativ för att konfigurera integreringen:

* Annonsörer med både [!DNL Analytics for Advertising] och Customer Journey Analytics har samma funktioner som de har via [!DNL Analytics for Advertising], med tillägg av visualiseringar i Customer Journey Analytics.

  Du kan fortfarande spåra klickningshändelser med Adobe Experience Platform Web SDK (`alloy.js`) eller Adobe Experience Cloud Identity Service (`visitorAPI.js`). Annonsörer med Advertising DSP kommer fortfarande att använda ett JavaScript-kodfragment för att spåra visningshändelser. Data som finns i Customer Journey Analytics inkluderar:

   * Kampanjresultatdata från Adobe Advertising i Customer Journey Analytics

   * Webbplatsaktivitet och konverteringar som spåras av [!DNL Google Ads] och [!DNL Microsoft Advertising] i Customer Journey Analytics, uppdateras dagligen

   * Attributionsdata från [!DNL Analytics] i Adobe Advertising, där de kan användas för optimering och rapportering

  I det här fallet bör du ändå [samla in historiska data för AMO ID:n och EF ID:n för användning i Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* (Kommande betafunktion) Annonsörer med Customer Journey Analytics, men inte [!DNL Analytics for Advertising], kan utbyta data mellan Adobe Advertising och Customer Journey Analytics med [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). Du kan spåra webbplatshändelser med hjälp av cookies, hashade IP-adresser och universella ID:n ([!DNL LiveRamp RampIDs] och ID5-ID:n) och attribuera webbplatshändelser till betald mediaaktivitet. Följande data är tillgängliga på kampanj-, annonsgrupp-, paket-, placering- och nyckelordsnivå:

   * Kampanjresultatdata från Adobe Advertising i Customer Journey Analytics

     **Obs!** Data från [!DNL Apple] och [!DNL Tiktok] är inte tillgängliga.

   * Webbplatsaktivitet och konverteringar som spåras av [!DNL Google Ads] och [!DNL Microsoft Advertising] i Customer Journey Analytics

   * Attribueringsdata från Customer Journey Analytics i Adobe Advertising, där de kan användas för optimering och rapportering

  I det här fallet använder du Web SDK för att spåra webbplatshändelser (med cookies, hashed IP-adresser eller universella ID:n) och för att tilldela webbplatshändelser till betald medieaktivitet i [!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Meta] samt Adobe DSP. Du kommer också att använda Adobe Experience Platform för datainsamling.

## Hur man initierar en inbyggd integrering mellan Adobe Advertising och Customer Journey Analytics

Kontakta Adobe Account Team, som kommer att slutföra den initiala konfiguration som krävs för att börja och hjälpa dig att planera implementeringen och dataanvändningen baserat på organisationens behov.

>[!MORELIKETHIS]
>
>* [Förutsättningar](prerequisites.md)
>* (Adobe Analytics-användare) [Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
