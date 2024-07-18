---
title: Aktivera överföring av mål till annonsnätverk
description: Lär dig hur du överför mål för dina hybridportföljer till  [!DNL Google Ads] och [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: f491537c2dd56716abe0ab4fa8c26b8558dca664
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Aktivera överföring av mål till annonsnätverk

*Annonsörer med endast [!DNL Google Ads] och [!DNL Microsoft Advertising] konton*

*Annonsörer endast aktiverade för hybridoptimering*

Search, Social och Commerce kan överföra målen för ett annonserkontos portföljer till [!DNL Google Ads] och [!DNL Microsoft Advertising] så att du kan använda dem för hybridoptimering. De uppladdade målen är tillgängliga som konverteringsåtgärder för anpassade konverteringsmål på kontonivå och kampanjnivå.

Om du aktiverar det här alternativet aktiveras automatiskt en överföring för mål i portföljer som innehåller kampanjer med smarta budgivningsstrategier. Search, Social, &amp; Commerce skapar en konvertering i annonsnätverket för varje relevant mål. Konverteringen representerar alla viktade konverteringsvärden i målet på nivån för EF-ID (klicka-ID). För [!DNL Google Ads] klick är EF-ID:t [!DNL Google Ads] `gclid`; för [!DNL Microsoft Advertising] klick är EF-ID:t [!DNL Microsoft Advertising] `msclkid`. På grund av det här klicknings-ID:t kan konverteringsdata mappas till det specifika nyckelordet och klicktiden.

Varje överförd konvertering har följande namn:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

där `<network_ID>` är det numeriska ID som Search, Social och Commerce använder för annonsnätverket, är `<objective_id>` det numeriska mål-ID:t och `<network_account_ID>` är det numeriska ID:t för annonsnätverkskontot eller hanterarkontot.

Överföringar till [!DNL Google Ads] sker dagligen kl. 06:00 i annonsörens tidszon. Överföringar till [!DNL Microsoft Advertising] sker dagligen kl. 09:00 i annonsörens tidszon.

>[!IMPORTANT]
>
>Konverteringar som spåras av Google Ads och Microsoft Advertising UET-taggen (Universal Event tracking) överförs inte till annonsnätverken igen. Om ni inkluderar dem i ett mål måste ni lägga till dem i kampanjmålen i annonsnätverkets redaktör.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]** på huvudmenyn.

1. Markera kryssrutan bredvid **[!UICONTROL Enable Objective Upload]**.

1. (Annonsörer med [!DNL Google Ads] konton som gör affärer i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK); valfritt) Om du har inhämtat samtycke från användare i EES och Storbritannien att överföra sina data i annonssyfte markerar du kryssrutan bredvid **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicka på **[!UICONTROL Save]**.

1. (Om dina konverteringar spåras på en hanterarkontonivå) [Lägg till autentiseringsuppgifter för ditt hanterarkonto](/help/search-social-commerce/admin/manager-accounts.md) på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Kontrollera att varje mål - med namnet `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - visas inom två dagar i annonsnätverket.

   I [!DNL Google Ads]-redigeraren söker du upp dina [konverteringsåtgärder](https://support.google.com/google-ads/answer/11461796). I [!DNL Microsoft Advertising]-redigeraren ska du slå upp dina [konverteringsmål](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Uppdatera vid behov datumintervallet så att det innehåller överföringsdatumet.

## Hur det viktade målet beräknas

Det viktade målet som skickas till annonsnätverket är summan av alla mätvärden som samlats in, med undantag för konverteringar som spåras av [!DNL Google Ads] eller UET-taggen ([!DNL Microsoft Advertising] Universal Event tracking). Värdet beräknas med hjälp av den attribueringsmetod som har ställts in för annonsörens konto Search, Social och Commerce.

Exempel: Målmåttet är Art Additions med vikten 25, och dina mått inkluderar GGL_Lead och Revenue med vikten 1 och Downloads med vikten 0,5.

![Exempel på ett viktat mål](/help/search-social-commerce/assets/objective-example.png "Exempel på ett viktat mål")

Anta att ett nyckelord resulterade i följande åtgärder för portföljen:

* 10 kundvagnstillägg
* 500 dollar i intäkt
* 50 nedladdningar
* 5 GGL_Lead

GGL_Lead tas inte med i beräkningen/överföringen eftersom det är ett Google Ads-spårat mätvärde. Det viktade objektiva värdet beräknas därför som ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Du kan visa data för Adobe Advertising-viktade intäkter i annonsnätverkets rapporter. Det bästa sättet är att jämföra de viktade intäkterna med [!DNL Google Ads] &quot;All conv. (efter konv. time) eller måttet [!DNL Microsoft Advertising], All conv. intäkter,&quot; segmenterad till O_ACS_OBJ*-mätvärdet.<!--clarify -->

## Felsöka saknade mål

Om målet - med namnet `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - för en av dina portföljer inte visas i annonsnätverket ska du kontrollera följande:

* ([!DNL Google Ads]) Kontrollera om konverteringarna ska överföras till konto- eller hanterarnivå. Om de ska överföras på ledningsnivå:

   * Kontrollera om autentiseringsuppgifterna för hanterarkontot [!DNL Google Ads] anges på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Om det behövs [lägger du till autentiseringsuppgifterna för hanterarkontot](/help/search-social-commerce/admin/manager-accounts.md).

   * Kontrollera om annonsnätverkskontot redan innehåller samma måttnamn. Om den gör det byter du namn på måttet så att du kan skapa rätt egenskap på hanterarnivå.

* Kontrollera att portföljens&quot;hybridalternativ&quot; har valts och att målet har giltiga intäkter.

>[!MORELIKETHIS]
>
>* [Om att hantera en annonsörs konverteringsmått](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Överför konverteringsmått till  [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
