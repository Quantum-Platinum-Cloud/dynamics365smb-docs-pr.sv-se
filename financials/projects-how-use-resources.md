---
title: "Skapa och justera resursanvändning och priser | Microsoft Docs"
description: "Beskriver hur du kan registrera resursförbrukning eller förbrukning för ett projekt för att hålla reda på och hantera kostnader, priser och arbetstyper."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 48692c9837007c6dd9c3891f0940b6f15b1d6541
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Så här använder du resurser för projekt
Du registrerar förbrukning av resurser i projektjournalen för att hålla reda på kostnader, priser och de specifika projekttyper som är kopplade till projekt. Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).

Du kan även bokföra förbrukningen av en resurs i en resursjournal eller projektjournal. Transaktioner bokförda i resursjournaler påverkar inte redovisningen.

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Så här tilldelar du resurser till projekt
Du tilldelar resurser till projekt genom att skapa planeringsrader för projektet. Mer information finns i [Så här skapar du Projekt](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Registrera resursförbrukning för ett projekt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projektjournaler** och välj sedan relaterad länk.
2. Öppna den relevanta projektjournalen och fyll sedan i fälten som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## <a name="to-adjust-resource-prices"></a>Justera resurspriser
Om du vill ändra kostnader eller priser för många resurser på en gång kan du använda ett batch-jobb .  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Justera resurskost./-priser** och välj sedan relaterad länk.
2. Fyll i fälten på en rad efter behov och välj sedan knappen **OK**.

> [!NOTE]  
>   Batch-jobbet varken skapar eller justerar alternativa kostnader eller priser för resurser. Detta ändrar bara innehållet i fältet på resurskortet för fältet **Justeringsfält** som du har valt i batch-jobbet. Justeringarna börjar gälla direkt för resurser så kontrollera justeringsfaktorerna innan du kör batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Så här får du förslag till resursprisändringar enligt befintliga alternativa priser:
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursprisändringar** och välj sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (pris)** och fyll sedan i fälten efter behov.
3. Välj **OK**.  
4. När batch-jobbet har avslutats visar fönstret **Resursprisändringar** resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Så här får du förslag till resursprisändringar enligt standardpriser
Om du vill skapa flera alternativa resurspriser baserat på standardpriserna på resurskorten kan du använda ett batch-jobb .  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursprisändringar** och välj sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (res)** och fyll sedan i fälten efter behov.  
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Så här får du förslag till resursprisändringar baserat på alternativa priser
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. I rutan **Sök** anger du **Föreslå res.prisändring (pris)** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)     
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
