---
title: Hantera  [!DNL Google Ads] dynamiska sökmål
description: Lär dig hur du skapar och hanterar  [!DNL Google Ads] dynamiska sökmål.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] dynamiska sökmål

Endast *[!DNL Google Ads]konton*

Du kan skapa, redigera och ändra status för dynamiska sökmål för kampanjer som använder söknätverket.

>[!NOTE]
>
>Du kan skapa och redigera stora mängder måldata på en gång genom att överföra [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) och publicera dem i annonsnätverket.

## Skapa ett [!DNL Google Ads] dynamiskt sökmål

Du kan skapa dynamiska sökmål för att definiera sidor på dina webbplatser (dvs. de domäner som används i annonsernas webbadresser) vars innehåll används för att rikta in dina dynamiska sökannonser i samma annonsgrupp.

Du kan ange alla villkor eller upp till tre enskilda villkor som mål.

>[!NOTE]
>
>För bästa spårningsprestanda skapar du ett [!UICONTROL All Targets]-mål för endast en annonsgrupp per kampanj.

>[!TIP]
>
>Om du vill skapa flera kontokomponenter samtidigt använder du [kampanjmallar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Välj annonsnätverket, kontot, kampanjen och annonsgruppen och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målinställningarna för [dynamisk sökning](#dynamic-search-target-settings).

1. Klicka på **[!UICONTROL Post]**.

## Redigera inställningar för det dynamiska sökmålet [!DNL Google Ads]

Du kan redigera status eller maximalt bud för ett [!DNL Google Ads] dynamiskt sökmål. Du kan inte ändra de villkor som anges som mål.

>[!TIP]
>
>Om du vill redigera stora mängder data samtidigt använder du [kampanjmallar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]** på undermenyerna.

1. Markera kryssrutan bredvid varje rad som ska redigeras.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet ovanför datatabellen.

1. Ange målinställningarna för [dynamisk sökning](#dynamic-search-target-settings).

   För flera mål tillämpas ändringarna på alla valda mål. För [!UICONTROL Bid field] kan du ändra befintliga värden till ett angivet värde eller antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

1. Spara data:

   * (Enstaka mål) Klicka på **[!UICONTROL Post]**.

   * (Flera annonsgrupper) Klicka på **[!UICONTROL Post Now]**.

## Ändra status för [!DNL Google Ads] dynamiska sökmål

Du kan pausa alla aktiva dynamiska sökmål i en kampanjtyp som stöds om du inte längre vill använda dem för dynamiska sökannonser i samma annonsgrupp. Du kan sedan använda dem som mål genom att ändra annonsstatusen tillbaka till aktiv.

Du kan också ta bort alla dynamiska mål.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Auto Targets]** på undermenyerna.

1. (Valfritt) Filtrera listan så att den innehåller specifika dynamiska mål.

1. Gör något av följande:

   * Om du vill ändra status för ett dynamiskt mål klickar du i kolumnen **[!UICONTROL Status]** och ändrar status.

   * Så här tar du bort ett eller flera dynamiska mål:

      1. Markera kryssrutan bredvid varje dynamiskt mål som du vill ta bort.

     Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicka på ![Mer](/help/search-social-commerce/assets/more.png "Mer") i verktygsfältet och välj **[!UICONTROL Delete]**.

      1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

## [!DNL Google Ads] inställningar för dynamiskt sökmål {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Krävs om du inte anger en webbplatsdomän och ett språk i kampanjens [!UICONTROL DSA Options]-avsnitt, skrivskyddat för befintliga mål) Dynamiska sökmål för annonsgruppen:

* *[!UICONTROL All Targets]* (standard): Alla indexerade sidor anges som mål.

* *\[Särskilda mål\]:* Målar upp till tre villkor för indexerade sidor. När du väljer det här alternativet måste du ange villkoren genom att ange informationskategorier och specifika värden som annonserna ska riktas mot (t.ex.&quot;URL:en innehåller skor.exempel.com&quot;). Om du vill ange fler än ett villkor klickar du på **[!UICONTROL + And]**. Målkriterierna är följande:

   * *[!UICONTROL Category]:* Om du vill visa annonser för indexerade sidor med en specifik [!DNL Google Ads] innehållskategori.

   * *[!UICONTROL URL]:* Om du vill visa annonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.

   * *[!UICONTROL Page Title]:* Om du vill visa annonser för indexerade sidor med specifik text i sidrubriken.

   * *[!UICONTROL Page Content]:* Om du vill visa annonser för indexerade sidor med specifikt innehåll.

**Status:** Status för målinställningarna:

* *[!UICONTROL Active]* (standard): Aktiverar budgivning.

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
