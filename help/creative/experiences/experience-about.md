---
title: Om upplevelser i Advertising Creative
description: Lär dig hur du konfigurerar personaliserade annonsupplevelser och optimerar annonselement baserat på prestanda.
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Om upplevelser i Advertising Creative 2.0

*Stängd beta*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] innehåller två olika annonsupplevelsestrukturer för annonser i det kreativa biblioteket <!-- can use a single library only -->:

* **Erfarenheter med målgruppsanpassning i beslutsträd:** [!DNL Creative] gör att du kan konfigurera personaliserade annonsupplevelser under hela kundresan med hjälp av en beslutsträdsmodell. Ni kan anpassa alla annonselement - bilder, rubriker, erbjudanden och landningssidor - baserat på målgruppen.

  Du kan till exempel ange samma paket för personer i Chicago och New York City som befinner sig i ett visst Adobe Analytics-målgruppssegment, men skicka personer i Chicago som befinner sig i samma segment till andra landningssidor än New Yorkers. Du kan också ange ett annat paket för personer i segmentet som bor var som helst, förutom Chicago och New York, och ett tredje paket för andra personer som inte är med i segmentet.

  Bland målgruppsalternativen finns tittare i era egna målgruppssegment från Adobe Audience Manager, Adobe Analytics och Advertising Cloud DSP, tittare i specifika geografiska områden, inklusive länder, delstater, DMA:er i USA, städer och postnummer, visningsprogram för vilka specifika nyckelvärdepar (datpass-mål) skickas från DSP, utgivare eller partner, visningsprogram med [!DNL Creative] omdirigerade pixlar och angivna attributvärden samt visningsprogram med specifika enhetstyper , operativsystem och webbläsare.

  Du kan tilldela kreativa paket till varje upplevelse, alternativt anpassa optimering och schemaläggning för de kreativa paketen och ändra standardstartsidorna och spårnings-URL:er <!-- and any flexible attributes --> för enskilda kreatörer i varje paket.

* **Upplevelser utan mål för beslutsträd:** [!DNL Creative] optimerar annonselementen för annonsupplevelsen utan att begränsa målgruppen.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Du anger start- och slutdatum och vissa standardinställningar för varje upplevelse, men mycket av arbetsflödet är inte direkt inom upplevelsen. I stället för att lägga till kreatörer direkt i upplevelsen skapar du en annonstagg för varje annonsstorlek för upplevelsen och lägger sedan till kreatörer i den, konfigurerar kreativ optimering och schemaläggning samt anpassar landningssidor och spårnings-URL:er från [!UICONTROL Tag Manager].

## Annonsoptimering

<!-- MORE -->
[!DNL Creative] optimerar annonselementen för alla upplevelser baserat på prestanda. För upplevelser som riktar sig till specifika målgrupper kan annonserna optimeras baserat på resultatet för de enskilda annonselementen för målgrupperna. För upplevelser utan specifika målgruppsmål optimeras annonselementen enbart utifrån de enskilda annonselementens prestanda.

## Implementera och hantera upplevelser

När du har skapat en liveupplevelse (med alla nödvändiga annonselement) kan du [generera en JavaScript- eller iframe-tagg för hela upplevelsen](experience-tag-export.md), som du kan överföra som en annons till en kampanj i Adobe Advertising DSP eller implementera som en annons i en DSP från tredje part. [!DNL Creative] visar annonser för upplevelsen baserat på målgrupps- och annonsrotationsalternativen samt tillgängligt annonsmaterial.

## Prestandadata för era upplevelser

När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått.

![Metrisk, alternativ](/help/creative/assets/metrics-option.png "Metrisk, alternativ")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Du kan visa detaljerade prestandadata för alla upplevelser från vyn [!UICONTROL Creative] > [!UICONTROL Experiences]. Om du vill övervaka prestanda för alla dina upplevelser skapar du en [!UICONTROL Custom Creative Report].

<!--
You can [view detailed performance data for any experience](experience-view-report.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## Upplevelsestatus {#experience-statuses}

<!-- verify that these are all still the same -->

Status för en upplevelse anges automatiskt, förutom för *removed* som du anger manuellt.

*Live:* Upplevelsen innehåller alla nödvändiga element, så du kan generera en upplevelsetagg som ska implementeras som en annons i en DSP. <!-- A live experience may be scheduled to start in the future -->

*Utkast:* Alla grenar av upplevelsen har inte tilldelats några kreativa funktioner, så upplevelsen är ofullständig och du kan inte generera någon upplevelsetagg.

*Bearbetning:* En tidigare aktiv upplevelse har redigerats, men är nu ofullständig. Du kan inte generera en upplevelsetagg för den. **Obs!** Om du redan har implementerat en upplevelsetagg för upplevelsen kommer den tidigare versionen fortfarande att hanteras. Om du senare slutför upplevelsen - så att den blir offentlig igen - kommer den nya versionen att hanteras med den befintliga taggimplementeringen.

*Borttagen:* Upplevelsen har tagits bort från [!DNL Creative] och är inte längre synlig i [!UICONTROL Experiences]-vyerna.

>[!NOTE]
>
>Du kan ändra status för en annons i en DSP utan att påverka upplevelsestatusen i [!DNL Creative].

## Vyn [!UICONTROL Experiences]

Vyn [!UICONTROL Experiences] visar alla dina målinriktade och icke-målinriktade upplevelser. Du kan se upplevelsenamn, status, start- och slutdatum, antal och dimensioner för de tilldelade kreativa eller kreativa paketen samt om upplevelsen omfattar dynamiska annonser. När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått.

Ni kan skapa och hantera era upplevelser, inklusive optimering och tilldela kreativa upplevelser och kreativa paket till era upplevelser. Du kan också skapa och byta namn på märkord och exportera märkorden i JavaScript- och iframe-format för implementering i DSP. Annonsörer med Advertising DSP kan ladda upp taggar direkt till en Advertising DSP-kampanj som reklam.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Skapa en upplevelse utan mål](experience-create-no-targeting.md)
