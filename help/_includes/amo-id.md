---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO-ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för dataklassificering av [!DNL Analytics] och Customer Journey Analytics samt för inmatning av reklamstatistik (som visningar, klick och kostnader) från Adobe Advertising.

För [!DNL Analytics] lagras AMO-ID:t i en [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=sv-SE) - eller rVar-dimension (AMO-ID).

För Customer Journey Analytics lagras AMO-ID:t i egenskapen `trackingCode` för objektet `conversionDetails`, som är en del av [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

AMO-ID:t kallas även `s_kwcid`, som ibland uttalas som [!DNL squid].
