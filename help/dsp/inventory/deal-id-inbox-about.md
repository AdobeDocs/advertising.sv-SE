---
title: Om [!UICONTROL Deal ID Inbox]
description: Lär dig mer om funktionen [!UICONTROL Deal ID inbox] som gör att du kan acceptera privata avtal som du redan har förhandlat med utgivare  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (tidigare kallad  [!DNL AdX]), and [!DNL Magnite DV+] (tidigare  [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Om [!UICONTROL Deal ID Inbox]

Med Advertising DSP [!UICONTROL Deal ID inbox] kan du snabbt konfigurera avtal som DSP har importerat från utgivare via SSP (Supply Side Plattforms) så att du inte behöver konfigurera varje avtal manuellt. Du kan acceptera de garanterade och ej garanterade privata lagererbjudanden som du redan har förhandlat med utgivare på [!DNL FreeWheel], [!DNL Google Authorized Buyers] (tidigare kallat [!DNL AdX]) och [!DNL Magnite DV+] (tidigare [!DNL Rubicon]) från [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP är den första DSP som kan integreras med [!DNL FreeWheel]-API:t.

I [!UICONTROL Deal ID inbox] kan du se detaljerna om erbjudandet så som din utgivare ser dem, snabba upp konfigurationen av erbjudandet och undvika manuella inmatningsfel.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP uppdaterar automatiskt alla avtalsdetaljer varje dag kl. 04.30 EST. Den uppdaterar även alla [!DNL FreeWheel] avtal och uppdaterar befintliga avtal från [!DNL Google] och [!DNL Magnite DV+] timmar. Du kan även uppdatera avtalsinformationen manuellt för att fylla i nya avtal när som helst.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>För programmatiska garanterade avtal genom [!DNL Google Authorized Buyers] måste du leverera minst 90 % av din budget, annars förlorar ditt konto åtkomsten till [!DNL Google] avtal i [!UICONTROL Deal ID inbox].

## Implementera [!UICONTROL Deal ID Inbox]

Om du vill få erbjudanden i [!UICONTROL Deal ID inbox] måste dina SSP-konton mappa din organisations DSP-konto till ditt SSP-konto. DSP kan dela organisationens kontonamn med berörda SSP:er. Kontakta kontoteamet på Adobe för instruktioner.

Under avtalsförhandlingar ska du be utgivaren att skicka avtalet till din köpare i stället för till det överordnade DSP-kontot. Avtalsidentifieraren kan vara ett namn eller ett ID, beroende på SSP.

## Åtgärder ni kan vidta

* **Granska avtal** för att verifiera att SSP har skickat rätt utgivare, flygdatum, CPM och annan avtalsinformation. Om utgivaren har gjort ett misstag kontaktar du dem utanför DSP så att de kan korrigera och skicka om avtalet.

* **Acceptera erbjudanden** efter granskning, och de visas inte längre i [!UICONTROL Deal ID inbox]. Godkända erbjudanden listas i [!UICONTROL Inventory] > [!UICONTROL Deals] och är redo att rikta sig till annonsörer.

* **Ignorera erbjudanden** som inte behövs eller som inte har begärts. Ignorerade erbjudanden flyttas till fliken [!UICONTROL Ignored Deals] i [!UICONTROL Deal ID inbox], som fungerar som ett arkiv. DSP varnar inte SSP:er och utgivare när du ignorerar ett avtal.

* **Ändra information för redan accepterade erbjudanden** från [!UICONTROL Inventory] > [!UICONTROL Deals] (inte i [!UICONTROL Deal ID inbox]). När utgivare skickar ändringar till avtal ansvarar annonsörer på liknande sätt för att implementera dessa ändringar i [!UICONTROL Inventory] > [!UICONTROL Deals] eftersom [!UICONTROL Deal ID inbox] inte synkroniserar ändringar från SSP:er efter att avtal har skapats.

## Vilka typer av avtal kan inte accepteras?

Om en avtalslista inte innehåller en ![Acceptera](/help/dsp/assets/accept.png)-ikon eller en [!UICONTROL Accept]-knapp kan du inte acceptera den från [!UICONTROL Deal ID inbox]. I stället kan du [skapa avtals-ID-informationen manuellt](/help/dsp/inventory/deal-id-create.md).

Du kan inte acceptera följande typer av avtal:

* [!DNL Google] erbjudanden som inte är i USD.

* [!DNL Magnite DV+] erbjudanden som inte är i USD

* [!DNL FreeWheel] erbjudanden som inte finns i din kontovaluta.

* Erbjudanden som har ett slutdatum före idag.

* Gammala [!DNL Magnite DV+] avtal som är märkta som &quot;flera medietyper&quot;.

Avtalsdetaljerna innehåller anledningen till att erbjudandet inte är tillgängligt att acceptera.

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Översikt över lagerfunktioner](inventory-overview.md)
