---
title: Använda  [!DNL Last Event Service] JavaScript-biblioteket med [!DNL Web SDK]
description: Lär dig hur du växlar från att använda biblioteket  [!DNL Analytics] [!DNL visitorAPI] till biblioteket  [!DNL Experience Platform] [!DNL Web SDK] för din  [!DNL Analytics for Advertising] implementering.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Använda JavaScript-biblioteket [!DNL Last Event Service] med Adobe Experience Platform [!DNL Web SDK]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Om din organisation använder det äldre Adobe Analytics `visitorAPI.js`-biblioteket för datainsamling kan du växla till att använda [&#x200B; Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=sv-SE)-biblioteket (`alloy.js`), som gör att du kan interagera med de olika Experience Cloud-tjänsterna via [!DNL Edge Network].

JavaScript-biblioteket [!DNL Analytics for Advertising] [!DNL Last Event Service], i befintligt skick, registrerar händelserna view-through och click-through och sammanfogar dem till de associerade konverteringarna med ett extra ID (`SDID`). Biblioteket [!DNL Web SDK] har dock inte något [!DNL stitch ID]. Om du vill använda [!DNL Web SDK] för [!DNL Analytics for Advertising] måste du ändra 1) taggen [!DNL Last Event Service] som du använder på dina webbsidor och 2) dina [!DNL Web SDK] `sendEvent` -kommandon därefter.

## Steg 1: Redigera taggen [!DNL Last Event Service] för att generera en `[!DNL StitchID]`

I taggen [!DNL Analytics for Advertising] [!DNL Last Event Service] som du använder på dina webbsidor lägger du till kod för att generera `[!DNL StitchID]` med hjälp av den slumpmässiga ID-generatorn som paketeras i biblioteket.

**Äldre tagg:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Ny tagg:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Steg 2: Använd [!DNL Web SDK] för att skicka [!DNL StitchID] som XDM-data för [!DNL Analytics]

Infoga följande egenskap i ditt [!DNL Web SDK] `sendEvent`-kommando för att skicka [!DNL StitchID] till [!DNL Experience Edge] som [!DNL Experience Data Model] (XDM)-data för [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] använder värdet som `SDID`.

**Egenskap att lägga till:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exempel:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-kod för [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
