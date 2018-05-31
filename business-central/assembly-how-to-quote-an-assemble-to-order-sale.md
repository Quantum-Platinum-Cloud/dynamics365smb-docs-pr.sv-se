---
title: "Så här skapar du en offert för montering mot kundorder-försäljning | Microsoft Docs"
description: "Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 402745a9c90d1b82779e436f4a6533d2aed1b344
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Skapa en försäljning för montering mot kundorder
Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

När du säljer någon annan typ av artikel kan du också skapa en försäljningsoffert för en anpassad monteringsartikel innan du omvandlar den till en försäljningsorder. Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig försäljningsoffert. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsoffert.

> [!NOTE]  
>  Precis som på alla typer av offerter används inte antalet på monteringsoffertar för tillgänglighet, planering eller reservationer.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Så här skapar du en försäljningsoffert för en artikel för montering mot kundorder  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsoffert** och välj sedan relaterad länk.  
2.  Skapa en försäljningsoffertrad med en rad för en monteringsartikel. Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md).  
3.  I fältet **Antal att montera mot kundorder** anger du hela antalet.

    > [!NOTE]  
    >  Du bör inte erbjuda ett delantal i offerten. Därför måste du ange samma antal som du angett i fältet **Antal** på försäljningsoffertraden.  

4.  På snabbfliken **Rader** väljer du **Rad**, **Montering mot kundorder** och sedan **Montering mot kundorderrader**. Alternativt kan du välja fältet **Antal att montera mot kundorder** på raden.  
5.  I fönstret **Montering mot kundorderrader** granskar eller ändrar du monteringsorderrader enligt den offert som kunden begär. Om du vill ha mer information kan du välja åtgärden **Visa dokument** för att öppna hela avropsordern för offerten. Du kan inte ändra innehållet i de flesta fält, och du kan inte bokföra.  
6.  När du har justerat monteringsorderraderna enligt offerten stänger du fönstret **Montering mot kundorderrader** så att du kommer tillbaka till fönstret **Försäljningsoffert**.  
7.  Om kunden accepterar offerten skapar du en försäljningsorder för den offererade monteringsartikeln. Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md). Den länkade monteringsofferten och eventuella anpassningar är kopplad till den nya försäljningsordern så att artikelmontering eller -försäljning kan förberedas.  

## <a name="see-also"></a>Se även  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
