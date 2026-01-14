---
title: Om Adobe Advertising Creative
description: Läs mer om  [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Om Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Som en del av Adobe Advertising är Advertising Creative en självbetjäningsplattform för automatisering av personaliserade annonsupplevelser i realtid och optimering av annonser på elementnivå för det kreativa.<!-- Verify --> Du kan implementera annonsupplevelserna som annonser i alla DSP, inklusive Adobe Advertising DSP.

## Egna kreativa bibliotek med återanvändbara kreatörer

Med Creative Libraries kan ni hantera de kreativa verktyg ni kommer att använda i era annonsupplevelser. Du kan skapa flera bibliotek, där var och en innehåller enskilda kreatörer och kreativa grupper (kallas *paket* som du kopplar till upplevelser).

### [!DNL Adobe] resursintegreringar

[!DNL Creative] är direkt integrerat med Adobe Experience Manager, vilket gör att du enkelt kan överföra de [!DNL Adobe] bildresurser som ditt designteam skapar och godkänner för standardbildannonser.

## Både regelbaserade och icke-målinriktade upplevelser

* **Riktade regelbaserade upplevelser:** Bygg upp artiklar med en regelbaserad beslutsträdsmodell - och ta fram en koreografisk sträng med annonser som har anpassats i realtid baserat på vad du vet om målgruppen. Berättelserna kan till exempel ändras utifrån kundbeteende, geografi, demografiska förhållanden, återmarknadsföring, position i kundresan och mycket annat.

* **Icke-målinriktade upplevelser:** Schemalägg och optimera annonselement utan att begränsa målgruppen.

### [!DNL Adobe] dataintegreringar

Du kan använda era egna målgruppssegment från Adobe Audience Manager och Adobe Analytics - samt anpassade målgruppssegment som du skapar i Advertising DSP och återmarknadsföringspixlar som du skapar med [!DNL Creative] - som mål för specifika kreatörer i en annonsupplevelse. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementering av upplevelser som annonser

När du har skapat en upplevelse kan du generera en JavaScript- eller iframe-tagg för upplevelsen och implementera taggen som en tredjepartsannons i en Advertising DSP-kampanj eller i någon annan DSP.

### Optimering av annonselement

Du kan också tillåta att [!DNL Creative] optimerar annonselementen för alla upplevelser baserat på prestanda - oavsett om du definierar specifika målgruppsmål eller inte - med optimerad, viktad annonrotation, som drivs av [!DNL Adobe AI].

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Återmarknadsföring av pixlar

Du kan skapa återmarknadsföringspixlar som ska användas som mål för kreatörer i en annonsupplevelse. Målen visar endast annonser för användare med angivna attribut som tidigare besökt specifika webbsidor.

## Imponera, klicka och konvertera

[!DNL Creative] spårar automatiskt alla visningar och klickningar efter annonser som har skickats från en upplevelse. Du kan också lägga till URL:er för visningsspårning och klickspårning från tredje part till kreatörer i Creative Libraries samt anpassade URL:er för spårning i en upplevelse.

[!DNL Creative] spårar även konverteringar från hanterade annonser som har skapats från dina annonsupplevelser.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Resultatrapportering

Du kan visa detaljerade resultatrapporter på erfarenhetsnivå i Creative > Experiences.

Du kan också skapa anpassade Creative-rapporter på Rapporter > Anpassade rapporter för att övervaka prestandan på upplevelsenivå i alla dina upplevelser. Om du använder dina [!DNL Creative]-upplevelser som annonser inom DSP-kampanjer finns det resultatdata för dessa annonser i ytterligare anpassade rapporter, precis som data för dina andra DSP-annonser. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Du kan också leverera dina anpassade rapporter till angivna [rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md).

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Om dina kreativa bibliotek](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Om upplevelser i Advertising Creative](/help/creative/experiences/experience-about.md)
