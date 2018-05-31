---
title: "Ångra en bokföring genom att bokföra en mottransaktion | Microsoft Docs"
description: "Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9a4a7001ab5a752bf2e2acdd273d2a584a1e0b8a
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-postings"></a>Återföra bokningar
För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt. När du har återfört en post måste du skapa en korrekt post.

Du kan endast återföra poster som har bokförts från en redovisningsjournalrad. En transaktion kan endast återföras en gång.

Läs mer om hur du bokför från en redovisningsjournal i [Bokför transaktioner direkt till redovisningsjournalen](finance-how-post-transactions-directly.md).

Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.

Om du har bokfört fel positivt antal, till exempel om en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Att återföra bokföringen av en redovisningstransaktion journal
Du kan återföra poster från alla fönster **Transaktioner**. Följande procedur baseras fönstret **redovisningstransaktioner**.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningstransaktioner** och välj sedan relaterad länk.
2. Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**. Observera att det måste komma från en journalbokföring.
3. I fönstret **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.
4. Välj knappen **Ja** på bekräftelsemeddelandet.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Så här ångrar du ett bokfört antal i en bokförd inköspleverans  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokförda inköpsinleveranser** och välj sedan relaterad länk.  
2.  Öppna den bokförda inleveransen som du vill ångra.  
3.  Markera de rader som du vill ångra.  
4.  Välj åtgärden **Ångra inleverans**.

    En rättningsrad infogas under den valda inleveransraden.  

    Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.  

    Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Så här ångrar du ett bokfört antal i bokförda returleveranser

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokförda returutleveranser** och välj sedan relaterad länk.  
2.  Öppna den bokförda returutleveranser som du vill ångra.
3. Markera de rader som du vill ångra.  

4.  Välj åtgärden **Ångra returutleverans**.  

    En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.  

    Gå nu tillbaka till inköpsreturordern som är klar att bokföras.  

5.  Observera antalet i fältet **Returordernr** i fönstret **Returordernr**. .  
6.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsreturorder** och välj sedan relaterad länk.  
7.  Öppna returordern i fråga och välj åtgärden **öppna igen**.  
8.  Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.  

## <a name="to-post-a-negative-entry"></a>Bokföra en negativ transaktion  
Använd fältet **Korrigering** för att bokföra en negativ debet istället för en kredit, eller för att bokföra en negativ kredit istället för en debet för ett konto. För att uppfylla juridiska krav visas detta fält som standard i alla journaler. Fälten **Debetbelopp** och **Kreditbelopp** innehåller både ursprungstransaktionen och den korrigerade transaktionen. Dessa fält påverkar inte kontosaldot.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.  
2.  Välj önskat batch-namn i fältet **Batch-namn**.  
3.  Ange information i relevanta fält.  
4.  På journalraden som du vill aktivera för negativa poster väljer du kryssrutan **Korrigering**.  
5.  Välj åtgärden **Bokför** och välj sedan knappen **Ja** för att bokföra journalen.

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
