---
title: Arbeta med strukturer
description: Du kan skapa en monteringsstruktur eller produktionsstruktur för att ange vilka komponenter eller resurser som krävs för att sätta ihop artiklarna som strukturen representerar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: a-reishima
---
# <a name="work-with-bills-of-material" />Arbeta med strukturer

Du använder strukturlistor (stycklistor) till strukturens överordnade artiklar som monteras från andra artiklar eller tillverkas av resurser eller maskingrupper från komponenter.

## <a name="assembly-boms-or-production-boms" />Monteringsstrukturer eller produktionsstrukturer

[!INCLUDE[prod_short](includes/prod_short.md)] stöder två olika typer av strukturer:

| Strukturtyp | Kategorin Allmänt | Exempel |
| -------- | ---------------- | ------- |
| [Monteringsstrukturer](assembly-how-work-assembly-boms.md) | Distributionslager/montering | Artiklar som består av andra artiklar, monterade med grundläggande eller inga resurser. |
| [Produktionsstrukturer](production-how-to-create-production-boms.md) | Produktion | Artiklar som består av olika komponenter och delprodukter, produceras i en produktions- eller maskingrupp. |

Du använder monteringsorder för att slutboka artiklar från komponenter i en enkel sätt, som kan utföras av en eller flera grundläggande resurser, som inte är maskin- eller produktionsgrupper, eller utan något resurser. Det kan exempelvis vara en monteringsprocess att välja två som vinflaska och en kaffesäck och sedan packa dem som presentartiklar.  

En monteringsstruktur är mycket viktigt som definierar vilka komponentartiklarna ingår i en slutartikelmontering mot kundorder, och vilka resurser som används för att monterar monteringsartikeln. När du anger monteringsartikeln och ett antal i huvudet för en ny monteringsorder, fylls monteringsorderraderna i automatiskt enligt monteringsstrukturen med en monteringsorderrad per komponent eller resurs. Läs mer på [Monteringshantering](assembly-assemble-items.md).

Du använder produktionsorder för att slutboka artiklar från komponenter i en komplex behandling som kräver en verksamhetsföljd och en produktions- eller maskingrupper, som representerar produktionskapaciteterna. Det kan till exempel vara att en produktionsprocess klippa ut stålplattor i en operation, svetsar dem i nästa operation och färga slutartikeln i den senaste operationen. Läs mer på [Produktion](production-manage-manufacturing.md).

En produktionsstruktur är huvuddata som definierar en produktionsartikel och komponenter som ingår i den. För monteringsartiklar måste produktionsstrukturen godkännas och tilldelas produktionsartikeln innan den kan användas i en produktionsorder. När du anger produktionsartikeln på en produktionsorderrad, antingen manuellt eller genom att uppdatera order, då blir produktionsstrukturinnehållet produktionsorderkomponenterna. Läs mer på [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).

Begreppet av resurser i produktionen är mycket mer avancerad än i monteringshantering. Produktionsgrupper och maskingrupper fungerar som resurser, och produktionssteg representeras av operationer som tilldelas resurser i produktionsstrukturer. Mer information finns i artikeln [Skapa operationsföljder](production-how-to-create-routings.md).

Både monteringsorder och produktionsorder kan kopplas direkt till försäljningsorder. Du kan dock endast använda monteringsorder att anpassa slutartikeln direkt för en kundförfråga med försäljningsordern.

## <a name="see-also" />Se även

[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Hantera produktvarianter](inventory-item-variants.md)  
[Lager](inventory-manage-inventory.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
