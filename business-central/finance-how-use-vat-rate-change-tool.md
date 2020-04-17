---
title: Använda ändringsverktyget för momssats | Microsoft Docs
description: Använda ändringsverktyget för momssats
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992244"
---
# <a name="use-the-vat-rate-change-tool"></a>Använda ändringsverktyget för momssats

## <a name="understanding-the-vat-rate-conversion-process"></a>Förstå konverteringen av momssatsen  
Verktyget för momsändring utför momssatskonvertering för huvuddata, journaler och order på olika sätt. De valda huvuddata och journalerna uppdateras med den nya allmänna produktbokföringsmallen eller produktbokföringsmallen för moms. Om en order har levererats helt eller delvis, kommer de levererade artiklarna behålla den aktuella produktbokföringsmallen eller produktbokföringsmallen för moms. En ny orderrad skapas för de olevererade artiklarna och uppdateras för att stämma med den nuvarande och nya momsen eller allmänna produktbokföringsmallen. Dessutom ska artikelomkostnadsfördelningar, reservationer och artikelspårningsinformation uppdateras.  

Det finns några saker som verktyget inte konverterar:

* Försäljnings- eller inköpsorder och fakturor där leveranser har bokförts. Dessa dokumentet bokförs med hjälp av den aktuella momssatsen.  
* Dokument som har bokförda förskottsfakturor. Du har till exempel gjort eller tagit emot förskottsbetalningar för fakturor som inte har slutförts innan du använder ändringsverktyget för momssats. I det här fallet blir det en differens mellan momsen som har förfallit och momsen som har betalats i förskottsbetalningar när fakturan har slutförts. Ändringsverktyget för momssats hoppar över dessa dokument och du måste uppdatera dem manuellt.  
* Direktleveranser eller specialorder  
* Försäljnings- eller inköpsorder med lagerintegration om de är delvis levererade eller mottagna.  
* Servicekontrakt  

### <a name="to-prepare-vat-rate-change-conversions"></a>Så här förbereder du konverteringar av momssatser  
Innan du skapar ändringsverktyget för momssats, måste du göra följande förberedelser.

* Om du har transaktioner som används olika satser måste de delas upp i olika grupper, antingen genom att skapa nya redovisningskonton för varje sats eller genom att använda datafilter för att gruppera transaktioner efter sats.  
* Om du skapar nya redovisningskonton, måste du skapa nya generella bokföringsmallar.  
* Om du vill reducera antalet dokumentet som konverteras, bokför så många dokument som möjligt och minska ej bokförda dokument till en minimum.  
* Säkerhetskopiera data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Så här ställer du in ändringsverktyget för momssats  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för ändring av momssats** och välj sedan relaterad länk.  
2. På snabbflikarna **Huvuddata**, **Journaler** och **Dokument**, välj en bokföringsmall i alternativlistan för nödvändiga fält. För varje grupp kan du välja om du vill konvertera produktbokföringsmallar för moms eller generella produktbokföringsmallar, eller konvertera båda värdena om de är tillgängliga i huvuddataartikeln. För vissa områden kan du också definiera ett filter för att endast konvertera en delmängd av värden, till exempel redovisningskonton. 

### <a name="to-set-up-product-posting-group-conversion"></a>Så här skapar du konvertering av produktbokföringsmallar  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för ändring av momssats** och välj sedan relaterad länk.  
2. På sidan **Inställningar för ändring av momssats** väljer du åtgärden **Moms prod.bokf.mall, konv.** eller **Produktbokföringsmall, konv**.  
3. I fältet  **Från kod**, ange den aktuella bokföringsmallen.  
4. I fältet **Till kod** anger du den nya bokföringsgruppen.  

### <a name="to-perform-vat-rate-change-conversion"></a>Utföra konvertering för ändring av momssats  
Du använder momssatsändringsverktyget till rätta ändringar i standardsatsen för moms. Du utför moms och generella bokföringsmallkonverteringar för att ändra momssatser och underhålla exakt momsrapportering. Beroende på inställningen görs följande ändringar:  

* Moms- och bokföringsmallar konverteras.  
* Ändringar genomförs i redovisningskonton, kunder, leverantörer, öppna dokument, journalrader, o.s.v.  

> [!IMPORTANT]  
>  Innan du utför konverteringen av momssats, kan du testa konverteringen. Följ instruktionerna nedan för att göra det, men du måste avmarkera **utför konvertering** och **Ändringsverktyget för momssats har slutförts**. Under testkonverteringen avmarkerades fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och fältet **konverteras datum** i tabellen **Ändringsloggtransaktion för momssats** är tom. Välj **Ändringsloggtransaktion för momssats** för att visa resultatet av testkonverteringen. Kontrollera varje transaktion, innan du utför konverteringen. Kontrollera särskilt transaktioner som använder en gammal momssats.     

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ändring av momssats** och väljer sedan länken **Inställningar för ändring av momssats**.  
2. Kontrollera att du har ställt in konverteringen för momsproduktbokföringsmall eller produktbokföringsmall.  
3. Markera kryssrutan **utför konvertering**.  

    > [!IMPORTANT]  
    >  Avmarkera kryssrutan **Ändringsverktyget för momssats har slutförts**. Kryssrutan markeras automatiskt, när konverteringen av momssats slutförs.  

4. Välj åtgärden **Konvertera**.  
5. Välj åtgärden **Ändringsloggtransaktion för momssats** för att visa resultatet av konverteringen.  

> [!IMPORTANT]  
>  När konverteringen är klar markeras fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och **konverteras datum** i den **Ändringsloggtransaktion för momssats** fylls i med konverteringsdatumet.  
## <a name="see-also"></a>Se även  
[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt (moms)](finance-setup-unrealized-vat.md)      
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)