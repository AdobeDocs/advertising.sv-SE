---
title: Redigera inställningar för matning av kalkylbladsrapporter
description: Lär dig hur du redigerar inställningarna för kalkylbladsfeeds.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Redigera inställningar för matning av kalkylbladsrapporter

*Endast för grundläggande rapporter och modellnoggrannhetsrapporter*

Du kan ändra vilken rapportmall som [!DNL Microsoft Excel] -mallar och andra parametrar används för kalkylbladsfeeds.

>[!NOTE]
>
> Om du redigerar kolumnerna i rapportmallen eller använder en ny eller uppdaterad rapportmall måste du uppdatera [!DNL Excel] och ladda upp mallen igen.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Valfritt) Uppdatera rapportmallen eller [!DNL Excel] mall som används för kalkylarksmatning:

   * (Valfritt) Om du vill använda en annan eller uppdaterad rapportmall för flödet [skapa en ny [!DNL Excel] mall för rapportmallen](spreadsheet-feed-create-excel-template.md).

     Du måste överföra både rapportmallen och den nya [!DNL Excel] i nästa steg.

   * (Valfritt) Om du bara vill lägga till anpassade kolumner i [!DNL Excel] infogar du kolumnerna till höger om kolumnerna från rapportmallen och sparar sedan filen som en [!DNL Excel] kalkylblad i XLSX-format. Du måste ladda upp den nya [!DNL Excel] i nästa steg.

1. Ändra inställningar för kalkylbladsfeed:

   * Klicka på **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Klicka på bredvid namnet på kalkylbladsfeeden ![Knappen Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Knappen Visa/redigera inställningar").

   * I [!UICONTROL Edit Spreadsheet Feed] dialogrutan, ändra [matningsinställningar för kalkylblad](spreadsheet-feed-settings.md).

   * Klicka på **[!UICONTROL Submit]**.

   * (Valfritt) När matningen är klar [!UICONTROL Update Status] är *[!UICONTROL Finished]*, klicka **[!UICONTROL XLSX]** intill feeden och öppna eller spara sedan filen i enlighet med webbläsarens normala procedur.

     >[!NOTE]
     >
     > Om rapportmallen som är kopplad till feeden tas bort senare, tas även feeden bort.

     Kalkylbladsflödena uppdateras automatiskt klockan 08:00 varje dag i annonsörens tidszon. Om rapportmallen innehåller adresser för alla e-postmottagare får dessa adresser meddelanden när kalkylbladet uppdateras.

>[!MORELIKETHIS]
>
>* [Om rapportfeeds för kalkylblad](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Skapa en [!DNL Excel] mall för kalkylbladsrapportflöde](spreadsheet-feed-create-excel-template.md)
>* [Redigera inställningar för matning av kalkylbladsrapporter](spreadsheet-feed-edit.md)
>* [Feed-inställningar för kalkylbladsrapport](spreadsheet-feed-settings.md)
>* [Visa eller spara en matningsfil för kalkylbladsrapport](spreadsheet-feed-view-or-save.md)
>* [Uppdatera tabellrapportfeeds manuellt](spreadsheet-feed-refresh.md)
