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

Du kan ändra vilken rapportmall, [!DNL Microsoft Excel]-mall och andra parametrar som används för en kalkylbladsfeed.

>[!NOTE]
>
> Om du redigerar kolumnerna i rapportmallen eller använder en ny eller uppdaterad rapportmall måste du uppdatera [!DNL Excel]-mallen och överföra den igen.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]** på huvudmenyn.

1. (Valfritt) Om du vill uppdatera rapportmallen eller mallen [!DNL Excel] som används för kalkylarksfeeden:

   * (Valfritt) Om du vill använda en annan eller uppdaterad rapportmall för feeden [skapar du en ny [!DNL Excel] mall för rapportmallen](spreadsheet-feed-create-excel-template.md).

     Du måste överföra både rapportmallen och den nya [!DNL Excel]-filen i nästa steg.

   * (Valfritt) Om du bara vill lägga till anpassade kolumner i mallen [!DNL Excel] infogar du kolumnerna till höger om kolumnerna från rapportmallen och sparar sedan filen som ett [!DNL Excel] -kalkylblad i XLSX-format. Du måste överföra den nya [!DNL Excel]-filen i nästa steg.

1. Ändra inställningar för kalkylbladsfeed:

   * Klicka på **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]** på huvudmenyn.

   * Bredvid namnet på kalkylbladsfeeden klickar du på ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar").

   * I dialogrutan [!UICONTROL Edit Spreadsheet Feed] ändrar du inställningarna för [kalkylbladsfeed](spreadsheet-feed-settings.md).

   * Klicka på **[!UICONTROL Submit]**.

   * (Valfritt) När matningens [!UICONTROL Update Status] är *[!UICONTROL Finished]* klickar du på **[!UICONTROL XLSX]** intill matningen och öppnar eller sparar sedan filen enligt webbläsarens normala procedur.

     >[!NOTE]
     >
     > Om rapportmallen som är kopplad till feeden tas bort senare, tas även feeden bort.

     Kalkylbladsflödena uppdateras automatiskt klockan 08:00 varje dag i annonsörens tidszon. Om rapportmallen innehåller adresser för alla e-postmottagare får dessa adresser meddelanden när kalkylbladet uppdateras.

>[!MORELIKETHIS]
>
>* [Om tabellrapportfeeds](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Skapa en [!DNL Excel] mall för ett kalkylbladsrapportflöde](spreadsheet-feed-create-excel-template.md)
>* [Redigera inställningar för kalkylbladsrapportfeed](spreadsheet-feed-edit.md)
>* [Inställningar för kalkylbladsrapportfeed](spreadsheet-feed-settings.md)
>* [Visa eller spara en kalkylbladsrapportfeed-fil](spreadsheet-feed-view-or-save.md)
>* [Uppdatera kalkylbladsrapportfeeds manuellt](spreadsheet-feed-refresh.md)
