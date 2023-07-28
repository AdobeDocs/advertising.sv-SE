---
title: Krav för att konfigurera en [!DNL Google Analytics] datakälla
description: Lär dig mer om de steg du måste slutföra innan du konfigurerar en [!DNL Google Analytics] datakälla.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Krav för att konfigurera en [!DNL Google Analytics] datakälla

Innan du konfigurerar en [!DNL Google Analytics] datakälla måste du ange frågesträngsparametern ef_id för sökning, sociala medier och handel som primärnyckel för att skicka data från [!DNL Google Analytics] för sökning, sociala medier och handel. Ställ in primärnyckeln för varje [!DNL Google Analytics] konto- och egenskapskombination som du vill synkronisera data för. Andra personer i organisationen kan behöva utföra dessa uppgifter; se nedan för mer information.

Om landningssidans URL:er för dina annonser eller nyckelord inte redan innehåller omdirigeringar av typen Sök, Socialt och Commerce, ska du lägga till dem först.

## Krav 1: Implementera en sök-, social- och handelstoken (&quot;ef_id&quot; frågesträngsparameter) i landningssidans URL:er för alla tillämpliga annonskonton

För varje betald sökning klickar du på de relevanta kampanjerna, en unik `ef_id` måste genereras och läggas till på landningssidans URL som en frågesträng, t.ex. `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, där `&ef_id=abcde:123456789:s` är tilläggssymbolen, `ef_id` och `ef_id` värde. För att inkludera ett ef_id måste de relevanta annonsnätverkskontona och kampanjerna ha [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; och [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

För befintliga konton och kampanjer är ef_id antagligen redan implementerat.

Om ef_id inte finns med ber du ditt kontoteam på Adobe om hjälp.

När alla krav är uppfyllda `ef_id` används som primärnyckel för att skicka data från [!DNL Google Analytics] för sökning, sociala medier och handel.

## Krav 2: Hämta token för sökning, sociala medier och handel (&quot;ef_id&quot; frågesträngsparameter) i en anpassad dimension för varje relevant [!DNL Google Analytics] property

Upprepa följande åtgärder för varje [!DNL Google Analytics] konto- och egenskapskombination som du vill synkronisera data för. Se [[!DNL Google Analytics] dokumentation om hur du skapar och implementerar anpassade dimensioner](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) om du vill ha hjälp med dessa uppgifter.

1. I [!DNL Google Analytics], skapa en anpassad dimension med namnet &quot;`ef_id`&quot;. Ange dimensionens omfång till [!DNL User]och ställ in dimensionen på aktiv.

   >[!NOTE]
   >
   >Den här förutsättningen kräver redigeringsbehörighet för de relevanta egenskaperna.

1. Uppdatera dina [!DNL Google Analytics] spårningskod för att fånga värdet för frågesträngsparametern ef_id när den finns i landningssidans URL och lagra den i den anpassade dimensionen ef_id.

   >[!NOTE]
   >
   >ef_id ska bara finnas i URL:er för landningssidor.

   Om till exempel landningssidans URL är `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, värdet för ef_id-dimensionen i [!DNL Google Analytics] är `abcde:123456789:s`.

   >[!NOTE]
   >
   >Detta krav ska uppfyllas av en kvalificerad utvecklare.

>[!MORELIKETHIS]
>
>* [Synkronisering [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Konfigurera en [!DNL Google Analytics] visa som en datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgänglig [!DNL Google Analytics] mått](data-source-ga-metrics.md)
