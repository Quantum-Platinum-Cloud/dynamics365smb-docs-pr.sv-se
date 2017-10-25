---
title: Designdetaljer - Order | Microsoft Docs
description: "Det här avsnittet innehåller information om order-till-order-länkar i en tillverka-mot-order-miljö."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 24f5c56e9e148128d83593757d820fa62686403e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-order"></a>Designdetaljer: Order
I tillverka-mot-order-miljö köps en artikel in eller produceras för att exklusivt täcka en viss efterfrågan. Vanligtvis gäller det A-artiklar och motiveringen för att välja partiformningsmetoden Order kan vara att efterfrågan är ovanlig, ledtiden är oansenlig eller de obligatoriska attributen varierar.  
  
Programmet skapar order-till-order-länk som fungerar som ett preliminärt samband mellan tillgången, en leveransorder eller lagret och efterfrågan som ska uppfyllas.  
  
Förutom att använda orderprincipen kan order-till-order-kopplingen användas på följande sätt vid planeringen:  
  
* När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder).  
* När du använder funktionen Försäljningsorderplanering för att skapa en produktionsorder från en försäljningsorder.  
  
Även om ett produktionsföretag anser sig vara en miljö som tillverkar mot order, kan det vara bra att använda en partiformningsmetod av typen Parti-för-parti om artiklarna är standardartiklar med attribut utan variation. Det medför att systemet använder oplanerat lager och endast ackumulerar försäljningsorder med samma utleveransdatum eller inom en definierad tidsenhet.  
  
## <a name="order-to-order-links-and-past-due-dates"></a>Order-till-order-länkar och utgångna förfallodatum  
Till skillnad från de flesta uppsättningar med tillgång-efterfrågan planeras länkade order med förfallodatum före planeringsstartdatumet helt automatiskt. Affärsorsaken till undantaget är att de specifika uppsättningarna med efterfrågan-tillgång måste synkroniseras till körning. För mer information om den frysta zonen som gäller de flesta typerna av efterfrågan-tillgång, se [Designdetaljer: Hantera order före planeringsstartdatumet](design-details-dealing-with-orders-before-the-planning-starting-date.md).  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)