---
title: Uppdatera valutakurser | Microsoft Docs
description: "För att använda flera valutor i din verksamhet kan du lägga upp en kod för varje valuta och använda en extern valutakurstjänst, som t.ex. FloatRates."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 35ecddf35dbe094ef05760ba4148f8ae79e7bf26
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="update-currency-exchange-rates"></a>Uppdatera valutakurser
Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.  

Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan granska och rapportera ekonomiska siffror i fler än en valuta. I programmet stöds användning av flera valutor. Redovisningen ställs in med hjälp av den lokala valutan (BVA) och en annan valuta ställs in som en alternativ valuta, med en tilldelad aktuell valutakurs.  

 Genom att ange en andra valuta som en alternativ rapporteringsvaluta kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t.ex. momstransaktioner. När redovisningstransaktionsbelopp beräknas i en alternativ rapporteringsvaluta används informationen från fönstret **Valutakurser** för att söka efter relevant valutakurs.  

> [!WARNING]  
>  Funktionen Alt. rapporteringsvaluta bör inte användas som underlag vid omräkning av ekonomirapporter. Verktyget kan inte användas för att utföra omräkningar av ekonomirapporter för utländska dotterbolag som en del i en företagskonsolidering. Funktionen Alt. rapporteringsvaluta ger endast möjligheten att förbereda rapporter i en annan valuta på ett sådant sätt som om den valutan var företagets lokala valuta.

## <a name="adjusting-exchange-rates"></a>Justera valutakurser  
Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats. Batch-jobbet Justera valutakurser används för att justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visa rapporter och belopp i den alternativa rapporteringsvalutan  
Med hjälp av en alternativ rapporteringsvaluta kan rapporteringsprocessen för ett företag förenklas i följande fall:  

- Företag i länder/regioner utanför EU som har en stor andel transaktioner med länder/regioner inom EU. I det här fallet kan landet utanför EU också vilja rapportera i euro för att göra sina ekonomirapporter mer användbara för sina EU-handelspartner.  

- Företag som också vill visa rapporter i en mer internationell handelsvaluta än sin egen lokala valuta.  

Redovisningstransaktioner används som underlag i flera rapporter i modulen Redovisning. Om du vill visa den ekonomiska informationen i rapporten i alternativ rapporteringsvaluta markerar du helt enkelt fältet **Visa i Lägg till valuta** i det relevanta fönstret för redovisningsrapporten.  

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fönstret **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Valutor** och välj sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** i fönstret **valutor** uppdateras med den senaste valutakursen.

## <a name="see-also"></a>Se även
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
