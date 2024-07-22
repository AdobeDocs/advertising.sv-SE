---
title: Manuella inställningar för avtal-ID
description: Se beskrivningar av inställningarna för manuellt angivna avtal-ID.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Manuella inställningar för avtal-ID

| Avsnitt | Parameter | Beskrivning | Obligatoriskt | Redigerbar |
|---------|-----------|-------------|----------|----------|
| [Avtalsinformation] | [!UICONTROL Deal name] | Namnet som identifierar din [!UICONTROL Deal ID] i Advertising DSP. Ange ett namn eller välj **[!UICONTROL Auto-name]** för att låta DSP generera ett namn baserat på avtalsinformationen.<br><br>Exempel på ett automatiskt genererat namn: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
| | [!UICONTROL External deal ID] | Det ID som din utgivare och SSP använder för att identifiera erbjudandet. | Ja | Nej |
| | [!UICONTROL Publisher] | Namnet på utgivaren som säljer det här lagret. | Ja | Nej |
| | [!UICONTROL SSP] | Den SSP-plattform som avtalet löper genom. | Ja | Nej |
| | [!UICONTROL Media type] | Den typ av media som köpts genom det här erbjudandet: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* eller *[!UICONTROL Publisher Managed]*. Alternativen varierar beroende på SSP.<br><br> Om avtalet tillåter flera medietyper väljer du medietypen för standardplaceringen när du skapar erbjudandet. Senare kan du ändra värdet eller bara [bifoga en ny placering med den extra medietypen](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nej |
| | [!UICONTROL Deal type] | Avtalsåtagande och prisstruktur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Du och utgivaren har inte implementerat ett fast antal visningsleveranser. I avtalet anges minimipriset för lagret, men CPM kan variera och öka beroende på marknadsvillkoren.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Du och utgivaren har inte implementerat ett fast antal visningsleveranser. Priserna sätts till en förhandlad fast ränta.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Du och utgivaren har kommit överens om ett fördefinierat antal visningar, målinriktning, flygdatum och fast pris.<br><br><b>Obs!</b> Garanterade erbjudanden kräver flygdatum och ett visst antal visningar i avsnittet [!UICONTROL Tracking]. Du måste också skapa en standardplacering av en programmatisk garanterad (PG) för erbjudandet, och du kan välja att använda erbjudandet för andra placeringar i stället.</li></ul> | Ja | Nej |
| | [!UICONTROL CPM] | Förhandlingskostnaden per 1 000 visningar (CPM). | Ja | Ja |
| | [Valuta] | Valutan för erbjudandet.<br><br>Alla SSP accepterar erbjudanden i USD. När SSP godkänner valutan för ditt DSP är även den valutan tillgänglig. | Ja | Nej |
| | [!UICONTROL Billing method] | Alla kontrakt-ID:n är [!DNL Adobe]-finansierade och fakturerade. DSP betalar alla tillgängliga medieleverantörer baserat på användning, hanterar avvikelser med leverantörerna och skickar en konsoliderad faktura till kontot. Det här alternativet medför ytterligare avgifter enligt kontots rabattkort. | Ja | Nej |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | E-postadressen till det användarkonto som har åtkomst till avtalet. | Nej | Ja |
| | [!UICONTROL Advertisers that can access this deal] | De specifika annonsörer på kontot som har tillgång till erbjudandet.<br><br><b>Obs!</b> Du kan dela erbjudandet med annonsörer i ytterligare konton från vyn [!UICONTROL Deals]. Klicka på **[!UICONTROL #]** på avtalsraden, klicka på **[!UICONTROL share]** och dela sedan avtalet med en e-postadress. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Start- och slutdatum för trafik som använder det här avtalet. Datumen är avsedda endast för spårning och påverkar inte annonsleveransen.<br><br><b>Tips!</b> I vyn [!UICONTROL Inventory] > [!UICONTROL Deals] visar kolumnen [!UICONTROL Pacing & Budget] hur erbjudandet matchar det angivna flygdatumet och det angivna visningsmålet. Om leveransen är under- eller överbelagd kontaktar du utgivaren för att justera hur mycket av volymen den skickar genom erbjudandet. | Garanterade erbjudanden: Ja<br>Erbjudanden utan garanti: Nej | Ja |
| | [!UICONTROL Impressions] | (Valfritt för erbjudanden utan garanti) Det uppskattade antalet visningar som du förväntar dig att göra med det här erbjudandet. Detta värde är endast till för spårningsändamål. Utgivaren kontrollerar och levererar. | Garanterade erbjudanden: Ja<br>Erbjudanden utan garanti: Nej | Ja |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Skapa information om avtal-ID manuellt](deal-id-create.md)
>* [SSP-partners](ssp-partners.md)
>* [Om privat lager](private-inventory-about.md)
