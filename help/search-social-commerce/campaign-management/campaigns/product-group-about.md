---
title: Om att handla produktgrupper
description: Läs mer om att handla produktgrupper i shoppingkampanjer.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Om att handla produktgrupper

*[!DNL Google Ads]och [!DNL Microsoft® Advertising] endast köpkampanjer*

I shoppingkampanjer avgör era produktgrupper - inte nyckelord - vilka produkter på ert handelscenter som annonserna visas för. Varje produktgrupp baseras på ett enda produktattribut (t.ex. kategori, produkttyp, märke, villkor, produkt-ID eller anpassade etiketter) och använder samma bud för alla matchande produkter. Du kan inkludera eller exkludera anbud för produkterna i varje grupp.

Du konfigurerar produktgrupper på annonsgruppsnivå för att avgöra vilka produkter i ert handlarcenterkonto som visas i annonsgruppens shoppingannonser. Även om annonsgruppen inte innehåller annonsenheter, visas annonsnätverket fortfarande annonser för produkterna.

När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

Mer information om [!DNL Google] shoppingkampanjer och annonser, se&quot;[Implementera [!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; och [Google Ads-dokumentation](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Mer information om [!DNL Microsoft®] shoppingkampanjer, se&quot;[Implementera [!DNL Microsoft® Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; och [[!DNL Microsoft® Advertising] dokumentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Support finns inte för [!DNL Google Ads] med en lista över grupper i maximala resultatkampanjer, som ersätter smarta shoppingkampanjer. Använd [!DNL Google Ads] redigerare.

## Produktgruppshierarki

Innan du kan skapa produktgrupper med specifika attribut för en annonsgrupp måste du först skapa en produktgrupp som innehåller alla funktioner och som heter[!UICONTROL All Products].&quot; Från den här överordnade produktgruppen kan du skapa underordnade produktgrupper för delmängder av produkter, och du kan skapa underordnade från de underordnade produktgrupperna. När du har skapat den första underordnade produktgruppen för en annonsgrupp, en annan produktgrupp som kallas[!UICONTROL Everything Else]&quot; skapas automatiskt med standardanbudet för annonsgrupp. När du lägger till fler produktgrupper visas[!UICONTROL Everything Else]gruppen justeras i enlighet därmed så att den utgör alla produkter som inte ingår i en annan produktgrupp.

Inom en annonsgrupp kan du skapa upp till sju nivåer av produktgrupper (exklusive &quot;[!UICONTROL All Products]&quot;) att inkludera eller exkludera från anbud, med en eller flera produktgrupper som har samma attribut på varje nivå (till exempel [!UICONTROL Brand]=Köp för en produktgrupp och [!UICONTROL Brand]=AcmePlus för ett annat på samma nivå). Överordnade produktgrupper kallas underindelningar och den lägsta nivån av indelning kallas en enhet. Du kan ange offerter och spårningsmallar, eller helt exkludera budgivning, på enhetsnivå. Hela uppsättningen aktiva produktgrupper för en annonsgrupp används hierarkiskt för att avgöra vilka produkter som omfattas. Om du till exempel delar upp [!UICONTROL All Products] till [!UICONTROL Brand]=AcmeBasic och [!UICONTROL Brand]=AcmePlus, och sedan kan du dela upp var och en av dessa produktgrupper ytterligare [!UICONTROL Condition]=Nytt och ange anbud. Endast nya produkter med varumärkena AcmeBasic och AcmePlus får annonseras eller uteslutas från annonser.

![Exempel på en produktgrupp](/help/search-social-commerce/assets/product-group-list.png "Exempel på en produktgrupp")

![Exempel på produktgruppshierarki](/help/search-social-commerce/assets/product-group-tree.png "Exempel på produktgruppshierarki")

## The [!UICONTROL Product Groups] visa

Du kan skapa och redigera produktgrupper och ta bort produktgrupper och deras underordnade produktgrupper i [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] vy.

## Spårnings- och prestandadata för kundproduktgrupper

(Konton/kampanjer med &quot;[!UICONTROL EF Redirect]&quot; spårningsalternativ) Om du vill tillåta sökningar, sociala medier och Commerce att spåra konverteringar för produktgrupper, [generera spårnings-URL:er för produktgrupper med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md)och gör sedan något av följande:

* (Krävs för [!DNL Google Ads]; bästa praxis för [!DNL Microsoft® Advertising]) Lägg till spårnings-URL:en i [!DNL Tracking Template] i inställningarna för konto, kampanj eller produktgrupp. För enklare underhåll bör du lägga till dem på högsta möjliga nivå. Alla tilläggsparametrar som har angetts för kontot eller kampanjen inkluderas inte.

  >[!CAUTION]
  >
  >([!DNL Microsoft® Advertising]) Använd bara det här alternativet om du inte inkluderar URL:er för sökning, sociala medier och Commerce-spårning i en anpassad kolumn i produktflödet. Om du gör båda, kommer URL-adresserna att innehålla två omdirigeringar och orsaka brutna länkar.

* ([!DNL Microsoft® Advertising] (endast) Lägg till spårnings-URL:en till produktdata i [!DNL Microsoft® Merchant Center] konto. Om du vill göra det tar du med spårnings-URL:en tillsammans med värdet i `link` eller `mobile_link` fält, om det är lämpligt, i en anpassad kolumn som kallas [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) i produktflödet. URL:er som skapas med den här metoden innehåller inte spårningsparametrar som anges i konto- eller kampanjinställningarna i Sök, Socialt och Commerce.

Du kan visa data om produktgrupper i [den [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Hantera produktgrupper för butik](product-group-manage.md)
>* [[!DNL Google Ads] produktgruppsinställningar](product-group-settings-google.md)
>* [Implementera [!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft® Advertising] produktgruppsinställningar](product-group-settings-microsoft.md)
>* [Implementera [!DNL Microsoft® Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
