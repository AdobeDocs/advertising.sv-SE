---
title: Krav för att konfigurera en  [!DNL Google Analytics] datakälla
description: Lär dig mer om de steg du måste slutföra innan du konfigurerar en [!DNL Google Analytics] datakälla.
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Krav för att konfigurera en [!DNL Google Analytics]-datakälla

Innan du kan konfigurera en [!DNL Google Analytics]-datakälla måste du ange frågesträngsparametern ef_id för sökning, sociala medier och Commerce som primärnyckel för att skicka data från [!DNL Google Analytics] till Search, Social och Commerce. Ställ in den primära nyckeln för varje kombination av [!DNL Google Analytics]-konto och egenskaper som du vill synkronisera data för. Andra personer i organisationen kan behöva utföra dessa uppgifter; se nedan för mer information.

Om landningssidans URL:er för dina annonser eller nyckelord inte redan innehåller omdirigeringar av typen Sök, Socialt och Commerce, ska du lägga till dem först.

## Krav 1: Implementera en sök-, social- och Commerce-token (&quot;ef_id&quot; frågesträngsparameter) i landningssidans URL:er för alla tillämpliga annonskonton

På varje betald sökklick för relevanta kampanjer måste en unik `ef_id` genereras och läggas till i landningssidans URL som en frågesträng, till exempel `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, där `&ef_id=abcde:123456789:s` är tilläggssymbolen, `ef_id`-nyckeln och `ef_id`-värdet. Om du vill ta med ett ef_id måste de relevanta annonsnätverkskontona och kampanjerna ha [!UICONTROL Tracking Type] [!UICONTROL EF Redirect] och [!UICONTROL Redirect Type] [!UICONTROL Token].

För befintliga konton och kampanjer är ef_id antagligen redan implementerat.

Om ef_id inte finns med ber du ditt kontoteam på Adobe om hjälp.

När alla nödvändiga komponenter har slutförts används `ef_id` som primärnyckel för att skicka data från [!DNL Google Analytics] till Search, Social och Commerce.

## Krav 2: Hämta token Search, Social och Commerce (&quot;ef_id&quot; frågesträngsparameter) i en anpassad dimension för varje relevant [!DNL Google Analytics]-egenskap

Upprepa följande uppgifter för varje kombination av konto och egenskap för [!DNL Google Analytics] som du vill synkronisera data för. Mer information om de här åtgärderna finns i [[!DNL Google Analytics] dokumentationen om hur du skapar och implementerar anpassade dimensioner](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article).

1. Skapa en anpassad dimension med namnet `ef_id` i [!DNL Google Analytics]. Ange dimensionens omfång till [!DNL User] och ställ in dimensionen på aktiv.

   >[!NOTE]
   >
   >Den här förutsättningen kräver redigeringsbehörighet för de relevanta egenskaperna.

1. Uppdatera spårningskoden för [!DNL Google Analytics] för att hämta värdet för frågesträngparametern ef_id när den finns i landningssidans URL och lagra den i den anpassade dimensionen ef_id.

   >[!NOTE]
   >
   >ef_id ska bara finnas i URL:er för landningssidor.

   Om till exempel landningssidans URL är `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf` är värdet för ef_id-dimensionen i [!DNL Google Analytics] `abcde:123456789:s`.

   >[!NOTE]
   >
   >Detta krav ska uppfyllas av en kvalificerad utvecklare.

>[!MORELIKETHIS]
>
>* [Synkronisering av  [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Konfigurera en [!DNL Google Analytics] vy som datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgängliga [!DNL Google Analytics] mått](data-source-ga-metrics.md)
