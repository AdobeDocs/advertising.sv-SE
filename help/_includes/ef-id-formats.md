---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---
# Adobe Advertising EF ID:n

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
