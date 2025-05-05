---
title: De inledande inställningsaktiviteterna för rapporter
description: Lär dig hur du gör mätvärden tillgängliga i rapporter och hur du automatiserar rapporter.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# De inledande inställningsaktiviteterna för rapporter

Nya användare bör utföra följande initiala konfigurationsuppgifter:

* Gör konverteringsmåtten som Adobe Advertising spårar för annonsören [tillgängliga för rapporter och andra vyer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md), och [ändra eventuellt namn på konverteringsmåtten] (/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md som visas i kolumnrubriker för läsbarhet.

  Transaktionsegenskaper är inte tillgängliga för rapporter om du inte uttryckligen gör dem tillgängliga.

  Om du senare börjar spåra ett nytt konverteringsmått måste du upprepa den här uppgiften.

* (Valfritt) Automatisera rapportgenerering:

   * Om du regelbundet vill generera rapportdata för en viss tidsperiod, t.ex. en [!UICONTROL Campaign Report] för den senaste veckan eller de senaste 30 dagarna, kan du konfigurera [rapportmallar](/help/search-social-commerce/reports/automation/templates/template-about.md) och schemalägga att de ska köras varje dag eller en viss dag i veckan eller månaden. Varje gång rapporten är schemalagd att köras genereras en ny rapport. Du kan meddela e-postadresserna till specifika användare av sökningar, sociala medier och Commerce när rapporten har slutförts, baserat på de [meddelandeinställningar som har konfigurerats i [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Om du vill visa aktuella, dagliga rapportdata i ett anpassat kalkylblad, med eller utan pivottabeller och eventuella ytterligare kolumner som du behöver för att utföra ytterligare beräkningar, kan du skapa en daglig [kalkylbladsfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Kalkylbladsflödena uppdateras dagligen med de senaste prestandadata och fortsätter att behålla data för de föregående datumen. Om du vill konfigurera kalkylbladsfeeds måste du först skapa en anpassad kalkylbladsmall i [!DNL Microsoft Excel]. Du kan meddela e-postadresserna till specifika användare av Sök, Socialt och Commerce när en feed-fil är tillgänglig, baserat på de [meddelandeinställningar som konfigurerats i [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Om du vill få grundläggande och avancerade rapporter på en FTP-plats kan du konfigurera [FTP-åtkomst till grundläggande och avancerade rapporter](/help/search-social-commerce/reports/automation/ftp-reports.md) genom att begära ett FTP-konto och konfigurera rapportmallar med en specifik namnkonvention.

>[!MORELIKETHIS]
>
>* [Om rapporter](report-about.md)
>* [Data som används för rapporter](data-used-for-reports.md)
