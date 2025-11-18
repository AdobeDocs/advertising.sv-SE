---
title: Om upplevelser i Advertising Creative
description: Lär dig hur du konfigurerar personaliserade annonsupplevelser och optimerar annonselement baserat på prestanda.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 9f54812a555032a7184e8a4b0dbf69ce00a32d2c
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# Om upplevelser i Advertising Creative 2.0

Varje annonsupplevelse kan innehålla en annonstyp (standardskärm, standardvideo eller dynamisk visning). [!DNL Advertising Creative 2.0] innehåller två olika annonsupplevelsestrukturer för annonserna i ett enda kreativt bibliotek.

* **Erfarenheter med målgruppsanpassning i beslutsträd:** [!DNL Creative] gör att du kan konfigurera personaliserade annonsupplevelser under hela kundresan med hjälp av en beslutsträdsmodell. Ni kan anpassa alla annonselement - bilder, rubriker, erbjudanden och landningssidor - baserat på målgruppen.

  Du kan till exempel ange samma paket för personer i Chicago och New York City som befinner sig i ett visst Adobe Analytics-målgruppssegment, men skickar personer i Chicago till andra landningssidor än New Yorkers. Du kan också ange ett annat paket för personer i segmentet som bor var som helst, förutom Chicago och New York, och ett tredje paket för andra personer som inte är med i segmentet.

  Målalternativen är:

   * Era målgruppssegment från Adobe Audience Manager, Adobe Analytics och Advertising DSP, alla andra kundsegment som importerats för kontot, era egna segment från Advertising DSP, tredjepartssegment från Advertising DSP samt alla befintliga Advertising DSP-målgrupper som skapats i Audience Library

   * Specifika geografiska platser, inklusive länder, delstater, DMA:er i USA, städer och postnummer

   * Visare som specifika nyckelvärdepar (mål för dataöverföring) skickas från DSP, utgivaren eller partnern (t.ex. SKU=01234567890123 eller Cart=empty)

   * [!DNL Creative] omdirigerade pixlar och angivna attributvärden

   * Specifika enhetstyper, operativsystem och webbläsare

  När ni väl har skapat en målgruppsgren i beslutsträdet kan ni koppla målgruppen till potentiella kreatörer genom att tilldela grenen kreativa paket. För varje upplevelse kan du anpassa optimering och schemaläggning för de kreativa paketen och ändra standardstartsidorna och spårnings-URL:er <!-- later: and any flexible attributes --> för enskilda kreatörer i varje paket.

* **Upplevelser utan mål för beslutsträd:** [!DNL Creative] optimerar annonselementen för annonsupplevelsen utan att begränsa målgruppen. För varje upplevelse anger du start- och slutdatum och vissa standardinställningar, men mycket av arbetsflödet ligger inte direkt i upplevelsen. I stället för att lägga till kreatörer direkt i upplevelsen kan du använda [!UICONTROL Tag Manager] för att skapa en annonstagg för varje annonsstorlek för upplevelsen och sedan lägga till kreatörer i den, konfigurera kreativ optimering och schemaläggning samt anpassa landningssidorna och spårnings-URL:er<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Eftersom de två typerna av upplevelser har olika arbetsflöden kan ni inte ändra en icke-riktad upplevelse till en målinriktad upplevelse eller en målinriktad upplevelse till en upplevelse som inte är målinriktad.

## Annonsvisning och optimering

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] visar annonser från första part och utlöser tredjepartsannonser för upplevelsen baserat på den angivna målsättningen (när det är tillämpligt), schemaläggning, annonsrotation och optimeringsmålalternativen samt tillgängligt annonsmaterial.

* **Schemaläggning:** (valfritt) Schemalägg specifika kreatörer som ska köras under angivna sekventiella tidsperioder.

* **Annonsrotation:** Rotera kreatörerna algoritmiskt enligt det angivna optimeringsmålet, enligt en angiven paketsekvens eller enligt relativa vikter.

* **Optimeringsmål:** Optimera annonselement för antingen den bästa klickfrekvensen eller ett befintligt [Advertising DSP-anpassat mål](/help/dsp/optimization/custom-goal.md)

  [!DNL Creative] optimerar annonsupplevelserna genom att ge intryck av att dela med de resurser som presterar bäst i upplevelsen. För upplevelser som riktar sig till specifika målgrupper kan annonserna optimeras baserat på resultatet för de enskilda annonselementen för målgrupperna. För upplevelser utan specifika målgruppsmål optimeras annonselementen enbart utifrån de enskilda annonselementens prestanda.

Du kan till exempel schemalägga att Creative 1 ska köras under de första två veckorna för att optimera klickfrekvensen och att Creative 2 ska köras under de följande två veckorna för att optimera för ett visst anpassat mål.

