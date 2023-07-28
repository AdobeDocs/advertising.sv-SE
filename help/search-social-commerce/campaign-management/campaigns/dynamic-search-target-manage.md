---
title: Hantera [!DNL Google Ads] dynamiska sökmål
description: Lär dig hur du skapar och hanterar [!DNL Google Ads] dynamiska sökmål.
exl-id: 85b1455a-dda1-4bb9-b4be-d6e0a837fd9d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] dynamiska sökmål

*[!DNL Google Ads]endast konton*

Du kan skapa, redigera och ändra status för dynamiska sökmål för kampanjer som använder söknätverket.

>[!NOTE]
>
>Du kan skapa och redigera stora mängder måldata samtidigt genom att överföra [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) och publicera dem i annonsnätverket.

## Skapa en [!DNL Google Ads] dynamiskt sökmål

Du kan skapa dynamiska sökmål för att definiera sidor på dina webbplatser (dvs. de domäner som används i annonsernas webbadresser) vars innehåll används för att rikta in dina dynamiska sökannonser i samma annonsgrupp.

Du kan ange alla villkor eller upp till tre enskilda villkor som mål.

>[!NOTE]
>
>För bästa spårprestanda skapar du en[!UICONTROL All Targets]&quot; för endast en annonsgrupp per kampanj.

>[!TIP]
>
>Om du vill skapa flera kontokomponenter samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket, kontot, kampanjen och annonsgruppen och klicka sedan på **[!UICONTROL Continue]**.

1. Ange [målinställningar för dynamisk sökning](#dynamic-search-target-settings).

1. Klicka på **[!UICONTROL Post]**.

## Redigera [!DNL Google Ads] målinställningar för dynamisk sökning

Du kan redigera status eller högsta bud för en [!DNL Google Ads] dynamiskt sökmål. Du kan inte ändra de villkor som anges som mål.

>[!TIP]
>
>Om du vill redigera stora mängder data samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Markera kryssrutan bredvid varje rad som ska redigeras.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Ange [målinställningar för dynamisk sökning](#dynamic-search-target-settings).

   För flera mål tillämpas ändringarna på alla valda mål. För [!UICONTROL Bid field]har du möjlighet att ändra befintliga värden till ett angivet värde eller att antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

1. Spara data:

   * (Enstaka mål) Klicka **[!UICONTROL Post]**.

   * (Flera annonsgrupper) Klicka **[!UICONTROL Post Now]**.

## Ändra status för [!DNL Google Ads] dynamiska sökmål

Du kan pausa alla aktiva dynamiska sökmål i en kampanjtyp som stöds om du inte längre vill använda dem för dynamiska sökannonser i samma annonsgrupp. Du kan sedan använda dem som mål genom att ändra annonsstatusen tillbaka till aktiv.

Du kan också ta bort alla dynamiska mål.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika dynamiska mål.

1. Gör något av följande:

   * Om du vill ändra status för ett dynamiskt mål klickar du i dialogrutan **[!UICONTROL Status]** och ändra status.

   * Så här tar du bort ett eller flera dynamiska mål:

      1. Markera kryssrutan bredvid varje dynamiskt mål som du vill ta bort.

     Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ![Mer](/help/search-social-commerce/assets/more.png "Mer") och markera **[!UICONTROL Delete]**.

      1. Klicka på **[!UICONTROL Delete]**.

## [!DNL Google Ads] målinställningar för dynamisk sökning {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Krävs om du inte anger en webbplatsdomän och ett språk i kampanjens [!UICONTROL DSA Options] -sektion; skrivskyddad för befintliga mål) Dynamiska sökmål för annonsgruppen:

* *[!UICONTROL All Targets]* (standard): Alla indexerade sidor anges som mål.

* *\[Särskilda mål\]:* Målar upp till tre villkor för indexerade sidor. När du väljer det här alternativet måste du ange villkoren genom att ange informationskategorier och specifika värden som annonserna ska riktas mot (t.ex.&quot;URL:en innehåller skor.exempel.com&quot;). Om du vill ange fler än ett villkor klickar du på **[!UICONTROL + And]**. Målkriterierna är följande:

   * *[!UICONTROL Category]:* Visa annonser för indexerade sidor med en specifik [!DNL Google Ads] innehållskategori.

   * *[!UICONTROL URL]:* Om du vill visa annonser för indexerade sidor med en viss URL-adress, där värdet kan finnas var som helst i URL-adressen.

   * *[!UICONTROL Page Title]:* Om du vill visa annonser för indexerade sidor med en viss text i sidrubriken.

   * *[!UICONTROL Page Content]:* Visa annonser för indexerade sidor med specifikt innehåll.

**Status:** Status för målinställningarna:

* *[!UICONTROL Active]* (standard): Aktiverar offerter.

* *[!UICONTROL Paused]:* Inaktiverar budgivning.

* *[!UICONTROL Deleted]* (endast befintliga mål): Tar bort målinställningarna.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** Den maximala kostnaden per klick (CPC) för en annons eller kostnad per 1 000 visningar (CPM) för en annons, beroende på modell för annonsnätverk och kampanjpriser. Det här värdet åsidosätter annonsgruppens värde.

>[!NOTE]
>
>Om målet finns i en optimerad portfölj tillämpas det angivna CPC-anbudet för en dag. Därefter lägger optimeringsfunktionen anbud enligt egna beräkningar.

>[!MORELIKETHIS]
>
>* [Om [!DNL Google Ads] dynamiska sökmål](dynamic-search-target-about.md)
