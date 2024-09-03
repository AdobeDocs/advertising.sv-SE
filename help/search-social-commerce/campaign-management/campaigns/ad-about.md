---
title: Hantera annonser
description: Läs mer om annonser i Search, Social och Commerce, inklusive tillgängliga annonstyper.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Om annonser

Endast *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] och befintliga [!DNL Baidu]-konton*

En annons kan visas på en målwebbplats (för innehåll eller placeringsriktade kampanjer), när en användare söker efter något av nyckelorden i annonsgruppen (för sökkampanjer) eller för innehåll på din webbplats (dynamiska sökannonser i [!DNL Google Ads] sökkampanjer) eller när en användare utför en sökning som är relevant för något av objekten i din [!DNL Google Merchant Center] eller [!DNL Microsoft Merchant Center] produktfeed (shoppingannonser i [!DNL Google Ads] eller produktannonser i [!DNL Microsoft Advertising]  kampanjer).

## Tillgängliga annonstyper

Du kan skapa och hantera annonstyper som stöds för annonsgrupper i ett synkroniserat annonsnätverkskonto:

* **Textannonser eller utökade textannonser** för en annonsgrupp i en kampanj som riktar sig till söknätverket. Textannonser kan innehålla valfria spårningsparametrar som åsidosätter parametrarna på annonsgrupps- eller kampanjnivå. Beroende på annonsnätverket kan du skapa antingen utökade/utökade textannonser eller standardtextannonser.

* Enhetsoberoende, inbyggda **målgruppsannonser** för [!DNL Microsoft Advertising] kampanjer på [!DNL Microsoft Audience Network]. Du har två alternativ för målgruppsannonser, baserat på kampanjinställningarna:

   * Om kampanjen är länkad till en handlares centerbutik kan annonsnätverket automatiskt generera annonser som är baserade på kampanjen, med hjälp av butikens produktinformation. Ni behöver inte skapa flödesbaserade annonser för kampanjen, men ni måste skapa annonsgrupper med målinriktning mot användarna.

   * Om kampanjen inte är länkad till ett handlarcenterkonto skapar du bildbaserade målgruppsannonser med det responsiva annonsformatet, som inkluderar flera text- och bildresurser. Annonsnätverket sätter ihop annonserna med de mest effektiva kombinationerna av annonselement och visar dem på webbplatser som [!DNL MSN], [!DNL Outlook.com] och [!DNL Microsoft Edge].

* **Annonser som bara är tillgängliga för samtal** för [!DNL Google Ads] kampanjer i söknätverket. Annonser som bara kan ringa är textannonser som innehåller ett telefonnummer. Du kan också använda ett [!DNL Google Ads]-tilldelat vidarebefordringsnummer för avancerad samtalsrapportering.

* **Utökade dynamiska sökannonser** (kallas nu bara&quot;dynamiska sökannonser&quot; i annonsnätverken) för [!DNL Google Ads] och [!DNL Microsoft Advertising] dynamiska sökannonseringsgrupper i sökkampanjer. Dynamiska sökannonser använder innehåll från er webbplats, i stället för nyckelord, för att bestämma när era annonser ska visas. Annonsnätverket genererar rubriken dynamiskt, väljer landningssidans URL och visar URL och genererar automatiskt den slutliga URL:en.

  Du kan definiera sidorna på dina webbplatser vars innehåll används för att rikta in dina dynamiska sökannonser genom att ange specifika dynamiska sökmål för annonsgruppen. För [!DNL Google Ads] kan du skapa dynamiska sökmål i Sök, Socialt och Commerce. För [!DNL Microsoft Advertising] måste du skapa dem i [!DNL Microsoft Advertising]. I [!DNL Google Ads] kampanjer kan du välja att ange en webbplatsdomän och ett språk i kampanjens [!DNL DSA Options]-avsnitt i stället för, eller utöver, att skapa dynamiska sökmål.

  När en användares sökord exakt matchar ett nyckelord i en av dina nyckelordsbaserade kampanjer visas en annons från den nyckelordsbaserade kampanjen i stället för en dynamisk sökannons. Annonsnätverket visar en dynamisk sökannons i stället för en nyckelordsriktad annons när användarens sökord är en bred matchning eller frasmatchning med något av dina nyckelord och din dynamiska sökannons har en högre annonsrankning.

  Mer information om annonser för dynamiska sökningar finns i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/2471185) och [[!DNL Microsoft Advertising] dokumentationen](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimediaannonser** för [!DNL Microsoft Advertising] sökkampanjer. Multimediaannonser är stora bildannonser som visas på framträdande huvudlinje- och sidofältspositioner, och endast en multimediaannons visas per sida. De kan innehålla flera text- och bildresurser, som responsiva annonser, och annonsnätverket sätter ihop annonserna med de mest effektiva kombinationerna av annonselement. Multimediaannonser ersätter inte er text och era placeringar.

* Kampanjrader för **[!DNL Microsoft Advertising]produktannonser (shoppingannonser)** i köpnätverket. Shoppingannonser använder produkter i din befintliga [!DNL Microsoft Merchant Center]-produktfeed, i stället för nyckelord, för att bestämma hur och var annonserna ska visas. Webbadresserna för annonskopior och landningssidor genereras automatiskt från din produktinformation i flödet, men du kan också konfigurera kampanjrader som ska inkluderas för annonsgruppen.

  Du kan styra vilka produkter som visas med dina [!DNL Microsoft Advertising]-shoppingannonser genom att ställa in separata produktgrupper för annonsgruppen i vyn [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

  Mer information om arbetsflödet för produkt-/shoppingannonser finns i [Implementera [!DNL Microsoft Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md).  Mer information om produktannonser finns i [dokumentationen för Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsiva sökannonser för [!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer i söknätverket. Annonsnätverket sätter dynamiskt ihop textbaserade responsiva sökannonser från en uppsättning annonsrubriker och beskrivningar, vilket gynnar kombinationer som fungerar bra ihop. Annonsen innehåller upp till tre rubriker, två beskrivningar och en anpassningsbar URL från bas-URL:en och valfria sökvägsfält1 och sökvägsfält2. Du kan även fästa annonsrubriker och beskrivningar på specifika positioner.

>[!NOTE]
>
>[!DNL Google Ads] tillhandahåller inte data utanför sina interna redigerare om de textkombinationer som visades som annonser. Mer information om rapportering för varje textkombination finns i [dokumentationen för Google Ads](https://support.google.com/google-ads/answer/7684791).

## Vyn [!UICONTROL Ads]

Du kan skapa, redigera och ändra status för annonser i vyn [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads].

## Prestandadata på annonsnivå

Data på annonsnivå är tillgängliga för de flesta annonstyper.

Den är dock inte tillgänglig för [!DNL Google Ads] dynamisk sökannons (DSA), prestandamängd, smart shopping och [!DNL YouTube] kampanjer. Förvänta diskrepanser mellan den totala annonsnivån för en kampanj och kampanjens totala data.

| Annonsnätverk/kampanj/annonstyp | Datatillgång |
|---|---|
| [!DNL Google Ads] dynamisk sökannons (DSA) | Campaign, annonsgrupp |
| Högsta prestanda för [!DNL Google Ads] | Campaign |
| [!DNL Google Ads] handla, smart shopping | Campaign, annonsgrupp |
| [!DNL Google Ads] [!DNL YouTube] | Campaign, annonsgrupp |

>[!MORELIKETHIS]
>
>* [Hantera annonser](ad-manage.md)
