---
title: Koppla transaktioner i olika valutor | Microsoft Docs
description: "Du kan koppla transaktioner i olika valutor om du t.ex.. säljer i en valuta och får betalningen i en annan valuta."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 960ae581a3f933c6e9c2ed5183944ddf62ca5965
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Aktivera koppling av kundreskontratransaktioner till olika valutor
Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.

Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.

Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner i fönstret **Inköpsinställningar**. Denna inställning liknar den för kundreskontratransaktioner i fönstret **Försäljningsinställningar**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsinställningar** och välj sedan relaterad länk.
2. I fältet **Koppling mellan valutor** markerar du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| Ingen |Koppling mellan valutor är inte tillåten. |
| EMU |Koppling mellan EMU-valutor är tillåten. |
| Alla |Koppling mellan alla valutor är tillåten. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Så här skapar du redovisningskonton för avrundningsdifferenser vid valutakoppling  
Om du kopplar transaktioner till olika valutor måste du ange de redovisningskonton som du vill bokföra avrundningsdifferenserna på.  

> [!NOTE]  
>  Du måste skapa redovisningskonton innan du slutför uppgiften. Mer information finns i [Förstå redovisning och kontoplan](finance-general-ledger.md).

1. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kundbokningsgruppen** och välj sedan relaterad länk.  
2. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  
3. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Leverantörsbokföringsmallar** och välj sedan relaterad länk.  
4. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
