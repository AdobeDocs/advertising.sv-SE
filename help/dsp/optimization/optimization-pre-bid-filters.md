---
title: Pre-Bid-filter på placeringsnivå och Så här använder du dem
description: Referera till tillgängliga filter på placeringsnivå före köp och se hur du använder dem.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Pre-Bid-filter på placeringsnivå och Så här använder du dem

| Förköpsfilter | Beskrivning | När detta filter ska användas |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Ställer in ett minsta förutsägelsetröskelvärde för sannolikheten för att en auktion kan resultera i en klickfrekvens. Om du t.ex. anger tröskelvärdet till 0,1 % så lägger du bara bud på auktioner när den förväntade sannolikheten för ett klick är större än eller lika med 0,1 %.<br><br><b>Obs!</b> Filter används före optimeringsmål. Därför kan mycket strikta filter förhindra utgifter. | Använd när du har ett KPI-mål för klickfrekvens (CTR) och inte vill spendera budgeten när CTR ligger under tröskelvärdet. Det här filtret kan vara ganska restriktivt, så det är viktigt att ställa in realistiska mål. Beroende på andra placeringsbegränsningar är målet 0,03-,07 % vanligtvis en bra startpunkt. Ni kan optimera detta på webbplatsnivå efter behov för att förbättra mätvärdena.<br><br>Om ditt mål är att uppnå en lägsta CTR och bästa möjliga CPM, rekommenderas att du kombinerar ett [!UICONTROL Click Through Rate] -filter med optimeringsmålet [!UICONTROL Lowest CPM]. Om ditt mål är en maximal CPM utan någon verklig fördel för övertäckning och en minsta CTR kan det vara lämpligare att para ihop ett [!UICONTROL Click Through Rate]-filter med optimeringsmålet [!UICONTROL Always Max Bid + Highest CTR]. |
| [!UICONTROL 100% Completion Rate] | Anger en obligatorisk minsta slutförandehastighet som måste uppfyllas innan du lägger ett bud på ett intryck. | Använd det här filtret när kampanjens huvudmål är antalet slutförda aktiviteter. Faktor för andra målinriktningsparametrar, men 65 % är den rekommenderade startprocenten. |
| [!UICONTROL Player Size - Adobe] | Anger en nödvändig minsta spelarstorlek med data från DSP. Du kan lägga ett bud på ett intryck när tröskelvärdet [!UICONTROL Player Size] har uppnåtts. | Används för att säkerställa att ni levererar ett komplett spelarlager med data från DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Anger en obligatorisk minsta spelarstorlek, med data från [!DNL Moat] eller [!DNL Integral Ad Science] ([!DNL IAS]). Du kan lägga ett bud på ett intryck när tröskelvärdet [!UICONTROL Player Size] har uppnåtts. | Används för att säkerställa att du levererar på ett fullständigt spelarlager med plattformstäckande [!DNL Moat]- eller [!DNL IAS]-data.<br><br><b>Obs!</b> Använd bara det här filtret när kampanjen har konfigurerats att använda [!DNL Moat] - eller [!DNL IAS]-data. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Anger en obligatorisk minsta visningsprocent, med DSP visningsvärden och mått. Du kan lägga bud på ett intryck när det angivna tröskelvärdet är uppfyllt.<br><br><b>Anteckningar:</b><ul><li>Om kampanjens [!UICONTROL Viewability Sensitivity]-inställning är [!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)] används visningsstandarden [!DNL Media Rating Council] (MRC) för kampanjen. Om inställningen [!UICONTROL Viewability Sensitivity] är [!UICONTROL Strict (100% of ad in view & audio on for 50% duration)] används visningsstandarden [!DNL GroupM] för kampanjen.</li><li>Måttdefinitioner för Adobe skiljer sig från definitioner från andra tillverkare, så det kan finnas små skillnader med data från tredje part.</li></ul> | Det bästa sättet är att matcha optimeringsmålet och eventuella filterinställningar före bud med kampanjens [!UICONTROL Viewability Sensitivity]-inställning. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Så här optimerar DSP era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
