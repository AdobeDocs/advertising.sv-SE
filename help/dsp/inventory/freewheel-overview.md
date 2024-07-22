---
title: Översikt över konfiguration av PG-erbjudanden i  [!DNL Freewheel]
description: Lär dig mer om förutsättningarna och de extra steg som krävs för att köra annonser för programmatiska annonsköp med utgivare på  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Översikt över inställning av programmatiska garanterade erbjudanden i [!DNL Freewheel]

Om du ställer in programmatiska garanterade avtal med utgivare på [!DNL Freewheel] krävs extra behörigheter och steg.

>[!PREREQUISITES]
>
>Arbeta med ditt kontoteam på Adobe för att se till att ditt [!DNL DSP]-konto har följande behörigheter:
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
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Skicka en annons för en programmatisk garanterad affär till [!DNL Freewheel]](freewheel-submit.md)
>* [Kontrollera status för annonser för [!DNL FreeWheel] Programmatiska garanterade erbjudanden](freewheel-check-status.md)
>* [Felkoder för  [!DNL Freewheel] Lägg till överföringar](freewheel-error-codes.md)
