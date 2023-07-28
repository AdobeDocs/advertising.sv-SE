---
title: '''[!DNL Microsoft® Advertising] produktgruppsinställningar'
description: Referera inställningarna för [!DNL Microsoft® Advertising] shoppingproduktgrupper.
exl-id: a34511ef-f5bc-4d93-a56e-90348f670ad6
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] produktgruppsinställningar

## Produktgrupper&quot;Alla produkter&quot;

**[!UICONTROL Condition]:** (Skrivskyddat) Alla produkter

**[!UICONTROL Bid]:** (Endast inkluderade produktgrupper) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för ett reklamklick. Det här värdet används bara för enheter utan underordnade produktgrupper och används i stället för annonsgruppsnivån.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Den här mallen åsidosätter mallar på högre nivåer och används endast för enheter utan underordnade produktgrupper.

## Alla andra produktgrupper

**[!UICONTROL Condition/Value]:** (Skrivskyddat för befintliga produktgrupper) De produktdimensioner som ska anges som mål. För nya produktgrupper anger du den dimension som ska användas som målprodukter och kvalificeringsattributet för den valda informationskategorin (till exempel&quot;Acme&quot; när du riktar dig mot varumärket eller&quot;New&quot; när du riktar dig mot en viss produktgrupp).

När du har skapat en produktgrupp för specifika produktdimensioner (det vill säga inte&quot;Alla produkter&quot;) skapar Search, Social och Commerce automatiskt en produktgrupp för&quot;Allt annat&quot;.

En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanjer](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; Din lista över dimensioner kan begränsas baserat på kampanjens [!UICONTROL Inventory Filter] inställning.

**[!UICONTROL Excluded]:** (Valfritt för nya produktgrupper, skrivskyddat för befintliga produktgrupper) Utesluter annonser för matchande produkter.

**[!UICONTROL Bid]:** (Endast inkluderade produktgrupper) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för ett reklamklick. Det här värdet används bara för enheter utan underordnade produktgrupper och används i stället för annonsgruppsnivån.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Den här mallen åsidosätter mallar på högre nivåer och används endast för enheter utan underordnade produktgrupper.

>[!MORELIKETHIS]
>
>* [Om att handla produktgrupper](product-group-about.md)
>* [Hantera produktgrupper för butik](product-group-manage.md)
>* [Produktfilter för köpkampanjer](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementera [!DNL Microsoft® Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
