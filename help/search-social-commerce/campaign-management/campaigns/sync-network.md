---
title: Synkronisera annonsdata manuellt
description: Lär dig hur du manuellt aktiverar synkronisering av din kampanjstruktur och kampanjentiteter för annonsnätverk som stöds.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Synkronisera annonsdata manuellt

*[!DNL Google Ads], [!DNL Microsoft Advertising] (tidigare [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex]och befintlig [!DNL Baidu] endast konton*

Synkronisering är den process genom vilken Search, Social och Commerce samlar in uppdaterad information för varje annonsörs anslutna annonsnätverkskonton på [stödda annonsnätverk](/help/search-social-commerce/introduction/supported-inventory.md). Dessa data omfattar annonsörens kampanjstruktur och kampanjentiteter, inklusive de flesta av deras attribut som hanteras eller rapporteras i Sök, Socialt och Commerce. Det omfattar inte klickdata, och inte heller bud och budmodifierare som anges utanför Search, Social och Commerce, som samlas in separat.

Search, Social och Commerce synkroniserar automatiskt (synkroniserar) med annonsnätverkskonton en gång om dagen, och även när det upptäcker en ny kampanj i något av dina annonsnätverk. Dessutom skickas omedelbart alla ändringar av kampanjdata från Search, Social och Commerce till annonsnätverket.

Du kan begära synkronisering manuellt för alla aktiva och pausade kampanjer i angivna konton eller i specifika aktiva och pausade kampanjer. Den här aktiviteten samlar in enheter i annonsnätverket som är nya eller ändrade.

För kampanjer med[!UICONTROL Auto Upload]&quot; genererar och bokför synkroniseringsåtgärden även spårningskoder som saknas eller behöver ändras i spårningsmallarna eller mål-URL:erna. URL:erna genereras enligt parametrarna i spårningsinställningarna för kontoinställningarna eller kampanjen. Om det finns spårnings-URL:er för de relevanta objekten genereras de inte om de inte behövs (till exempel om nyckelordens matchningstyp, den kreativa texten eller kontots spårningsparametrar har ändrats).

>[!NOTE]
>
>När som helst [skapa ett kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)kan du synkronisera med annonsnätverket innan kalkylbladet skapas.

1. Klicka på **[!UICONTROL Search]>[!UICONTROL Campaigns]**. I undermenyn väljer du antingen **[!UICONTROL Accounts]** för att synkronisera alla kampanjer i specifika konton eller **[!UICONTROL Campaigns]** för att synkronisera specifika kampanjer.

1. (Valfritt) Filtrera listan så att den innehåller specifika konton eller kampanjer.

1. Markera kryssrutan bredvid varje konto eller kampanj som du vill synkronisera. Ni kan synkronisera upp till 50 kampanjer i taget. Om du synkroniserar fler än fem konton åt gången delas jobbet upp i grupper om upp till fem konton.

1. Klicka **![Mer](/help/search-social-commerce/assets/more.png "Mer")** i verktygsfältet och välj **[!UICONTROL Sync]**.

Du kan följa statusen för synkroniseringsjobbet i [!UICONTROL Workspace] vy. Jobbet kan ta en timme eller mer att utföra.

>[!MORELIKETHIS]
>
>* [Hämta/skapa en kalkylbladsfil](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
