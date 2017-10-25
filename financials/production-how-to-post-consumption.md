---
title: "Så här: batch-bokföra förbrukning | Microsoft Docs"
description: "Om bokföringsmetoden är **manuell** måste du bokföra komponenterna manuellt med hjälp av förbrukningsjournalerna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a>Så här: batch-bokföra förbrukning
Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.

Du kan också ställa in systemet att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder. Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Om du vill bokföra förbrukning för produktion av en eller flera rader  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Förbrukningsjournal** och välj sedan relaterad länk.  
2.  Fyll i fälten med data om produktionsorden och om förbrukningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Om distributionslagret där komponenterna lagras har konfigurerats till att använda lagerplatser men inte kräva bearbetning av plockning, kopplar du en lagerplatskod till journalraden för att ange var artiklarna ska tas från i distributionslagret. Mer information finnsi [Så här: Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).  
3.  Välj åtgärden **Bokför** om du vill bokföra förbrukningen. De associerade artikeltransaktionerna misnkas.

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
