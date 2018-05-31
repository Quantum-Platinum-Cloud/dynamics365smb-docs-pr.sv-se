---
title: "Så här skapar du specialorder | Microsoft Docs"
description: "Du kan skapa en specialorder för en specifik artikel som inte finns i lagret och som ska levereras till en specifik kund. Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 84b7a66734b3da5bdbc474bc43e463481c7f6ba5
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a>Skapa specialorder
Du kan skapa en specialorder för en specifik artikel som inte finns i lagret och som ska levereras till en specifik kund. Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order.  

Specialorder anger att inköps- och försäljningsordern är länkade för att säkerställa att den specifika ej lagerförda artikeln plockas och levereras till kunden.  

Innan den här funktionen kan användas måste de kund-, leverantörs- och artikelkort som behövs för ordern läggas upp.  

## <a name="to-create-a-special-order"></a>Så här skapar du en specialorder  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Skapa och fyll i  försäljningsorder för artikeln. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3.  Fyll i försäljningsraden på snabbfliken **Rader** . I fältet **Inköpskod**, välj en inköpskod som har fältet **Specialorder** markerat.

    Därefter måste du skapa en inköpsorder från ett inköpskalkylark.  
4. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpskalkylark** och välj sedan relaterad länk.  
5. Välj åtgärden **Specialorder** och väljer sedan åtgärden **Hämta förs.order**.  
6.  I fönstret **Hämta förs.order** visar resultat där **Verifikationsnr** är numret på försäljningsordern. Välj **OK**. En inköpskalkylarksrad skapas för artikeln.  
7.  På inköpskalkylarksraden, i fältet **Åtgärdsmeddelande**, väljer du **Ny**.  
8.  I fönstret **Inköpskalkylark** väljer du åtgärden **Verkställ åtgärdsmeddelande**. Fönstret **Skapa inköpsorder** visas. Välj knappen **OK**.  

    Du får meddelande om att inköpsorderna har skapats. Välj **OK**.  

En inköpsorder som skapas som en specialorder för en försäljningsorder respekteras av planeringssystemet när behov och tillgång balanseras. Det innebär att inköpsordern (tillgång) förblir länkad till försäljningsordern (behov) även om inköpsorden kan tillgodose ett annat, tidigare behov. Mer information finns i [Designdetaljer: Partiformningsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Du kan använda funktionen Specialorder om artikeln redan har reserverats. Därför, för artiklar som säljs på särskilda order, kontrollera att fältet **Reservera** på artikelkortet har angetts till **alltid**.  

## <a name="see-also"></a>Se även  
[Arbeta med ej lagerförda artiklar](inventory-how-work-nonstock-items.md)  
[Försäljning](sales-manage-sales.md)  
[Skapa direktleveranser](sales-how-drop-shipment.md)   
[Designdetaljer: Partiformningsmetoder](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
