---
title: Inställningar för rapportmål
description: Se informationen som krävs för rapportdestinationer, per måltyp.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Inställningar för rapportmål

Vilken information som krävs för rapportdestinationer som inte är e-postrapporter varierar beroende på måltyp.

>[!NOTE]
>
> Du kan också leverera anpassade rapporter till e-postmottagare som inte behöver ha något sparat rapportmål. Du kan ange e-postmottagare i stället för sparade mål i rapportinställningarna.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Ett namn som hjälper dig att identifiera målet.

**[!UICONTROL S3 Bucket URL]:** Den fullständiga sökvägen till mappen på det [!DNL Amazon Simple Storage Service] (S3)-paket som rapporten överförs till. Exempel: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** Åtkomstnyckel-ID till ([!DNL Amazon S3])-bucket (tillhandahålls av [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Nyckeln för hemlig åtkomst till ([!DNL Amazon S3])-bucket (tillhandahålls av [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Ett namn som hjälper dig att identifiera målet.

**[!UICONTROL Server]:** Serverns värdnamn.

**[!UICONTROL Port]:** Portnumret som ska användas på servern. Standardvärdet är *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Användarnamnet som ska loggas in på servern.

**[!UICONTROL Password]:** Lösenordet för att logga in på servern.

**[!UICONTROL Path (Optional)]:** Serversökvägen som filerna överförs till.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Ett namn som hjälper dig att identifiera målet.

**[!UICONTROL Server]:** Serverns värdnamn.

**[!UICONTROL Port]:** Portnumret som ska användas på servern. Standardvärdet är *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Användarnamnet som ska loggas in på servern.

**[!UICONTROL Password]:** Lösenordet för att logga in på servern.

**[!UICONTROL Path (Optional)]:** Serversökvägen som filerna överförs till.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Ett namn som hjälper dig att identifiera målet.

**[!UICONTROL Server]:** Serverns värdnamn.

**[!UICONTROL Port]:** Portnumret som ska användas på servern. Standardvärdet är *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Användarnamnet som ska loggas in på servern.

**[!UICONTROL Password]:** Lösenordet för att logga in på servern.

**[!UICONTROL Path (Optional)]:** Serversökvägen som filerna överförs till.

>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Skapa en [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Redigera en [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Ta bort en [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
