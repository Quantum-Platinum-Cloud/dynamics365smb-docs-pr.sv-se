---
title: "Så här ställer du in inköpstransaktioner för tredje part från EU-land"
description: "EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/10/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 598f3b8ccde8fdd677776dda79b0949eda0f5dbb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-eu-third-party-purchase-transactions"></a>Ställa in treparts EU-inköpstransaktioner
EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige. Transaktionsbeloppet måste identifieras och rapporteras separat i enlighet med de svenska reglerna för momsrapportering och kraven för systemet för utbyte av mervärdesskattedata (VAT Information Exchange System, VIES). [!INCLUDE[d365fin](../../includes/d365fin_md.md)] omfattar en svensk tilläggsfunktionalitet så att inköpstransaktioner kan ställas in som EU trepartshandel. Bokförda EU trepartstransaktioner kan då filtreras i momsrapporter och exkluderas från beloppet i kolumnen **Försäljning till kund** i rapporten **Moms- och kvartalsredovisning**.  

## <a name="to-set-up-eu-third-party-purchase-transactions"></a>Så här ställer du in EU trepartsinköpstransaktioner  

1.  Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.  
2.  Välj en befintlig inköpsfakturan eller åtgärden **Nytt** för att skapa en ny.  
3.  I snabbfliken **Fakturadetaljer** markerar du kryssrutan **Treparts EU-handel**.  
4.  Välj knappen **OK**.  

## <a name="see-also"></a>Se även  
 [Rapportera moms till skattemyndigheterna](../../finance-how-report-vat.md)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)
