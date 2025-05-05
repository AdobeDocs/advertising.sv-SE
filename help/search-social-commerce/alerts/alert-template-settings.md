---
title: Anpassade inställningar för aviseringsmall
description: Läs mer om inställningarna för anpassade varningsmallar.
exl-id: c9cff26b-e6be-4dad-ac3a-b5a53387c4e6
feature: Search Alerts
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 0%

---

# Anpassade inställningar för aviseringsmall

| Tabb | Parameter | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | Datumintervallet för vilket du vill utvärdera villkoren för aviseringen. Mätvärden utvärderas i sammanställning över datumintervallet. Alternativen varierar från *[!UICONTROL Yesterday]* till *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | Villkoren för att utlösa aviseringen vid den tidpunkt som anges på fliken [!UICONTROL Scheduling and Delivery]. De tillgängliga kolumnerna varierar beroende på enhetstyp (till exempel kampanj eller nyckelord). Alla filter förenas med den booleska funktionen AND, vilket innebär att alla angivna villkor måste uppfyllas.<ul><li><p>Om du vill lägga till ett filter klickar du på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid ![Lägg till](/help/search-social-commerce/assets/add.png "Lägg till") **[!UICONTROL ADD FILTER]** och gör sedan följande:</p></li><ol><li><p>(Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i indatafältet **[!UICONTROL ADD FILTER]**.</p></li><li><p>Välj ett kolumnnamn på kolumnmenyn.</p></li><li><p>Definiera filtret i kolumnen:</p></li><ul><li><p>(Filter utan inmatningsfält) Klicka på ![nedpilen](/help/search-social-commerce/assets/arrow-down-expand.png "nedpilen") bredvid den andra menyn och markera sedan kryssrutorna intill varje värde som ska inkluderas.</p></li><li><p>(Måttkolumner som du vill spåra ökningar eller minskningar av värden för mellan det angivna datumintervallet och föregående period) För operatorn väljer du *ökningar med* eller *minskningar med* och anger sedan tröskelvärdet.</p><p>Om du till exempel har valt kolumnen [!UICONTROL Cost] och vill få ett varningsmeddelande när kostnaden för en kampanj ökar med 21 %, väljer du [!UICONTROL increases by] och anger 21 i indatafältet. I fältet [!UICONTROL Date Comparison Format] anger du att du är intresserad av en ändring i procent (i stället för en ändring i valutaenheter).</p><p>När du väljer det här alternativet läggs ytterligare två kolumner till för varje vanlig datakolumn. I stället för att ta med bara en kolumn för&quot;Clicks&quot;, innehåller rapporten kolumner för&quot;Clicks R1&quot; (för Range 1)&quot;Clicks R2&quot; (för Range 2) och antingen&quot;Clicks Diff&quot; eller&quot;ClicksDiff (%)&quot; beroende på angiven [!UICONTROL Date Comparison Format] (se nedan).</p><p>**Anteckningar:**</p><ul><li><p>Skillnadskolumnen är inte ifylld för härledda mått.<p></li><li><p>Den här funktionen är inte tillgänglig för kolumnerna för konverteringsmått, ID eller etikettklassificering.</p></li><li><p>Rapporter som jämför stora datumintervall kan ta längre tid att generera.</p></li></ul></ul><li><p>(Alla andra filter med indatafält) Välj en operator på den andra menyn och ange sedan det tillämpliga värdet.</p><p>Om du t.ex. har markerat kolumnen&quot;Klickningar&quot; och bara vill returnera rader med fler än 100 klick, väljer du&quot;större än&quot; och anger 100 i indatafältet.</p><p>Beroende på datatypen kan tillgängliga operatorer innehålla <i>större än</i>, <i>mindre än</i>, <i>lika</i>, <i>innehåller</i>, <i>inte innehåller</i>, <i>börjar med</i>, <i>slutar med</i>, <i>inget värde</i>, <i>&rbrace;har värdet </i>, <i>före</i>, <i>efter</i> eller <i>inget datum</i>.</p><p>**Obs!** Textvärden är inte skiftlägeskänsliga. Om du till exempel filtrerar efter kampanjer med&quot;lån&quot; i namnet kan resultatet vara&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.</p></li></ol><li><p>Om du vill ta bort ett filter klickar du på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort") bredvid filterdefinitionen.</p></li></ul> |
|  | [!UICONTROL Comparing] | (Tillgängligt när varningsspåren ökar eller minskar i en eller flera måttkolumner, skrivskyddat) De två datumintervall som data jämförs för. |
|  | [!UICONTROL Date Comparison Format] | (Tillgängligt när varningsspåren ökar eller minskar i en eller flera måttkolumner) Hur du uttrycker skillnaden mellan data i de två datumintervallen:<ul><li><p><i>[!UICONTROL Variance]</i> (standard) - Visar skillnaden som ett numeriskt värde.</p></li><li><p><i>[!UICONTROL % Change]</i> — Visar skillnaden i procent.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | Varningsnamnet. Den måste innehålla minst fem tecken. |
|  | [!UICONTROL Trigger this Alert] [when] | Hur ofta varningen söker efter angivna villkorsfilter och skickar e-postmeddelanden när alla villkor är uppfyllda:<ul><li><p>[!UICONTROL Daily at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AM|PM]]</p></li></ul>**Obs!** Detta värde påverkar inte utvärderingsperioden. |
|  | [!UICONTROL Email Recipients] | (Kan endast redigeras av den som skapat aviseringsmallen, skrivskyddat för alla andra) E-postadresser som du kan använda för att skicka meddelanden när en avisering skapas. Som standard anges adressen till mallskaparen.<br><br>Om du vill lägga till en adress anger du adressen och klickar sedan på **[!UICONTROL Add]**. Om du vill ange flera adresser avgränsar du dem med kommatecken eller mellanslag, eller lägger till dem separat.<br><br>När aviseringen innehåller upp till 1 000 poster bifogas en CSV-version av aviseringen till e-postmeddelandet. |

>[!MORELIKETHIS]
>
>* [Om anpassade aviseringar](alert-about.md)
>* [Skapa en anpassad aviseringsmall](alert-template-create.md)
>* [Redigera en anpassad aviseringsmall](alert-template-edit.md)
>* [Pausa en anpassad aviseringsmall](alert-template-pause.md)
>* [Aktivera en anpassad aviseringsmall](alert-template-activate.md)
>* [Ta bort en anpassad aviseringsmall](alert-template-delete.md)
>* [Visa anpassade aviseringar](alert-view.md)
>* [Exportera data för anpassade aviseringar](alert-export-data.md)
