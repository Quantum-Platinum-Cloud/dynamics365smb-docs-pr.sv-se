---
title: Konfigurera produktionsprocesser | Microsoft Docs
description: "För att material ska kunna omvandlas till tillverkade slutartiklar måste produktionsresurser som t.ex. strukturer, verksamhetsföljder, maskinoperatörer och maskiner ställas in i systemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2419755f5788eb7cb8ed464ac97fccd7e63e795c
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-manufacturing"></a>Ställa in Produktion
För att material ska kunna omvandlas till tillverkade slutartiklar måste produktionsresurser som t.ex. strukturer, verksamhetsföljder, maskinoperatörer och maskiner ställas in i systemet.

I systemet representeras operatörer och maskiner som maskingrupper, vilka i sin tur kan organiseras i produktionsgrupper. När dessa resurser upprättats kan de laddas med operationer enligt den material- (struktur) och processtruktur (verksamhetsföljd) som definierats för artikeln samt utifrån maskin- eller produktionsgruppens kapacitet. Du kan även ställa in produktionskapaciteten för varje resurs. Kapaciteten definieras av den arbetstid som finns tillgänglig i maskin- och produktionsgrupperna, och den styrs av kalendrar på alla nivåer. I en produktionsgruppkalender anges de arbetsdagar/arbetstimmar, skift, helgdagar och frånvaro som avgör den tillgängliga bruttokapaciteten (och som vanligtvis mäts i minuter). Allt detta avgörs utifrån de effektivitets- och kapacitetsvärden som har definierats.  

När du har lagt upp produktion kan du planera och utföra produktionsorder. Mer information finns i [Planering](production-planning.md) och [Produktion](production-manage-manufacturing.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Konfigurera produktionsfunktionerna, till exempel definiera arbetstimmar för en fabrik eller välja planeringsprinciper.|Sidan **Produktionsinställningar**.|  
|Definiera en standardarbetsvecka i modulen Produktion med start- och sluttider för varje arbetsdag samt tillhörande arbetsskiften.|[Skapa fabrikskalendrar](production-how-to-create-work-center-calendars.md)|  
|Organisera fasta värden och krav för produktionsresurser som t.ex. produktionsgrupper eller maskingrupper till att styra deras tillverkningsutflöde i maskingruppen.|[Ställa in produktionsgrupper och maskingrupper](production-how-to-set-up-work-and-machine-centers.md)|
|Ordna produktionsoperationer i krävd ordningen och tilldela dem till produktions- eller maskingrupper med nödvändiga arbetstider.|[Skapa verksamhetsföljder](production-how-to-create-routings.md)|
|Ordna produktionskomponenter eller underenheter under en producerad artikel och godkänn strukturlistan utförs vid produktionsgrupper.|[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)|
|Kontrollera att rätt komponentkvantitet är tillgänglig när tillverkade artiklar lagerförs med en enhet men tillverkas med en annan.|[Arbeta med måttenheter för produktionsbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definiera familjer av produktionsartiklar som har liknande produktionsprocesser för att minska förbrukning. Till exempel kan fyra enheter av en artikel produceras av ett ark och tio enheter av en annan artikel av samma ark.|[Arbeta med produktionsfamiljer](production-how-work-family.md)|
|Använd standarduppgifter om du vill förenkla verksamhetsföljder genom att snabbt lägga till extra information för återkommande transaktioner.|[Skapa standardverksamhetsföljdrader](production-how-set-up-standard-routing-lines.md)|  
|Förbered produktionsgrupper och verksamhetsföljder för att representera legotillverkning.|[Lägga ut legotillverkning för produktion](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Se även
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
