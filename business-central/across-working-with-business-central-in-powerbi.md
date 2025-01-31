---
title: Arbeta med Business Central-data i Power BI| Microsoft Docs
description: 'Använda insikter, business intelligence och KPI:er från dina Business Central-data med hjälp av Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2022
ms.author: jswymer
---
# <a name="work-with-include-prodshortincludesprodshortmd-data-in-power-bi" />Arbeta med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI

I denna artikel lär du dig det grundläggande inom att arbeta med rapporter och instrumentpaneler i Power BI som använder [!INCLUDE [prod_short](includes/prod_short.md)] som datakälla. Artikeln beskriver vissa aspekter som hjälper dig komma igång som [!INCLUDE[prod_short](includes/prod_short.md)]-användare. För allmänna instruktioner och riktlinjer för hur du använder Power BI, se [Power BI-dokumentation för konsumenter](/power-bi/consumer).

## <a name="get-ready" />Gör dig redo

Registrera dig frö Power BI-tjänsten. Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) om du inte redan har registrerat dig. När du registrerar dig använder du en e-postadress för arbetet samt ett lösenord.

## <a name="get-started" />Kom igång

När du väl har ett Power BI-konto kan du logga in på [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI-tjänsten utgör värd för samtliga dina tillgängliga rapporter. Välj **Min arbetsyta** > **Rapporter** för att visa rapporten. Välj sedan helt enkelt den rapport som du vill visa.

Med [!INCLUDE[prod_short](includes/prod_short.md)] online får du automatiskt en uppsättning standardrapporter på din arbetsyta. Om du vill skapa dina egna rapporter kan du använda Power BI Desktop för att skapa rapporterna och sedan publicera dem på din arbetsyta. Mer information finns i [Komma igång med att skapa rapporter i Power BI Desktop för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du börja från grunden genom att använda Power BI Desktop. Som tillval kan Power BI-rapporter distribueras som uppladdningsbara filer.

## <a name="get-the-latest-data" />Hämta senaste data

Varje enskild Power BI-rapport baseras på en datauppsättning som hämtar data från [!INCLUDE[prod_short](includes/prod_short.md)]-källorna. D måste se till att datan i dina Power BI-rapporter motsvarar datan i [!INCLUDE[prod_short](includes/prod_short.md)]. Detta koncept kallas *uppdatering*.  Uppdatering kanske inte sker automatiskt beroende på hur din organisation har konfigurerat Power BI. Du kan uppdatera data på två sätt: manuellt eller genom att schemalägga en uppdatering. Manuell uppdatering sker på begäran och vid behov. Schemalagd uppdatering utför uppdatering vid förvalda tidsintervall.

### <a name="refresh-manually" />Manuell uppdatering

I navigeringsfönstret, under **Datauppsättningar**, väljer du **Fler alternativ (...)** bredvid datauppsättningen och sedan **Uppdatera nu**.

### <a name="schedule-a-refresh" />Schemalägga en uppdatering

I navigeringsfönstret, under Datauppsättningar, väljer du Fler alternativ (...) bredvid datauppsättningen och sedan **Schemalägg uppdatering**. Fyll i informationen under avsnittet **Schemalägg uppdatering** och välj sedan **Verkställ**.

Mer information finns i [Konfigurera schemalagd uppdatering](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="a-nameuploadaupload-reports-from-files" /><a name="upload"></a>Ladda upp rapporter från filer

Power BI-rapporter kan distribueras bland användarna som .pbix-filer. Om du har en .pbix-fil kan du ladda upp filen till en arbetsyta. Om du vill ladda upp en rapport gör du följande:

1. Välj **Hämta data** på din nya arbetsyta.

2. I rutan Filer väljer du **Hämta**.

3. Välj **Lokal fil**, navigera till platsen där du sparade filen och välj sedan **Öppna**.

Mer information finns i [Ladda upp rapporten till tjänsten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> För att kunna ladda upp rapporten måste du ha en arbetsyta med [Premium-kapacitet](/power-bi/service-premium-what-is). Mer information finns i [Hantera Premium-kapaciteter](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] online kan du också ladda upp en rapport inifrån [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Arbeta med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)] – Ladda upp rapporter](across-working-with-powerbi.md#upload).

## <a name="a-nameshareashare-reports-with-others" /><a name="share"></a>Dela rapporter med andra

När en rapport väl finns på din arbetsyta kan du dela den med andra i din organisation.

Om du vill dela en rapport väljer du **Dela** i en listrapport eller en öppen rapport. I fönstret **Dela rapport** anger du den fullständiga e-postadressen till de individer eller distributionsgrupper som du vill dela med. Följ instruktionerna på skärmen för att slutföra delningen. Mer information finns i [Sela en instrumentpanel eller rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Du och de personer du delar med måste ha en [Power BI Pro-licens](/power-bi/service-features-license-type). Innehållet måste ligga på en arbetsyta med [Premium-kapacitet](/power-bi/service-premium-what-is). Mer information finns i [Så här delar du ditt arbete i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se även

[Business Central och Power BI](admin-powerbi.md)  
[Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeta med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-powerbi.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
