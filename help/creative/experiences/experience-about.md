---
title: Om upplevelser i Advertising Creative
description: Lär dig hur du konfigurerar personaliserade annonsupplevelser och optimerar annonselement baserat på prestanda.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 0a6cd8e32ae87c7fda9ed0e1b50f9b54cd337192
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Om upplevelser i Advertising Creative 2.0

*Stängd beta*

<!-- Revisit Description metadata  -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] innehåller två olika annonsupplevelsestrukturer för annonserna i ett kreativt bibliotek <!-- can use a single library only -->:

* **Erfarenheter med målgruppsanpassning i beslutsträd:** [!DNL Creative] gör att du kan konfigurera personaliserade annonsupplevelser under hela kundresan med hjälp av en beslutsträdsmodell. Ni kan anpassa alla annonselement - bilder, rubriker, erbjudanden och landningssidor - baserat på målgruppen.

  Du kan till exempel ange samma paket för personer i Chicago och New York City som befinner sig i ett visst Adobe Analytics-målgruppssegment, men skickar personer i Chicago till andra landningssidor än New Yorkers. Du kan också ange ett annat paket för personer i segmentet som bor var som helst, förutom Chicago och New York, och ett tredje paket för andra personer som inte är med i segmentet.

  Målalternativen är:

   * Era första målgruppssegment från Adobe Audience Manager, Adobe Analytics och Advertising Cloud DSP

   * Specifika geografiska platser, inklusive länder, delstater, DMA:er i USA, städer och postnummer

   * Visare som specifika nyckelvärdepar (mål för dataöverföring) skickas från DSP, utgivaren eller partnern

   * [!DNL Creative] omdirigerade pixlar och angivna attributvärden

   * Specifika enhetstyper, operativsystem och webbläsare

  Ni kan tilldela kreativa paket till varje upplevelse. För varje upplevelse kan du anpassa optimering och schemaläggning för de kreativa paketen och ändra standardstartsidorna och spårnings-URL:er <!-- and any flexible attributes --> för enskilda kreatörer i varje paket.

* **Upplevelser utan mål för beslutsträd:** [!DNL Creative] optimerar annonselementen för annonsupplevelsen utan att begränsa målgruppen.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> För varje upplevelse anger du start- och slutdatum och vissa standardinställningar, men mycket av arbetsflödet är inte direkt inom upplevelsen. I stället för att lägga till kreatörer direkt i upplevelsen använder du [!UICONTROL Tag Manager] för att skapa en annonstagg för varje annonsstorlek för upplevelsen och sedan lägga till kreatörer i den, konfigurera kreativ optimering och schemaläggning samt anpassa landningssidorna och spårnings-URL:er.

## Annonsoptimering

<!-- MORE -->
[!DNL Creative] optimerar annonselementen för alla upplevelser baserat på prestanda. För upplevelser som riktar sig till specifika målgrupper kan annonserna optimeras baserat på resultatet för de enskilda annonselementen för målgrupperna. För upplevelser utan specifika målgruppsmål optimeras annonselementen enbart utifrån de enskilda annonselementens prestanda.

## Implementera och hantera upplevelser

När du har skapat en liveupplevelse (med alla nödvändiga annonselement) kan du [generera en JavaScript- eller iframe-tagg för hela upplevelsen](experience-tag-export.md). Du kan överföra upplevelsetaggen som en annons till en kampanj i Adobe Advertising DSP eller implementera den som en annons i en DSP från tredje part. [!DNL Creative] visar annonser för upplevelsen baserat på målgrupps- och annonsrotationsalternativen samt tillgängligt annonsmaterial.

## Prestandadata för era upplevelser

När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Creative] > [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått.

![Metrisk, alternativ](/help/creative/assets/metrics-option.png "Metrisk, alternativ")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Du kan [visa detaljerade prestandadata för alla upplevelser](experience-performance-details.md) från vyn [!UICONTROL Experiences].

Skapa en [anpassad Creative-rapport](/help/creative/report-custom-creative.md) om du vill övervaka prestanda för alla dina upplevelser.

## Upplevelsestatus {#experience-statuses}

<!-- verify that these are all still the same -->

Status för en upplevelse anges automatiskt, förutom för *removed* som du anger manuellt.

*Live:* Upplevelsen innehåller alla nödvändiga element, så att du kan generera en upplevelsetagg som ska implementeras som en annons i en DSP. <!-- A live experience may be scheduled to start in the future -->

*Utkast:* Alla grenar av upplevelsen har inte tilldelats några kreativa funktioner, så upplevelsen är ofullständig och du kan inte generera någon upplevelsetagg.

*Bearbetning:* En tidigare aktiv upplevelse har redigerats, men är nu ofullständig. Du kan inte generera en upplevelsetagg för den. **Obs!** Om du redan har implementerat en upplevelsetagg för upplevelsen kan den tidigare versionen fortfarande hanteras. Om du senare slutför upplevelsen - så att den blir offentlig igen - kan den nya versionen hanteras med den befintliga taggimplementeringen.

*Borttagen:* Upplevelsen har tagits bort från [!DNL Creative] och är inte längre synlig i [!UICONTROL Experiences]-vyerna.

>[!NOTE]
>
>Du kan ändra status för en annons inom en DSP utan att påverka upplevelsestatusen i [!DNL Creative].

## Vyn [!UICONTROL Experiences]

Vyn [!UICONTROL Experiences] visar alla dina målinriktade och icke-målinriktade upplevelser. Du kan se upplevelsenamn, status, start- och slutdatum, antal och dimensioner för de tilldelade kreativa eller kreativa paketen samt om upplevelsen omfattar dynamiska annonser. När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått.

Ni kan skapa och hantera era upplevelser, inklusive optimering och tilldela kreativa upplevelser och kreativa paket till era upplevelser. Du kan också skapa och byta namn på märkord och exportera märkorden i JavaScript- och iframe-format för implementering i DSP:er. Annonsörer med Advertising DSP kan ladda upp taggar direkt till en Advertising DSP-kampanj som reklam.

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
