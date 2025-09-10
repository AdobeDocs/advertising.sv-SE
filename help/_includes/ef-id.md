---
source-git-commit: dede10acca1540a10699be3c14564a6f9360edd2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---
# Adobe Advertising EF ID:n

## Adobe Advertising EF ID:n

EF ID är en unik variabel som Adobe Advertising använder för att koppla aktivitet till en onlineklickning eller annonsexponering på den enskilda webbläsaren eller enheten. EF ID:n fungerar främst som nycklar för att skicka [!DNL Analytics]-data och Customer Journey Analytics-data till Adobe Advertising för rapportering och budoptimering inom Adobe Advertising.

För [!DNL Analytics] lagras EF-ID:t i dimensionen [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller [!DNL rVar] (reserverad [!DNL eVar]) (Adobe Advertising EF-ID).

För Customer Journey Analytics lagras EF-ID:t i egenskapen `trackingIdentities` för objektet `conversionDetails`, som är en del av [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

### EF ID-format {#ef-id-formats}

>[!NOTE]
>
>EF ID:n är skiftlägeskänsliga. Om en [!DNL Analytics]- eller Customer Journey Analytics-implementering tvingar URL-spårning till gemener, känner Adobe Advertising inte igen EF-ID:t. Detta påverkar Adobe Advertising budgivning och rapportering men påverkar inte Adobe Advertising rapportering inom [!DNL Analytics] eller Customer Journey Analytics.

#### [!DNL Google Ads] sökannonser

```
{gclid}:G:s
```

där:

* `gclid` är [!DNL Google Click ID] (GCLID).
* `s` är nätverkstypen (&quot;s&quot; för sökning).

#### [!DNL Microsoft Advertising] sökannonser

```
{msclkid}:G:s
```

där:

* `msclkid` är [!DNL Microsoft Click ID] (MSCLKID).
* `s` är nätverkstypen (&quot;s&quot; för sökning).

#### Visa annonser och sökannonser i andra sökmotorer

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

där:

* &lt;*Adobe Advertising besökar-ID*> är ett unikt ID per besökare (till exempel EhKVaAABCkJ0mDt). Kallas även *surfer-ID*.

* &lt;*timestamp*> är tiden i formatet YYYYMMDDHMMSS (till exempel 20190821192533 för År 2019, Month 08, Day 21, Time 19:25:33).

* &lt;*kanaltyp*> är den kanaltyp som ansvarar för klickningen eller exponeringen:

   * `d` för en klickning på en DSP-displayannons (visa klickfrekvens)
   * `i` om du vill se en visningsannons från DSP (visa-genomgång)
   * `s` om du vill ha en klickning på en sökannons (sökklickning).

Exempel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
