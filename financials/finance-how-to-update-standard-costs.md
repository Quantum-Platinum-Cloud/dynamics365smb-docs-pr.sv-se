---
title: "Så här kan du uppdatera standardkostnader | Microsoft Docs"
description: "Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 57da88de6a3bbb22cea7c12a2b579206ca5d7766
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-update-standard-costs"></a>Så här kan du uppdatera standardkostnader
Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln. Processen består typiskt av följande fyra steg:  

1.  Uppdatera kostnader på komponent- och kapacitetsnivå. Mer information finns i batch-jobbet **Föreslå artikelstandardkostnad**.  
2.  Konsolidera och summera komponent- och kapacitetskostnader för att beräkna den totala produktions- eller monteringskostnaden för artiklarna.  
3.  Använd standardkostnaderna som angavs när du körde de föregående batch-jobben. Standardkostnaderna börjar inte gälla förrän de implementeras. Mer information finns i Implementera standardkostnadsändringar.  
4.  Inför ändringarna för att uppdatera fältet **Styckkostnad** för artikelkortet och utföra lageromvärderingen. Mer information finns i [Så här omvärderar du lager](inventory-how-revalue-inventory.md).  

Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Uppdatera standardkostnader  
1.  Kör batch-jobbet **Justera kost. - artikeltrans.**  
2.  Kör batch-jobbet **Bokför lagerkostnad i redov.**  
3.  Öppna **Standardkostnadsformulär** och använd en eller flera av följande funktioner:  

    1.  Kör batch-jobbet **Föreslå artikelstandardkostnad**.  
    2.  Granska resultaten och gör nödvändiga ändringar.  
    3.  Kör batch-jobbet **Föreslå standardkostnad för kapacitet**.  
    4.  Granska resultaten och gör nödvändiga ändringar.
    5. Kör batch-jobbet **Uppsummerad standardkostnad**.
    6.  Granska resultaten och gör nödvändiga ändringar.
    7.  Kör batch-jobbet **Implementera standardkostnadsändringar**.  
4.  Granska och bokför fönstret  **Omvärderingsjournal** , vilken har fyllts på med transaktioner från föregående steg i den här processen.  

## <a name="see-also"></a>Se även  
 [Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md)   
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md) [[Finans](finance.md)]  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
