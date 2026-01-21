---
title: Om Adobe Advertising Creative
description: Lär dig mer [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 1394b988828f5400b858f1a40b1b6382431a62b0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Om Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Som en del av Adobe Advertising Advertising är Advertising Creative en självbetjäningsplattform för att automatisera realtids, personliga annonsupplevelser och eventuellt optimera dina annonser på kreativ elementnivå.<!-- Verify --> Du kan implementera annonsupplevelser som annonser i vilken DSP som helst, inklusive Adobe Advertising DSP.

## Anpassade kreativa bibliotek med återanvändbara kreatörer

Dina Creative Libraries låter dig hantera de kreativa material du kommer att använda i dina annonsupplevelser. Du kan skapa flera bibliotek, var och en med individuella kreatörer och kreativa grupper (kallade *paket,* som du kopplar till upplevelser).

### [!DNL Adobe] Tillgångsintegrationer

[!DNL Creative] är direkt integrerad med följande [!DNL Adobe] produkter, vilket gör det möjligt att importera tillgångar till dina kreativa bibliotek:

* **Adobe Experience Manager:** Ladda upp de [!DNL Adobe] bildresurser som ditt designteam skapar och godkänner för standardbildannonser.

* **Adobe GenStudio för Performance Marketing:** Importera alla annonsvarianter från dina displayannonsupplevelser som HTML5-kreatörer.

## Både regelbaserade och icke-riktade upplevelser

* **Riktade, regelbaserade upplevelser:** Bygg ut berättelser med en regelbaserad beslutsträdsmodell – och veckla ut en koreograferad rad annonser som anpassas i realtid baserat på vad du vet om din publik. Till exempel kan berättelserna förändras beroende på kundbeteende, geografi, demografi, ommålning, position i kundresan och mer.

* **Icke-riktade upplevelser:** Schemalägg och optimera annonselement utan att begränsa publiken.

### [!DNL Adobe] Dataintegrationer

Använd dina förstaparts-målgruppssegment från Adobe Audience Manager och Adobe Analytics – samt anpassade målgruppssegment du skapar i Advertising DSP och retargeting av pixlar du skapar med [!DNL Creative] – som mål för specifika kreatörer i en annonsupplevelse. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementering av upplevelser som annonser

När du har skapat en upplevelse kan du generera en JavaScript- eller iframe-tagg för upplevelsen och implementera taggen som en tredjepartsannons i en Advertising DSP-kampanj eller i någon annan DSP.

### Optimering av annonselement

Du kan valfritt tillåta [!DNL Creative] att optimera annonselementen för vilken upplevelse som helst baserat på prestation – oavsett om du definierar specifika målgrupper eller inte – med optimerad, viktad annonsrotation, som drivs av [!DNL Adobe AI].

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Ommålning av pixlar

Du kan skapa retargeting-pixlar att använda som mål för kreativa material inom en annonsupplevelse. Målen visar annonser endast till användare med angivna attribut som tidigare besökt specifika webbsidor.

## Visning, klick och konverteringsspårning

[!DNL Creative] Spårar automatiskt alla visningar och klick för annonser som visas från en upplevelse. Du kan också valfritt lägga till tredjeparts visningsspårning och klickspårnings-URL:er till kreativa filer i Creative Libraries, samt anpassade spårnings-URL:er i en upplevelse.

[!DNL Creative] Spårar också konverteringar från visade annonser skapade från dina annonsupplevelser.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Prestationsrapportering

Du kan se detaljerade prestationsrapporter på erfarenhetsnivå inom Creatives > Experiences.

Du kan också skapa anpassade kreativa rapporter på Reports > Custom Reports för att övervaka upplevelsenivåns prestation över dina upplevelser. Om du använder dina [!DNL Creative] upplevelser som annonser inom DSP-kampanjer finns prestandadata för dessa annonser tillgängliga i ytterligare anpassade rapporter, precis som data för dina andra DSP-annonser. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Du kan valfritt leverera dina anpassade rapporter till angivna [rapportdestinationer](/help/dsp/reports/report-destinations/report-destination-about.md).

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Om dina kreativa bibliotek](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Om erfarenheter inom reklamkreativt](/help/creative/experiences/experience-about.md)
