---
title: Ställ in en programgaranterad affär
description: Lär dig hur du skapar ett programmatiskt garantiavtal (PG) som du har förhandlat fram med en utgivare.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: f887524a22dd5d665dcfc38b1a4ce2a1242638d7
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Ställ in en programgaranterad affär

*[Endast plattformar som stöds av leverantörer](programmatic-guaranteed-about.md)*

När du har förhandlat om en programmatisk garanti (PG) med en utgivare som stöds kan du konfigurera avtalet i DSP med [!DNL Deal ID inbox] eller genom att ange avtalsinformationen manuellt.

>[!NOTE]
>
> För PG-avtal hanterar utgivaren allt budgetutrymme, budgetbegränsning och målinriktning. Alla SSP:er som tillåter PG via DSP bekräftar att utgivaren kan ställa in budgetbegränsning.
>
> Konfigurera programmatiska garanterade avtal med utgivare på [!DNL FreeWheel] kräver extra behörigheter och steg. Se &quot;[Översikt över hur man ställer in garantierbjudanden för programmatiska inköp i [!DNL FreeWheel]](freewheel-overview.md)&quot; för mer information.

## Konfigurera en programmatisk garanterad affär med [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Följande metod rekommenderas för [!DNL FreeWheel], [!DNL Google Authorized Buyers]och [!DNL Magnite DV+].

1. [Acceptera erbjudandet](deal-id-inbox-accept.md).

1. När du har sparat erbjudandet väljer du de annonser (eller 1 x 1-pixel för spårning av annonser som hanteras av utgivaren) som ska användas för erbjudandet och skapar en programmatisk standardplacering som garanteras (PG) enligt uppmaningen.

   Det är obligatoriskt att skapa en standardplacering för PG-paketet för att få 100 % av köpet. Den här typen av placering har ingen inriktning så DSP kan returnera ett bud till alla anbudsförfrågningar från utgivaren.

   * Om du bara tecknar ett enstaka erbjudande omdirigeras du automatiskt till arbetsflödet för att skapa standardplaceringar i PG.

     Alla [!DNL FreeWheel] Erbjudandena föreslås som ett enda avtal.

   * Om du godkänner ett förslag med flera PDF-avtal-ID:n ska du identifiera varje PG-standardplacering som du måste skapa. När du har skapat alla obligatoriska placeringar aktiveras knappen Fortsätt.

1. (Valfritt) Rikta in dig på PG-erbjudandet genom att klicka på ![Alternativ-menyn](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ett avtal kan vara avsett för flera praktik som stöder valfri kombination av medietyper (t.ex. ansluten TV, dator och ljud).

## Ställ in en programmatisk garantiavtal manuellt

Använd den här metoden för alla andra SSP:er.

1. [Ställ in detaljer för erbjudande-ID manuellt](deal-id-create.md).

1. När du har sparat erbjudandet väljer du de annonser (eller 1x1-spårningspixlar för annonser som hanteras av utgivaren) som ska användas för erbjudandet och skapar en standardplacering för PG, enligt uppmaningen.

   Det är obligatoriskt att skapa en PG-standardplacering för erbjudandet för att få 100 % av köpet. Den här typen av placering har ingen inriktning så DSP kan returnera ett bud till alla anbudsförfrågningar från utgivaren.

1. (Valfritt) Rikta in dig på PG-erbjudandet genom att klicka på ![Alternativ-menyn](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ett avtal kan vara avsett för flera praktik som stöder valfri kombination av medietyper (t.ex. ansluten TV, dator och ljud).

>[!MORELIKETHIS]
>
>* [Om programmatiska erbjudanden](programmatic-guaranteed-about.md)
>* [Tips för att förhandla om ett program med garanterad programmering](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Skicka in en annons för en programmatisk garanterad affär med [!DNL FreeWheel]](freewheel-submit.md)
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Skapa information om avtal-ID manuellt](deal-id-create.md)
>* [SSP-partners](ssp-partners.md)
>* [Översikt över inventeringsfunktioner](inventory-overview.md)