## Implementera och hantera upplevelser

När du har skapat en liveupplevelse (med alla nödvändiga annonselement) kan du [generera en JavaScript- eller iframe-tagg för hela upplevelsen](experience-tag-export.md). Du kan överföra upplevelsetaggen som en annons till en kampanj i Adobe Advertising DSP eller implementera den som en annons i en DSP från tredje part.

>[!NOTE]
>
>Hierarkisk målinriktning kan variera beroende på DSP. Advertising DSP lägger in målgruppsanpassning på annonsnivå ovanpå målinriktning på placeringsnivå.

## Prestandadata för era upplevelser

Följande prestandadata är tillgängliga:

* När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Creative] > [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått.

  ![Metrisk, alternativ](/help/creative/assets/metrics-option.png "Metrisk, alternativ")

* Du kan [visa detaljerade prestandadata för alla upplevelser](experience-performance-details.md) från vyn [!UICONTROL Experiences].

* Skapa en [anpassad Creative-rapport](/help/creative/reports/report-manage.md) om du vill övervaka prestanda för alla dina upplevelser.

## Upplevelsestatus {#experience-statuses}

Status för en upplevelse anges automatiskt, förutom för *Borttagen* som du anger manuellt.

| Status | Beskrivning |
| ------ | ----------- |
| [!UICONTROL Live] | Upplevelsen innehåller alla nödvändiga element, så att du kan generera en upplevelsetagg som ska implementeras som en annons i en DSP. En liveupplevelse kan planeras att starta i framtiden. |
| [!UICONTROL Draft] | Alla avdelningar i upplevelsen är inte tilldelade till kreatörer, så upplevelsen är ofullständig och du kan inte generera någon upplevelsetagg. |
| [!UICONTROL Processing] | En tidigare liveupplevelse redigerades men är nu ofullständig. Du kan inte generera en upplevelsetagg för den. **Obs!** Om du redan har implementerat en upplevelsetagg för upplevelsen kan den tidigare versionen fortfarande hanteras. Om du senare slutför upplevelsen - så att den blir offentlig igen - kan den nya versionen hanteras med den befintliga taggimplementeringen. |
| [!UICONTROL Deleted] | Upplevelsen togs bort från [!DNL Creative] och är inte längre synlig i [!UICONTROL Experiences]-vyerna. |

>[!NOTE]
>
>Du kan ändra status för en annons inom en DSP utan att påverka upplevelsestatusen i [!DNL Creative].

## Vyn [!UICONTROL Experiences]

Vyn [!UICONTROL Experiences] visar alla dina målinriktade och icke-målinriktade upplevelser. Du kan se upplevelsenamn, status, start- och slutdatum, antal och dimensioner för de tilldelade kreativa eller kreativa paketen samt om upplevelsen omfattar dynamiska annonser. När du aktiverar alternativet [!UICONTROL Metrics] i vyn [!UICONTROL Experiences] visar varje upplevelsekort eller rad antalet visningar och klick som upplevelsen har fått. När du är i kortläge kan du bläddra bland kreatörerna i en upplevelse med flera kreatörer genom att använda knapparna &lt; och >.

Ni kan skapa och hantera era upplevelser, skapa och byta namn på annonsupplevelsetaggar och exportera taggarna i JavaScript- och iframe-format för implementering i era DSP:er. Annonsörer med Advertising DSP kan ladda upp annonstaggar direkt till en Advertising DSP-kampanj.

### Tillgängliga åtgärder

Följande är viktiga åtgärder som är tillgängliga. En fullständig lista finns i innehållsförteckningen för kapitlet Creative > Experiences.

* [Hämta data från vyn](experience-download-view.md)

* [Skapa](/help/creative/experiences/experience-create-targeting.md) och [redigera](/help/creative/experiences/experience-edit-targeting.md) en upplevelse med målinriktning

* [Skapa](/help/creative/experiences/experience-create-no-targeting.md), [redigera](/help/creative/experiences/experience-edit-no-targeting.md) och [skapa en annonstagg](/help/creative/experiences/experience-tag-create-manually.md) manuellt för en upplevelse utan målinriktning

* [Klona](experience-clone.md) en upplevelse

* [Förhandsgranska](experience-preview.md) en upplevelse

* [Dela en demo-URL](experience-share-demo-url.md) för en upplevelse

* [Exportera annonstaggar för en upplevelse](experience-tag-export.md), inklusive möjlighet att överföra annonstaggar direkt till en Advertising DSP-kampanj

* [Ta bort](experience-delete.md) en upplevelse

>[!MORELIKETHIS]
>
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Skapa en upplevelse utan mål](experience-create-no-targeting.md)
