---
title: "Hur du arkiverar försäljnings- och inköpsdokument | Microsoft Docs"
description: "Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Arkivera dokument
Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från.

## <a name="to-set-up-automatic-document-archiving"></a>Så här ställer du in automatisk dokumentarkivering  
Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder innan du tar bort dokument.

Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument. Momenten är liknande för en inköpsorder.
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. I fönstret **Försäljnings- och kundfordringsinställningar** fyller du fälten enligt följande:

|Fält|Description|
|-----|-----------|
|**Arkivering av försäljningsofferter**|**Aldrig** om du aldrig vill arkivera försäljningsofferter när de tas bort. **Fråga** för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort. **Alltid** om du vill arkivera försäljningsofferter automatiskt när de tas bort.|
|**Arkivera avropsorder för försäljning**|Välj detta alternativ om du vill arkivera avropsorder automatiskt när de tas bort.|
|**Arkivera inköpsorder och inköpsreturorder**|Välj detta alternativ om du vill arkivera försäljningsorder automatiskt när de tas bort.|

## <a name="to-archive-a-sales-order"></a>För att arkivera en försäljningsorder
Följande förfarande beskriver hur du arkiverar en försäljningsorder. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Öppna en försäljningsorder som du vill arkivera.  
3.  Välj åtgärden **Arkivera dokument**.

Försäljningsordern arkiveras. Du kan visa den i fönstret **Arkiverade försäljningsorder**. Härifrån kan du också använda den för att återskapa den försäljningsorder som den arkiverades från.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Återskapa en försäljningsorder från arkivet
Följande förfarande beskriver hur du återskapar en försäljningsorder. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arkiverade försäljningsorder** och välj sedan relaterad länk.
2.  Markera den arkiverade försäljningsorder som du vill återskapa och välj sedan åtgärden **Återskapa**.  

Försäljningsordern skapas och läggs till i fönstret **Försäljningsorder**.

## <a name="to-delete-archived-sales-orders"></a>Ta bort arkiverade förs.orderversioner
Följande förfarande beskriver hur du tar bort arkiverade försäljningsorder. Stegen är liknande för andra arkiverade försäljnings- och inköpsdokument.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ta bort arkiverade försäljningsorderversioner** och välj sedan relaterad länk.  
2.  I fönstret **Ta bort arkiverade försäljningsorderversioner** väljer du lämpliga filter.  
3.  Välj knappen **OK**.

## <a name="see-also"></a>Se även
[Spåra dokumentrader](across-how-to-track-document-lines.md)  
[Försäljning](sales-manage-sales.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
