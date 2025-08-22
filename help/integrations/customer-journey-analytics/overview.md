---
title: Översikt över integrationen mellan Adobe Advertising och Adobe Customer Journey Analytics
description: Läs om hur du kan integrera Adobe Advertising med Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: ed3c3b4331b743d0c40f04fb8543c535d80ca1d5
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Översikt över integrationen mellan Adobe Advertising och Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Annonsörer med Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising är integrerat med Adobe Customer Journey Analytics för dubbelriktad datadelning. Det finns två alternativ för att konfigurera integreringen:

* Annonsörer med både [!DNL Analytics for Advertising] och Customer Journey Analytics har samma funktioner som de har via [!DNL Analytics for Advertising], med tillägg av visualiseringar i Customer Journey Analytics.

  Du kan fortfarande spåra klickningshändelser med Adobe Experience Platform Web SDK (`alloy.js`) eller Adobe Experience Cloud Identity Service (`visitorAPI.js`). Annonsörer med Advertising DSP kommer fortfarande att använda ett JavaScript-kodfragment för att spåra visningshändelser. Data som finns i Customer Journey Analytics inkluderar:

   * Kampanjresultatdata från Adobe Advertising

     **Obs!** Data från [!DNL Apple] och [!DNL Tiktok] är inte tillgängliga.

   * Webbplatsaktivitet och konverteringar som spåras av [!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Meta]

   * Attributdata från [!DNL Analytics], som kan användas för optimering och rapportering i Adobe Advertising

  I det här fallet behöver du inte utföra några extra steg förutom att [samla in historiska data för AMO ID:n och EF ID:n som kan användas i Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

* (Kommande betafunktion) Annonsörer med Customer Journey Analytics, men inte [!DNL Analytics for Advertising], kan utbyta följande data mellan Adobe Advertising och Customer Journey Analytics genom att spåra klicknings- och genomsiktshändelser med Adobe Experience Platform Web SDK (`alloy.js`). Data finns på kampanj-, annonsgrupp-, paket-, placering- och nyckelordsnivå.

   * Kampanjresultatdata från Adobe Advertising

     **Obs!** Data från [!DNL Apple] och [!DNL Tiktok] är inte tillgängliga.

   * Webbplatsaktivitet och konverteringar som spåras av [!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Meta]

   * Attribueringsdata från Customer Journey Analytics, som kan användas för optimering och rapportering i Adobe Advertising

  **Obs!** Inga organiska data är tillgängliga än.<!-- Does that belong somewhere up above? -->

  I det här fallet använder du Web SDK för att spåra webbplatshändelser (med cookies, hashed IP-adresser eller universella ID:n) och för att tilldela webbplatshändelser till betald medieaktivitet i [!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Meta] samt Adobe DSP. Du kommer också att använda Adobe Experience Platform för datainsamling.

## Hur man initierar en inbyggd integrering mellan Adobe Advertising och Customer Journey Analytics

Kontakta Adobe Account Team, som kommer att slutföra den initiala konfiguration som krävs för att börja och hjälpa dig att planera implementeringen och dataanvändningen baserat på organisationens behov.

>[!MORELIKETHIS]
>
>* [Förutsättningar](prerequisites.md)
>* (Adobe Analytics-användare) [Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
