---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks skrivbord till Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Tillägget QuickBooks datamigrering för Dynamics 365 for Financials
Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad installation för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Mer information finns i [Importera företagsdata från ett annat finanssystem](upload-data.md).

## <a name="exporting-data-from-quickbooks"></a>Exportera data från QuickBooks
Du måste ha exporterat en del eller alla av dina befintliga kunder, leverantörer, lagerartiklar och konton till en Intuit Interchange Format-fil (IIF ). Tillägget QuickBooks datamigrering innehåller en standardmappning avQuickBooks data så att du kan använda dina befintliga data för att testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget. Standardmappningen ska vara tillräcklig i de flesta fall, men du kan ändra mappningen i guiden för assisterad installation.  
I QuickBooks innehåller arkiv-menyn verktyg till exportlistor. För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande listor:

* Kundlista  
* Leverantörslista  
* Artikellista  
* Redov.kontolista  

Exporterade data sparas som en IIF-fil som du sedan kan överföra [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
