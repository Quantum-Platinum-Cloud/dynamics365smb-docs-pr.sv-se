---
title: Designdetaljer - Begreppet motkonto i korthet | Microsoft Docs
description: "Efterfrågan anges av ett företags kunder. Tillgång är det som företag kan skapa och ta bort för att fastställa saldo. Planeringssystemet börjar med den icke-härledda efterfrågan och spårar sedan tillbaka till tillgången."
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
ms.openlocfilehash: ffaa6b174d495b4a22423cabd13b74025db021ed
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-concept-of-balancing-in-brief"></a>Designdetaljer: Begreppet motkonto i korthet
Efterfrågan anges av ett företags kunder. Tillgång är det som företag kan skapa och ta bort för att fastställa saldo. Planeringssystemet börjar med den icke-härledda efterfrågan och spårar sedan tillbaka till tillgången.  
  
 Lagerprofilerna används för att innehålla information om efterfrågan och tillgång, antal och tidsplan. Dessa profiler utgör grunden för de två sidorna av den balanserande skalan.  
  
 Syftet med planläggningsmekanismen är att balansera efterfrågan och tillgång för en artikel för att se till att tillgång matchar efterfrågan på ett genomförbart sätt som definieras av planläggningsparametrar och regler.  
  
 ![](media/nav_app_supply_planning_2_balancing.png "NAV_APP_supply_planning_2_balancing")  
  
## <a name="see-also"></a>Se även  
 [Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
 [Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)