---
title: Om Lagerkostnad
description: 'Att hantera lagerkostnader är allt om registrering och rapportering av rörelsens driftskostnader, inklusive rapportering av produktionskostnader och lagerkostnader.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-inventory-costing" />Om Lagerkostnad
Hantering av Lagerkostnad används vid registrering och rapportering av rörelsens driftskostnader. Den omfattar rapportering av tillverkningskostnader och lagerkostnader, det vill säga varornas värdet.  

 Inom kostnadskalkylering måste du vara medveten om att värderingsprinciper anger hur varor värderas när de lämnar lagret, att kostnadsjusteringen uppdaterar kostnaderna för sålda varor med relaterad inköpskostnad som bokförs efter försäljningen och att lagervärdena måste bokföras på särskilda redovisningskonton med jämna mellanrum.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|skilja mellan de fem olika värderingsprinciperna och deras påverkan på kostnadsflöden.|[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)|  
|lära dig hur artikelkopplingstransaktioner dynamiskt kopplar lagerminskningar till lagerökningar så att kontrollen över kostnadsflödena bibehålls.|[Designdetaljer: Artikelkoppling](design-details-item-application.md)|  
|lära dig hur en artikels styckkostnad löpande uppdateras med kostnaden för dess senaste transaktion enligt artikelns värderingsprincip.|[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)|  
|lära dig hur en artikels genomsnittskostnad dynamiskt beräknas enligt den valda genomsnittskostnadsperioden.|[Designdetaljer: Genomsnittskostnad](design-details-average-cost.md)|  
|urskilja förväntad kostnad (ännu inte fakturerad) från faktisk kostnad och lära dig hur den hanteras i redovisningen.|[Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)|  
|förstå kostnadsjusteringsmekanismen, som säkerställer att kostnader flyttas fram även om lagertransaktioner sker slumpmässigt.|[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)|  
|veta varför standardkostnader ofta används av produktionsföretag som värderingsbas för komponenter och slutartiklar.|[Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md)|  
|förstå hur lagervärdet återspeglas i redovisningen.|[Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|lära dig hur artikelomkostnader, till exempel frakt och försäkring, kan tilldela ytterligare kostnadskomponenter till en artikels styckkostnad.|[Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)|  
|läsa om hur ett företag kan använda lagerperioder för att kontrollera lagervärdet över tid genom att definiera kortare perioder som kan stängas för bokföring under räkenskapsårets gång.|[Arbeta med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Förstå alla funktioner i kostnadsmotorn, inklusive vad som händer när du bokför transaktioner för montering och produktionsorder.|[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)|  

## <a name="see-also" />Se även
[Hantera lagerkostnader](finance-manage-inventory-costs.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
