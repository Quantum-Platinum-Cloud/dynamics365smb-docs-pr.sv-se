---
title: "Så här: ställa in status för serviceorder och reparationer | Microsoft Docs"
description: "Du måste ställa in nio olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bc804db29ec89904101f48b625770f730abb13d9
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Ställ in status för serviceorder och reparationer
Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider. Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.  

Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus. Det finns fyra prioriteter: Hög, medelhög, medellåg och låg.  
  
När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status. Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen. Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.  

## <a name="to-set-up-a-repair-status"></a>Så här skapar du en reparationsstatus  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Reparationsstatus** och välj sedan relaterad länk. 2. Skapa en ny reparationsstatus.  
3. Fyll i fälten **Kod** och **Beskrivning**.  
4. I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till. Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.  
5. Välj en reparationsstatus Du kan bara välja en.  
6. Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.  
7. Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.  
8. Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.
  
## <a name="to-set-up-service-status-priorities"></a>Så här skapar du servicestatusprioriteter  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Tjänsteorderstatus** och välj sedan relaterad länk.  
2. Välj den serviceorderstatus som du vill ange prioritet för.  
3. I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus. Upprepa det här steget för varje status.  
  
## <a name="see-also"></a>Se även  
[Förstå serviceorderstatus och reparationsstatus]()  
[Ställa in tjänstehantering](service-setup-service.md)  
