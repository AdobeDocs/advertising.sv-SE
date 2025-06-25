---
title: Hantera modifierare
description: Lär dig hur du konfigurerar och hanterar modifierare för dina annonsmallar för lagerdataflöden.
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Hantera modifierare

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Modifierare är adjektiver eller annonser som kan läggas till i eller tas bort från en mening utan att ändra den grundläggande meningsstrukturen. Du kan skapa grupper med modifierare som du kan använda som variabler i olika datafält i flödesdatamallar. Genom att ta med modifierare i kontostrukturfält (kampanj och annonsgrupp), nyckelord, bas-URL:er och annonser, skapar du ett värde för varje associerat modifieringsvärde. Om du till exempel använder en modifierargruppvariabel i en annonsrubrik och modifierargruppen innehåller tre modifierare (&quot;billig&quot;,&quot;rabatt&quot; och&quot;överkomlig&quot;) skapas tre separata annonser för varje datarad i dataflödet - en för varje modifierare. Om du inkluderar en modifieringsgrupp med flera värden i bas-URL:en för en annonsgrupp skapas en uppsättning nyckelord för var och en av de resulterande bas-URL:erna.

Varje modifieringsgrupp kan innehålla så många modifierare du vill. Varje mall kan bara använda en modifieringsgrupp.

## Skapa en modifieringsgrupp

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på **[!UICONTROL Modifiers]** i verktygsfältet ovanför datatabellen.

1. Klicka på **[!UICONTROL Create]** ovanför listan med modifieringsgrupper.

1. Ange gruppinställningar för modifierare:

   **[!UICONTROL Name]:** Namnet på modifieringsgruppen.

   **[!UICONTROL Modifiers]:** Gruppens modifieringsvärden (ett per rad).

1. Klicka på **[!UICONTROL Save]**.

## Redigera en ändringsgrupp

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på **[!UICONTROL Modifiers]** i verktygsfältet ovanför datatabellen.

1. Klicka på modifieringsgruppens namn i listan över modifieringsgrupper.

1. Redigera gruppinställningarna för modifierare:

   **[!UICONTROL Name]:** Namnet på modifieringsgruppen.

   **[!UICONTROL Modifiers]:** Gruppens modifieringsvärden (ett per rad).

1. Klicka på **[!UICONTROL Save]**.

## Ta bort ändringsgrupper

>[!IMPORTANT]
>
>När du tar bort en modifieringsgrupp tar du bort alla variabler för den modifieringsgruppen (som anges som `<modifier_group_name>`) från fälten för befintliga mallar. Om du försöker sprida data via en mall med variabler för modifierare som inte finns, misslyckas jobbet1.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på **[!UICONTROL Modifiers]** i verktygsfältet ovanför datatabellen.

1. Markera kryssrutan bredvid varje modifieringsgrupp som du vill ta bort.

1. Klicka på **[!UICONTROL Delete]** ovanför listan med modifieringsgrupper.

1. Klicka på **[!UICONTROL Yes]** i bekräftelsemeddelandet.

1. (Om det behövs) [Ta bort referenser till modifieraren](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) från alla tillämpliga mallar.

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Hantera annonsmallar](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
