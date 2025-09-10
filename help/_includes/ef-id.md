---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# Adobe Advertising EF ID:n

EF ID är en unik variabel som Adobe Advertising använder för att koppla aktivitet till en onlineklickning eller annonsexponering på den enskilda webbläsaren eller enheten. EF ID:n fungerar främst som nycklar för att skicka [!DNL Analytics]-data och Customer Journey Analytics-data till Adobe Advertising för rapportering och budoptimering inom Adobe Advertising.

För [!DNL Analytics] lagras EF-ID:t i dimensionen [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=sv-SE) eller [!DNL rVar] (reserverad [!DNL eVar]) (Adobe Advertising EF-ID).

För Customer Journey Analytics lagras EF-ID:t i egenskapen `trackingIdentities` för objektet `conversionDetails`, som är en del av [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].
