---
title: Skicka en annons för ett PG-avtal till  [!DNL FreeWheel]
description: Lär dig hur du begär godkännande av en annons för ett programmatiskt garanterat avtal med en utgivare på  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Skicka en annons för en programmatisk garanterad affär till [!DNL Freewheel]

*Konton med [!DNL FreeWheel] Programmatisk garanterad behörighet*

När du [har accepterat ett programmatiskt garanterat avtal med en utgivare på FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), inklusive att välja en annons och skapa den programmatiska standardplaceringen som ska användas för erbjudandet, måste du skicka annonsen till [!DNL Freewheel] för godkännande.

>[!PREREQUISITES]
>
>Arbeta med kontoteamet på Adobe för att se till att ditt [!DNL DSP]-konto har behörighet att använda det programmatiska garanterade arbetsflödet [!DNL FreeWheel].

1. Kopiera annonsnyckeln för annonsen som används med erbjudandet [!DNL Freewheel]:

   1. Klicka på kampanjens namn.

   1. Klicka på **[!UICONTROL Ads]** på undermenyn.

   1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit]** bredvid annonsnamnet.

   1. När annonsinställningarna är öppna kopierar du den alfanumeriska annonstangenten i den URL som visas i webbläsarens adressfält.

      I följande URL är annonsnyckeln till exempel `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Skicka annonsen till [!DNL Freewheel]:

   1. Gör något av följande:

      * Klicka på **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]** bredvid annonsnamnet.

      * Klicka på **[!UICONTROL Inventory]** > **[!UICONTROL Deals]** på huvudmenyn. Klicka på ![Alternativ-menyn](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]** i avtalsraden.

   1. Verifiera erbjudande-ID, ange **[!UICONTROL Ad Key]** som du kopierade i steg 1 och klicka sedan på **[!UICONTROL Submit]**.

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status för annonsinlämning](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Översikt över hur du ställer in garantierbjudanden för programmatiska inköp i  [!DNL Freewheel]](freewheel-overview.md)
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Kontrollera status för annonser för [!DNL FreeWheel] Programmatiska garanterade erbjudanden](freewheel-check-status.md)
>* [Felkoder för  [!DNL Freewheel] Lägg till överföringar](freewheel-error-codes.md)
