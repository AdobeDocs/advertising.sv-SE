---
title: Skapa och implementera ett CCPA-segment för avanmälan/utförsäljning
description: Lär dig hur du skapar och implementerar ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Skapa och implementera ett CCPA-segment för avanmälan/utförsäljning

Du kan skapa ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar Adobe Advertising samla in en pool med ID:n för annonsörens räkning.

>[!NOTE]
>
>* Information om hur du kan kommunicera CCPA-begäranden om att avanmäla sig från försäljning till Adobe Advertising med hjälp av Adobe Experience Platform Privacy Service API finns i [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=sv-SE](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=sv-SE).
>* Skapa ett [anpassat segment](/help/dsp/audiences/custom-segment-create.md) om du vill spåra användare som besöker webbsidor för syften som inte har att göra med att spåra CCPA-händelser för avanmälan och användare som exponeras för annonser från datorer, mobiler och CTV-enheter.

1. Skapa segmentet:

   1. Klicka på **Publiker > Segment** på huvudmenyn.

   1. Klicka på **[!UICONTROL Create]** ovanför datatabellen.

   1. Ange en unik **[!UICONTROL Segment Name]**.

      Rekommenderat segmentnamn: &quot;&lt;*Advertiser Name*> - CCPA Opt Out of Sale&quot; (till exempel &quot;Acme - CCPA Opt Out of Sale&quot;)

   1. För [!UICONTROL Segment Type] väljer du **[!UICONTROL CCPA Opt-out of sale]**.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera en pixeltagg för att spåra segmentet:

   1. Gå tillbaka till **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Håll markören över det nya segmentet i segmentraden och klicka på **[!UICONTROL Get pixel]**.

   1. Kopiera bildpixeln (med början från `<img src="https://rtd-tm.everesttech.net"`) för att samla in användar-ID för dator- och mobilbesökare till en webbsida.

   1. Ange taggen till annonsören eller webbplatskontakten för distribution med hjälp av den mekanism som företaget använder för att spåra förfrågningar om att avanmäla sig från försäljning (till exempel med hjälp av en plattform för hantering av samtycke).

      Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      När pixeln har implementerats börjar Adobe Advertising samla in en pool med ID:n för annonsörens räkning.

      Även om det är annonsörerna som bestämmer implementering och logik är det här ett exempel på hur en annonsör kan tända ut pixeln:

      1. En konsument hamnar på annonsörens hemsida.
      1. Konsumenten hittar och klickar på annonserarens&quot;CCPA opt out of sales&quot;-knapp.
      1. Konsumenten får en lista över tjänsteleverantörer som annonsören arbetar med.
      1. Konsumenten markerar kryssrutan för att avanmäla sig från att sälja data till Adobe Advertising.

         Den här åtgärden aktiverar pixeln och samlar in konsumentens cookie-ID inom det angivna [!UICONTROL CCPA Opt-out of sale]-segmentet.

>[!MORELIKETHIS]
>
>* [Stöd för Adobe Advertising i Kaliforniens konsumentsekretesslag: Stöd för konsumentavanmälan](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Om [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter ](ccpa-opt-out-about.md)
>* [Hämta rapporter om konsumentens avanmälan från försäljning](ccpa-opt-out-segment-report-retrieve.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Om målgruppshantering](audience-about.md)
