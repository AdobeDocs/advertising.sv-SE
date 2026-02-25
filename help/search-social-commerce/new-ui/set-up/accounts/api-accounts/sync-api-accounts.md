---
title: (Nytt användargränssnitt) Synkronisera annonsdata manuellt
description: Lär dig hur du manuellt aktiverar synkronisering av din kampanjstruktur och kampanjentiteter för annonsnätverk som stöds från det nya användargränssnittet.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nytt användargränssnitt) Synkronisera annonsdata manuellt via API-anslutning

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL Microsoft Advertising] (tidigare [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] och befintliga [!DNL Baidu]-konton är endast*

Synkronisering är den process genom vilken Search, Social och Commerce samlar in uppdaterad information för varje annonsörs anslutna annonsnätverkskonton i [annonsnätverk som stöds](/help/search-social-commerce/introduction/supported-inventory.md). Dessa data omfattar annonsörens kampanjstruktur och kampanjentiteter, inklusive de flesta av deras attribut som hanteras eller rapporteras i Sök, Socialt och Commerce. Det omfattar inte klickdata, och inte heller bud och budmodifierare som anges utanför Search, Social och Commerce, som samlas in separat.

Search, Social och Commerce synkroniserar automatiskt (synkroniserar) med annonsnätverkskonton en gång om dagen, och även när det upptäcker en ny kampanj i något av dina annonsnätverk. Dessutom skickas omedelbart alla ändringar av kampanjdata från Search, Social och Commerce till annonsnätverket.

Du kan begära synkronisering manuellt för alla aktiva och pausade kampanjer i angivna konton <!--Not available as of 2/23:  or in specific active and paused campaigns -->. Den här aktiviteten samlar in enheter i annonsnätverket som är nya eller ändrade.

För kampanjer med alternativet [!UICONTROL Auto Update] genererar synkroniseringsåtgärden även spårningskoder som saknas eller behöver ändras i spårningsmallarna eller mål-URL:erna. URL:erna genereras enligt parametrarna i spårningsinställningarna för kontoinställningarna eller kampanjen. Om det finns spårnings-URL:er för de relevanta objekten genereras de inte om de inte behövs (till exempel om nyckelordens matchningstyp, den kreativa texten eller kontots spårningsparametrar har ändrats).

>[!NOTE]
>
>När du [skapar ett kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) kan du synkronisera med annonsnätverket innan kalkylbladet skapas.

## Synkronisera kampanjer i ett annonsnätverkskonto

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Markera kryssrutan bredvid kontonamnet.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Klicka på **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]** i verktygsfältet för gruppåtgärder.

   * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

Du kan följa statusen för synkroniseringsjobbet i vyn [!UICONTROL Workspace]. Jobbet kan ta
en timme eller mer att visa.

>[!MORELIKETHIS]
>
>* [Hämta/skapa en kalkylbladsfil](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
