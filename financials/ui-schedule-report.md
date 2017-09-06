---
title: "Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs"
description: "Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, job queue
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0b97a5e48c4b339375ca9ad8cbe8388c5d47bb44
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="schedule-a-report-to-run"></a>Så här schemalägger du en rapportkörning
Du kan schemalägga en rapport att köras vid ett visst datum och tider. Planerade rapporter anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten. Om du väljer att spara rapporten till en fil skickas den bearbetade rapporten till området **Rapportinkorg**, på din startsida där du kan visa den.

Du kan schemalägga en rapport när du öppnar en rapport. Du väljer åtgärden **schema** och sedan anger du information som t.ex. skrivare och tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Om du har sparat den bearbetade rapporten till en fil, kommer den att vara tillgänglig i området **Rapportinkorg**.

## <a name="see-also"></a>Se även
[Ange skrivarval för rapporter](ui-specify-printer-selection-reports.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
