---
title: Skapa ett anpassat mål
description: Skapa ett anpassat mål
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 2060ab016917a69ef8bf718d339a35eb62b1269e
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Skapa ett anpassat mål

Du kan skapa anpassade mål som *mål* inom [!DNL Adobe Advertising Search].

Om du vill skapa ett anpassat mål måste DSP vara länkat till ett [!DNL Search] med samma Adobe Experience Cloud-organisations-ID, inifrån [!DNL Search] klientinställningar. Om ditt DSP inte är länkat till en [!DNL Search] konto, kontakta [!DNL Adobe] kontoteam.

>[!TIP]
>
>Se [bästa sättet att skapa anpassade mål](custom-goal-best-practices.md) för tips om hur du konfigurerar dina anpassade mål.

1. Logga in [!DNL Adobe Advertising Search] at (användare i Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) eller (alla andra användare) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Kontrollera att mätvärdena du vill inkludera i ditt mål har spårats, att de är tillgängliga i produkten och att de innehåller ett visningsnamn:
   1. På huvudmenyn klickar du på **[!UICONTROL Search]** > **[!UICONTROL Admin]>[!UICONTROL Transaction Properties]**.
   1. Leta reda på måtten och se till att **[!UICONTROL Show in UI and Reports]** är aktiverat för måttet.
   1. Om måttet inte har något värde i **[!UICONTROL Display Name]** kolumn, klicka i cellen, ange visningsnamnet och klicka sedan på **[!UICONTROL Apply].**
1. Skapa det anpassade målet som ett *mål*:
   1. På huvudmenyn klickar du på **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Klicka på i verktygsfältet **[!UICONTROL Create objective].**
   1. Ange målinställningarna:
      1. I **[!UICONTROL Change Objective Name]** anger du målnamnet.

         Målnamnet visas i [!UICONTROL Custom Goals] i DSP paketinställningar.

      1. Associera egenskaper med målet:

         >[!NOTE]
         >
         > Alla transaktionsegenskaper som spåras för annonsören listas som standard i [!UICONTROL Available Properties] lista.

         * Om du vill importera en CSV-fil med egenskaper och deras vikt klickar du på **[!UICONTROL Import]** och leta reda på filen som ska importeras.

            De importerade egenskaperna måste redan finnas för annonsören. namnen inte är skiftlägeskänsliga.

            De importerade egenskaperna ersätter alla befintliga egenskaper som har angetts.

         * Om du vill ange den första egenskapen manuellt med standardbredden (1) väljer du i en lista över alla transaktionsegenskaper som spåras för annonsören.

         * Om du vill lägga till en annan egenskap med standardbredden (1) manuellt klickar du på **[!UICONTROL +]** .

            >[!TIP]
            >
            > Om du vill söka efter en egenskap i listan anger du en sträng var som helst i egenskapsnamnet.

         * Om du vill lägga till flera egenskaper manuellt klickar du på **[!UICONTROL Add Multiple Properties].** För varje egenskap som du vill lägga till klickar du på egenskapsnamnet i dialogrutan [!UICONTROL Available Properties] och dra den till [!UICONTROL Added Properties] kolumn. När du är klar med att lägga till egenskaper klickar du på **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Om du vill söka efter en egenskap i listan anger du en sträng var som helst inom egenskapsnamnet i indatafältet.
            >* Om du vill filtrera listan så att den exkluderar egenskaper som har exkluderats i rapporter väljer du alternativet **[!UICONTROL Hide properties excluded from reports].**


         * (Om målet innehåller flera egenskaper) Om du vill ändra en egenskaps vikt i förhållande till de andra egenskaperna i målet anger du värden i **[!UICONTROL Weight]** fält.
      1. Klicka på längst ned i inställningarna **[!UICONTROL Save]**.


När du har skapat ett mål kan du tilldela det till ett DSP paket som ett anpassat mål när optimeringsmålet är[!UICONTROL Highest ROAS - Custom Goal]&quot; eller &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>För optimala prestanda måste de kombinerade mätvärdena i det anpassade målet (mål) innehålla minst tio konverteringar per dag. Om de inte gör det är det bästa sättet att lägga till ytterligare stödhändelser (transaktionsegenskaper), som produktsidor eller program som startar, i målet. Se [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md) för riktlinjer.

>[!MORELIKETHIS]
>
>* [Om anpassade mål](custom-goal-about.md)
>* [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)

