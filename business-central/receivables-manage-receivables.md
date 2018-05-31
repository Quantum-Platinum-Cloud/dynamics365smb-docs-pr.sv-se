---
title: "Översikt över uppgifter för hantering kundreskontra | Microsoft Docs"
description: "Innehåller information om hur du hanterar kundreskontra och kopplar betalningar till kund- eller leverantörstransaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3ffd3b31dcef871ceb30eae6a041f68a4972b2cb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="managing-receivables"></a>Hantera kundreskontra
En vanlig steg i alla finansiella takter är att stämma av bankkonton, som kräver att du kopplar betalningar till kund- eller leverantörsreskontratransaktioner för att stänga försäljningsfakturor och inköpskreditnotor.  

I [!INCLUDE[d365fin](includes/d365fin_md.md)], är ett av de snabbaste sätten att registrera betalningar från fönstret **Betalningsavstämningsjournal** genom att importera en bankutdragsfil feed. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på datamatchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra matchningrana innan du bokför journalen och avsluta bankkontotransaktioner för transaktioner när du bokför journalen. Bankkontot avstäms när alla utbetalningar kopplas.

Det finns dock andra praktiska ställen för att tillämpa betalningar och stämma av bankkonton:  

* Fönstret **Bankkontoavstämningar** låter dig kontrollera transaktionerna. Mer information finns i [Stämma av bankkonton separat](bank-how-reconcile-bank-accounts-separately.md).  
* Fönstret **Betalningsregistrering** där du kan tillämpa och manuellt kontrollera betalningar som tas emot som kontanter, check eller banktransaktion mot en skapad lista över obetalda försäljningsdokument. Observera att den här funktionen endast är tillgänglig för försäljningsdokument.  
* Fönstret **Inbetalningsjournal** där du kan manuellt bokföra kvitton till relevant redovisning, kund eller annat konto, genom att ange en betalningsrad. Du kan antingen använda kvittot eller återbetalningen till en eller flera öppna transaktioner, innan du bokför inbetalningsjournalen, eller från kundtransaktionerna.  

En annan del i hanteringen av kundfordringar är att kräva in utestående saldon inklusive dröjsmålsränta och skicka betalningspåminnelser. [!INCLUDE[d365fin](includes/d365fin_md.md)] erbjuder sätt att göra detta också. Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner baserade på en importerat kontoutdragsfil eller feed och stämma av bankkonton när alla betalningar är kopplade. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Koppla utbetalningar till öppna kundreskontratransaktioner som baseras på manuell inmatning i en lista över obetalda försäljningsdokument. |[Så här stämmer du av kundutbetalningar manuellt från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bokföring av inbetalningar eller återbetalningar för kunder i inbetalningsjournalen och koppla till kundreskontratransaktioner, antingen från journalen eller från bokförda transaktioner. |[Stäm av kundbetalningar manuellt](receivables-how-apply-sales-transactions-manually.md) |
| påminna kunder om förfallna belopp, beräkna dröjsmålsränta och hantera kundreskontra. |[Kräva in utestående saldon](receivables-collect-outstanding-balances.md) |
|Säkerställ att du vet kostnaden för levererade artiklar genom att tilldela extra artikelkostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer efter försäljning.|[Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)|
|Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.|[Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
