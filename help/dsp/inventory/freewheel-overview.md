---
title: Översikt över att konfigurera PG-erbjudanden i  [!DNL Freewheel]
description: Lär dig mer om förutsättningarna och de extra steg som krävs för att köra annonser för programmatiska annonsköp med utgivare på  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Översikt över hur du ställer in garanterade programerbjudanden i [!DNL Freewheel]

Om du ställer in programmatiska garanterade avtal med utgivare på [!DNL Freewheel] krävs extra behörigheter och steg.

>[!PREREQUISITES]
>
>Arbeta med ditt Adobe-kontoteam för att se till att ditt [!DNL DSP]-konto har följande behörigheter:
>
>* Behörighet att använda det programmatiska garanterade arbetsflödet [!DNL FreeWheel], som krävs för att skicka en annons för ett programmatiskt erbjudande till [!DNL FreeWheel].
>
>* (Om du arbetar med utgivare i Storbritannien som behöver ett [!DNL Clearcast]-klocknummer med varje annons) Tillstånd att inkludera klocknummer i dina annonser.

## Arbetsflöde

1. Skapa en annons med medietypen som anges i erbjudandet.

   För vissa utgivare i Storbritannien måste du inkludera ett [!DNL Clearcast]-klocknummer i annonsen.

1. [Acceptera det erbjudande-ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) som du redan har förhandlat med en utgivare på [!DNL Freewheel] med hjälp av Inkorgen för avtal-ID.

   När du har godkänt erbjudandet följer du instruktionerna för 1) väljer annonsen som ska användas för erbjudandet och 2) skapar en programmatisk garanterad standardplacering för annonsen.

1. [Skicka annonsen till  [!DNL Freewheel]](freewheel-submit.md)

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status för annonsinlämning](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Skicka en annons för ett programmatiskt garanterat erbjudande till [!DNL Freewheel]](freewheel-submit.md)
>* [Kontrollera status för annonser för ett [!DNL FreeWheel] PG-avtal](freewheel-check-status.md)
>* [Felkoder för [!DNL FreeWheel] och inskickade &#x200B;](freewheel-error-codes.md)
