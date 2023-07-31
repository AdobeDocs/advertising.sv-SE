---
title: Skapa ett anpassat mål
description: Skapa ett anpassat mål
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 7ed95f58f317420e6c5104779ca95d081c717247
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Skapa ett anpassat mål

Du kan skapa anpassade mål som *mål* inom [!DNL Advertising Search, Social, & Commerce].

Om du vill skapa ett anpassat mål måste DSP vara länkat till ett [!DNL Search, Social, & Commerce] med samma Adobe Experience Cloud-organisations-ID, inifrån [!DNL Search, Social, & Commerce] klientinställningar. Om ditt DSP inte är länkat till en [!DNL Search, Social, & Commerce] ska du kontakta kontoteamet på Adobe.

>[!TIP]
>
>Se [bästa sättet att skapa anpassade mål](custom-goal-best-practices.md) för tips om hur du konfigurerar dina anpassade mål.

1. Logga in [!DNL Advertising Search, Social, & Commerce] at (användare i Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) eller (alla andra användare) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Kontrollera att mätvärdena du vill inkludera i ditt mål har spårats, att de är tillgängliga i produkten och att de innehåller ett visningsnamn:
   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. Leta reda på måtten och se till att **[!UICONTROL Show in UI and Reports]** är aktiverat för måttet.
   1. Om måttet inte har något värde i **[!UICONTROL Display Name]** kolumn, klicka i cellen, ange visningsnamnet och klicka sedan på **[!UICONTROL Apply].**
1. Skapa det anpassade målet som ett *mål*:
   1. Klicka på **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Klicka på i verktygsfältet **[!UICONTROL Create objective].**
   1. Ange målinställningarna:
      1. I **[!UICONTROL Change Objective Name]** anger du målnamnet.

         Målnamnet visas i [!UICONTROL Custom Goals] i DSP.

      1. Associera egenskaper med målet:

         >[!NOTE]
         >
         > Alla konverteringsmått som spåras för annonsören listas som standard i [!UICONTROL Available Properties] lista.

         * Om du vill importera en CSV-fil med konverteringsmått och deras vikt klickar du på **[!UICONTROL Import]** och leta reda på filen som ska importeras.

           De importerade konverteringsmåtten måste redan finnas för annonsören. Namnen är inte skiftlägeskänsliga.

           De importerade konverteringsmåtten ersätter befintliga egenskaper som angetts.

         * Om du vill ange det första konverteringsmåttet manuellt med standardvikten (1) väljer du i en lista över alla konverteringsmått som spåras för annonsören.

         * Om du vill lägga till ytterligare ett konverteringsmått manuellt med standardbredden (1) klickar du på **[!UICONTROL +]** .

           >[!TIP]
           >
           > Om du vill söka efter ett mått i listan anger du en sträng var som helst i måttets namn.

         * Om du vill lägga till flera konverteringsvärden manuellt klickar du på **[!UICONTROL Add Multiple Properties].** För varje konverteringsmått som du vill lägga till klickar du på måttnamnet i dialogrutan [!UICONTROL Available Properties] och dra den till [!UICONTROL Added Properties] kolumn. När du är klar med att lägga till mätvärden klickar du på **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Om du vill söka efter ett mått i listan anger du en sträng var som helst inom måttets namn i indatafältet.
           >* Välj alternativet om du vill filtrera listan så att den exkluderar mätvärden som exkluderas i rapporter **[!UICONTROL Hide properties excluded from reports].**

         * (När målet innehåller flera konverteringsmått) Om du vill ändra måttets vikt i förhållande till andra mått i målet anger du värden i **[!UICONTROL Weight]** fält.

      1. Klicka på längst ned i inställningarna **[!UICONTROL Save]**.

När du har skapat ett mål kan du tilldela det till ett DSP paket som ett anpassat mål när optimeringsmålet är[!UICONTROL Highest ROAS - Custom Goal]&quot; eller &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>För optimala prestanda måste de kombinerade mätvärdena i det anpassade målet (mål) innehålla minst tio konverteringar per dag. Om de inte gör det är det bästa sättet att lägga till ytterligare konverteringsmått, som produktsidor eller programstart, i målet. Se [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md) för riktlinjer.

>[!MORELIKETHIS]
>
>* [Om anpassade mål](custom-goal-about.md)
>* [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
